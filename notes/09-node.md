# 12/13/2022 Tuesday - CheckPoint 6 | PostIt example | FullStack

1. Get Collection in console. 

	- add albums [empty array] into AppState

	-
1.5. Not having a model:	

	class AlbumsService {

	async getAll()

	const await res.data()

	

2. Draw albums to the page - raw data dump	

	add {{albums}}
	
    
	in HomePage 
    setup(){

	onMounted {

	getAlbums()

	}

	return: {
        FilterBy,

	computed(() => {
        AppState.albums)
    }
	}

    }
    
    <div v-for="a in albums" class="col-12 col-md-3">
    <img :src="a.coverImg" class="img-fluid">
    <div>{{album.title}}</div>


    <style>
        .card-img{

        }
        </style>

Box Shadow:
.box{
    box-shadow 4pt 4 pt color:
}

2.2. Put all of the data (albums) into quickly styled divs; like cards with box shadow and change the colors


3. Create a Album Card
-Inject the template html into the album card; keep the 
<div v-for="a in albums" class="col-12 col-md-3">
and inside of it put <AlbumCard album = "a"/>

-in AlbumCard
add computed to the return; and import it to the top of script.

for just first album ->  album: computed(() => AppState.albums[0])
what we want to access 1 from the array ->   album: computed(() => AppState.albums[0])

<script>
    export default
props:{
    album: {type: Object, required: true}
}



\\\\\\\\\\\\\
HomePage

<buttons for navigation>
    <buttons @click="filterBy= 'tropical'">
        <buttons>
styling around: <AlbumCard album = "a"/>


    setup(){
    const filterBy = ref('')
	onMounted {
	getAlbums()

	}
	return: {
        FilterBy,
    albums: computed(() => {
        if(filterBy.value == ''){
            return AppState.albums
        } else {
            return AppState.albums.filter(a => a.category == filterBy.value)
        }
    })
	computed(() => {
        AppState.albums)
    }
	}

\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

4. <!--SECTION OMG HOW TO CHANGE PAGES VS LINK + FILTER-->-->

<button @click="filterBy="animals" class="btn btn-success selectable">Animals 🐇</button>

<!--NOTE - Vue homepage-->
<SCRIPT>
export default{
setup(){
    const filterBy = ref('')
    async function getAlbums(){
        try{
            await albumsService.getAll()
        } catch (error){
            Pop.error(error)
            logger.error(error)
        }
    }
	onMounted ((){
	getAlbums()
    })
	return: {
        filterBy,
    albums: computed(() => {
        if(filterBy.value == ''){
            return AppState.albums
        } else {
            return AppState.albums.filter(a => a.category == filterBy.value)
        }
    })	
}
}
</SCRIPT>

Pop.toast(`<h4 class="text-warning">Yellow warning!</1>`)
- you can add divs! and icons! and emojis
TO MAKE MDI ICONS SPIN: mdi-spin
mdi-spin
mdi-cat


props - v foring on something
props makes it singular

*************************************
<!--SECTION How to Draw the Component to Page:-->
<div v-for="a in albums" class="col-12 col-md-3">
<AlbumCard :album="a">
*************************************

\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\


*************************************
<!--SECTION How to link to other Pages:-->
5. NEW PAGE: ALBUM PAGE // will work to each albumId!
    1. Create new router to album page | these will take you to the AlbumPage.vue with that unique album Id, displayed on the HomePage // when hovered, shows link destination in bottom left
    In router.js:
    {
        path: '/albums/:albumId',
        name: 'AlbumId',
        component: loadPage('AlbumPage')
    }

    2. In AlbumCard.vue:
    <router-link :to="{name: 'Album', params:{albumId: album.id}}">
    <div class="card col-12 col-md-3 elevation-2 bg-dark px-3 selectable">
    <div>{{album.title}}</div>
    <img :src="">
    <i class="mdi mdi-heart-outline mdi-spin"></i>
    </div>
    </router-link>

    3. In AlbumPage functions 


<script>
    export default{
        setup(){
        const route = useRoute()
            async function getAlbumById(){
                try {
                    await albumsService.getAlbumById(route.params.albumId)
                }catch ("oh no!, error)
                 logger.error(error)
                }
            }
            onMounted(){
                getAlbumById()
            }
        }
</script>

*************************************

    4.
<script>
class AlbumsService{
async getAll(){

}

async getAlbumById(){
    const res = await api.get(albumById) // this isn't complete
}


}
</script>

5. Create PicturesService.js
<script>
    class PicturesService{
        getPicturesByAlbumId(){
            const res = await api.get('api/alums/' + albumId + '/pictures')
            // const res = await api.get('api/alums/' + `${albumId}/pictures')
            logger.log('[get pictures by album id]', res.data)
        }
    }
    export const picturesService = new PicturesService()
</script>

    1.5
<script>
    async function getPicturesByAlbumId(){
        try{
            await pcituresService.getPicturesByAlbumId()
        }
    }
    + add function to onMounted
    + now they are drawing to the console. go back to backend now.
</script>


6. BACKEND | SERVER
1. Create a Pictures Controller (we're going to find collaborators on album)
2. Create Collaborator.js Model
<script>

    export const CollaboratorSchema = new Schema({
        albumId: {type: Schema.Types.ObjectId, required: true, ref: 'Album'},
        accountId: { type: Schema.Types.ObjectId, required: true, ref:'Account'}
    }, {timestamps})
    Collaborators.virtual('album', {
        localFiel: 'albumId',
        ref: 'Album',
        foreignField: '_id',
        justOne: true
    })

    CollaboratorsSchema.virtual('account({
        loc
    })
</script>

2. create CollabsService.js + Controller | import + export
<script>
<!--this is the CollabsController-->
    export class CollabsController extents BaseController{
        constructor(){
            super('api/collaborators')
            this.router
            .use(Auth)
            .post('', this.create)
        }
        async create(req, res, next){
            try{
                req.body.accountId = req.userInfo.id
                let collab = await collabsService.create(req.body)
            }catch{
                (error)
            }
        }
    }
3. Add to DbContext
Collabs = mongoose.model('Collaborators', CollaboratorSchema)

    <!--this is the CollabsService-->
async 

</script>

CollabsController is simple; like; create + delete
CollabsService is simple; like; create + delete
The virtual is what confuses me



~ testing ~ - def need studying on that

<!--NOTE - ON REMOVE | Update AppState-->
await collab.remove()
const album = albumService.getOne()


<!--NOTE - ON REUSABLE MODAL-->
1. Make ModalComponent.vue
2. Put <ModalComponent /> in App.vue (to show on every page)
3. Take body out of ModalComponent body + title ect. So you can make it reusable, make unique on components to inject
**** add <slot></slot> ***** in ModalComponent body place; makes it reusable
4. Make create AlbumForm.vue component
5. <ModalComponent > 
    <slot></slot>
    <ModalComponent /> in App.vue
6. In Model
<slot name="header"></slot>
<slot name=""></slot>


7. AlbumForm.vue
tip: bootstrap floating labels for input in forms

****************
<template>
<div ="modal-header" id=""> put all modal body stuff here; top most line
<h1> Title Here </h1>
<button> close
</div>

<form @submit.prevent="createAlbum()">  - the <form> - modal-body goes inside of form to make it all a form
<div class="modal-body">
~ <form div and inputs ect here ~>
<div class="form-floating">
<import v-model="editable.coverImg">
</div>
<div class="form-floating">
<input v-model="editable.title">
</div>

<div class="modal-footer">
submit + cancel buttons
<div>

</form>
</template>

<script>    
import ref 

export default {
    setup(){
        const editable = ref({})
        return {
            editable,
            const router = useRouter()
            async createAlbum(){
                try {
                    logger.log(editable.value) // edit this line out after it works
                const album = await albumsService.createAlbum(editable.value)
                editable.value = {} // this line makes the form empty after submit
                Modal.getOrCreateInstance('#exampleModal').hide() // hides form after submit!
                router.push({name: 'Album', params: {albumId: album.id}})
                } catch {
                    error(error)

                }
            }
        }
    }
}
</script>


Now, go to AlbumsService

async createAlbum(body){
    const res = await api.post('api/albums', body)
    logger.log('[create album]', res.data)
    AppState.albums.push(res.data)   // unshift only works well if database works that way? //Sort? idk 
    return res.data // lets us use unshift with the router on the formpage
}





8. Render new Album data to the AlbumPage


onMounted()

<template>
container-fluid
row 
row
<divs v-if="album" class="col-3"> /// this is the column with album creator info and collaborators
col-12
<img :src="album.cover" class="img-fluid rounded">
<div>{{album.title}}</div>
<div>by {{album.creator.name}}</div>  //  nested object to get the creator name
</divs>
<div class="col-12 d-flex">
<div>
{{album.memberCount}} Collaborators
</div>
<button class="btn btn-outline-light">
<div> Collab + heart icon</div>
</button>



row
<div class="col-8"> /// this col has all the pictures in the picture album
<div class="row">
<div v-for="p in pictures" class="col-3">
<a tag here to make a link when the pic is clicked to make it bigger>
<img :src:"p.imgUrl" class="selectable">
</div>
//// add pictures: [] in APPSTATE
add AppState.pictures.get() // to the Pictures Service get() function
<div v-for="c in collabs" class="col-6 col-md-6">
<img :src="c.profile.picture" class="img-fluid elevation-2 rounded selectable" :title="c.profile.name"> // can see name when hovered, with Title


</template>

.cover-img{
    box-shadow: 3pt 3pt #color
}

<script>
    export default{
        setup(){
        const route = useRoute()
            async function getAlbumById(){
                try {
                    await albumsService.getAlbumById(route.params.albumId)
                }catch ("oh no!, error)
                 logger.error(error)
                }

                async function getPicturesByAlbumId
            }
            async getCollabsByAlbumId(){
                await collabsService.
                
            }
            onMounted(){
                getAlbumById()
                getPicturesByAlbumId()
                getCollabsByAlbumId()
            }
            return{
                album: computed(() => AppState.album)
                pictures: computed(() => AppState.pictures)
                collabs: computed(()=> AppState.collabs)
            }
        }
</script>

add getCollabs to CollabsService
<script>
async getCollabsByAlbumId(albumId){
const res = await api.get('api/albums/' + albumId + 'collaborators')
logger.log('[]', res.data)
appState.collabs = res.data

}
</script>

add collabs: [empty array in APPSTATE]

****************




9. Set up, can click collaborator + see user's Collabs Albums
// on homepage: 

<script>
async function getMyCollabAlbums(){
    try{
        await collabsService.getMyCollabAlbums()
    }catch
    error
}

onMounted:
getMyAlbums()
getMyCollabAlbums() // can remove this with the Auth call below

// In CollabsService

async getMyCollabAlbums(){
    try{
    const res = await api.get('account/collaborators')
    logger.log('[get collab albums]', res.data)
    AppState.myCollabs = res.data
    } catch
    log error
}

// TEST

//AuthService.js -> section for adding things once user is authorized 
collabsService.getMyCollabAlbums()

//Add to AppState | myCollabs: []

// at top of HomePage - Under container-fluid + row || will go on top of the feed of albums

<div class="">My Collabs</div>
<div v-for="c in myCollabs" class=" col-12 col-md-3 p m"> // control size with styling
<AlbumCard :album="c.album">
</div>

                //script
return{
    editable,
    myCollabs: computed(()=> AppState.myCollabs)
    xxx
}
</script>



add pop alert to delete - to ask if sure; in controller

*******
*******
v-if="account.id"    | only see if logged in
******!SECTION****

v-if="account.id && ticketHolder" | only shows my events if I'm a ticket holder










*************************************
<!--SECTION Parameters:-->
: makes vue know you're supporting a param (parameter)
***********************************

<script>
</script>



<!--TODO - Study / Homework-->

1. Finish Vue videos
2. Finish Bootstrap videos
3. Build my own Inspire homepage
4. Build site I can write poetry on



<!--TODO - Web Apps to Make-->
1. Inspire, but real
- create a new TODO web app that I can actually use; so like, with the server ect.
2. Poet 
- Create a poetry webapp for my poems. maybe.... have all of them on there. then there can be collections, like seperate books you need a token for, and some that are free write collections. i can create private ones. Super rad.. it could be a poetry creator for me!
- can use form to create new poems to save to database
3. Music Player
- create a simple open home page web app that has genres/vibes and collections of music that I love on it, that I can 
4. Sautrah
- create a simple (becuz simple is beautiful) webpage for Sautrah
- book me, music, coding, poetry, media, contact, gaming (wanna twitch again)
5. Flow Dojo
- create a simple (like, sample start) web app for FlowDojo // merch, hire, media, details + contact


<!--TODO - Sautrah / Business-->
1. low fidelity sautrah page
2. high fidelity sautrah page
3. copyright Sautrah
4. Buy URL Sautrah
5. Build first test website for Sautrah


<!--SECTION - -->
Sautrah Pages / components
1. Book as a DJ, front end developer, poet, gamer
2. Music (...loading) + page + home page music loader to mixes and originals
3. Coding | links to github + webapps i have build
4. Poetry
5. Media
6. About/Bio
7. Account
8. Contact
9. Copyright

HomePage Links:
1. ^ above things
2. links to social media ect.




<!--SECTION - Questions -->
1. How to build ToDo into a site with my own server // so it actually works. Do I buy domain name for it? I have ideas for several web apps to build; will be good practice, good for me to use, good for my resume/portfolio
    1.5. Do I use our fullstack vue creator to try this out? Does it sit on github? or buy domain? How do I make an actual inspire I can use?
2. Virtuals?? ahhhh virtuals on schemas confuse me. Populate?
3. computed  - 
4. How to load pagination. Say you load 20 per page, how do you go to next and draw the next 20? + add in specific id? ()
5. Quick way to format date stream so it isn't crap? Maybe just mm/dd/yyyy + time

<!--SECTION - Tudor request 12/13/2022 -->
Virtuals on Schemas + Pagination + Real Aps
1. Virtuals confuse me; could we breakdown how they are written and used? Maybe a little description of populate, computed, getBy params vs query? 2. Simple Pagination? (if that exists) 3. How do you add a quick reload (like a watch) on a page turn, or a post form submit, or click on profile link, 'likePost() ect? Is it onMounted, on return in function? return on Page.vue? 4. Quick format date? So it doesn't come out all crazy 5. Inspire app I can use irl; how to build that in the future? Do I use a server/github/domain?