## PAVEL KOZEL

**Phone:**	+375(29)1222894  
**Email:**	pavelshherba@yandex.ru  
**Telegram:** [https://t.me/Pavel2794](https://t.me/Pavel2794 "Telegram")  
**LinkedIn:**	[https://www.linkedin.com/in/pavel-kozel-likedin/](https://www.linkedin.com/in/pavel-kozel-likedin/ "LinkedIn")

#### Summary ####

Relocate to Minsk and working as a junior Android developer is my main goal for the near future. I am a purposeful and perspective young man who appreciates your and my own time. I consider myself sociable and this helps me quickly join the team and make good friends. I strive and like to learn new things, which contribute to my further development in various areas of life. Despite my young age, I managed to get enough experience to understand what I want to do in the future. I have been observing for a long time what kind of lifestyle my friends and brother working in the IT field lead, and I really want to become a part of this life. I really aim at the result when I decided to become an Android developer and I could not find the right courses in my city, I found them in Minsk and traveled from Gomel every weekend without missing a beat. I have come a long way, but this is only the beginning. I am quite a passionate person, and if I do something I try to do it as best as possible.

#### Skills ####

**Programming Languages:** Java, SQL, Kotlin(beginner)  
**IDE:** Android Studio, IntelliJ IDEA  
**Source Control:** Git  
**Databases:** SQLite  
**OS:** Android  
**Work with:** Activity, Service, BroadcastReceiver, ContentProviders, Location and Map API, View, Layout, SharedPreference, SQLite, Room, Material Design, DialogFragment, Notification API, Animation, Media, Camera, AlarmManager, Permissions. Unit tests, MVC/MVP/MVVM, RxJava and RxAndroid, Json and XML parser   
**Technology stack:** OkHttp/Retrofit2, Picasso/Glade, ButterKnife

#### Code example (LATEST) ####

I brought a part of the code from my graduation project, and I will add a link to it in the next paragraph.

    public class RepositoryImpl implements RepositoryDataBase, RepositoryNetworking {

    private static final String API_KEY = BuildConfig.API_KEY;
    private static final int MAX_PAGE = 500;    // page must be less than or equal to 500

    private static int PAGE;
    private static String LANGUAGE = Locale.getDefault().getLanguage();

    private final ExecutorService EXECUTOR =
            Executors.newFixedThreadPool(Runtime.getRuntime().availableProcessors() - 1);

    private FavoriteMovieDao favoriteMovieDao;
    private ApiService apiService;

    public RepositoryImpl(Application application) {
        favoriteMovieDao = FavoriteMovieDatabase.getInstance(application).getFavoriteMovieDao();

        Retrofit retrofit = ApiBuilder.getRetrofitClient(application.getApplicationContext());
        apiService = retrofit.create(ApiService.class);
    }

...

    @Override
    public CompletableFuture<Void> saveFavoriteMovieToDb(MovieModel movie) {
        MovieEntity movieEntity = new MovieEntity(movie);
        return CompletableFuture.supplyAsync(() -> {
                    favoriteMovieDao.insert(movieEntity);
                    return null;
                },
                EXECUTOR);
    }

...

    /*Call from Api*/
...

    @Override
    public Call<MovieResponse> getRandomPagePopularMovies() {
        PAGE = (int) (Math.random() * (MAX_PAGE - 1) + 1);
        return apiService.getPopularMovies(API_KEY, LANGUAGE, PAGE);
    }

...
}

#### Experience ####

My graduation project from It-academy: [https://bitbucket.org/Kozel_Pavel/grand-project/src/work_branch/](https://bitbucket.org/Kozel_Pavel/grand-project/src/work_branch/)

My code when I first came to courses: [https://bitbucket.org/Kozel_Pavel/it-academy-android-training/src/](https://bitbucket.org/Kozel_Pavel/it-academy-android-training/src/)

#### Education ####

***Nov 2019 - March 2020*** – **Educational Center for Programming and High Tech 
(IT-Academy)**  
**Course:** Android Application Development  
**Description:** This course helped me build up the necessary knowledge base for further development. I have real practice with MVC/MVP/MVVM patterns, RxJava/ RxAndroid, REST API, Google Play services and many other. The teacher-developer conducted classes and shared his experience with us, which helped to quickly acquire the necessary skills. Every week it was necessary to complete assignments, which helped to gain practical experience and learn to plan ahead. As a result of the course, I completed my grand projectand strengthened the desire to grow further.

****2016- 2018*** – **Polesye State University**  
Specialization:* Master's degree, Enterprise economics and management

***2011- 2016*** – **Gomel State Technical University named by P.O. Sukhoi**  
*Specialization:* Bachelor's degree, Industrial Engineering

#### English Proficiency ####

Pre-Intermediate (Read technical literature and articles, can speak on every day topics)