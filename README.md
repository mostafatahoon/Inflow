 # Doctor Website Management Mobile App 
This is a mobile app designed to help doctors manage their website, appointments, and patient information. The app utilizes Retrofit to retrieve data from the API and an interceptor to include the access token in each request. 
It also includes two RecyclerViews, one for the date of the week and one for the appointments. The app uses a function to get the current date and time on the device and converts it using a simple format function. It also implements navigation using NavGraph and a navigation bottom bar. Glide is used to load and crop images retrieved from the API. Additionally, there is a function to determine if an appointment is finished or not based on the current time on the device, which dynamically updates the card displayed in the RecyclerView. 
 ## Features 
- View and check appointments for each day 
- Access and update doctor's profile 
- Write notes for each patient 
- Search for specific patients 
 ## Installation 
1. Clone the repository:  git clone https://github.com/your-repo-link.git>  
2. Open the project in your preferred IDE. 
3. Install the required dependencies using your package manager (e.g., Gradle, Maven). 
4. Build and run the app on your mobile device or emulator. 
 ## Configuration 
To configure the app, you need to provide the necessary API credentials and access token. Follow the steps below: 
1. Obtain the API credentials from your doctor website's backend team. 
2. Open the project and locate the  config  file. 
3. Replace the placeholder values with your API credentials. 
4. Generate an access token using the provided credentials and update the interceptor with the token.
// Update the interceptor with the access token
class MyInterceptor(var accessToken: String) : Interceptor {
    override fun intercept(chain: Interceptor.Chain): Response {
        val request = chain.request()
            .newBuilder()
            .addHeader("Authorization", "Bearer $accessToken")
            .build()
        return chain.proceed(request)
    }
}
## Usage 
1. Launch the app on your mobile device. 
2. Log in using your doctor credentials. 
3. Navigate through the app's different sections to view appointments, update profile, write patient notes, or search for specific patients. 
4. Enjoy using the app to manage your doctor website efficiently. 
 ## Contributing 
Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to submit a pull request or open an issue on the project repository. 
 ## License 
Gradution Project  
