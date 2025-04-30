# **Cella’s Manhwa**

Cella, si ratu scroll Facebook, tiba-tiba terinspirasi untuk mengumpulkan informasi dan foto dari berbagai **manhwa favoritnya**. Namun, kemampuan ngoding Cella masih cetek, jadi dia butuh bantuanmu untuk membuatkan skrip otomatis agar semua berjalan mulus. Tugasmu adalah membantu Cella mengolah data manhwa dan heroine-nya.

Berikut adalah daftar manhwa bergenre shoujo/josei yang paling disukai Cella:

|    No     |      Manhwa      |
| :--------: | :------------: |
| 1 | Mistaken as the Monster Duke's Wife |
| 2 | The Villainess Lives Again |
| 3 | No, I Only Charmed the Princess! |
| 4 | Darling, Why Can't We Divorce? |

### **a. Summoning the Manhwa Stats**

Cella ingin mengambil data detail dari **manhwa** menggunakan [API Jikan](https://docs.api.jikan.moe/). Informasi yang diambil:

- Judul
- Status
- Tanggal rilis
- Genre
- Tema
- Author

Setelah data berhasil diambil, hasilnya harus disimpan ke dalam file teks, dengan nama file disesuaikan dengan **judul versi bahasa Inggris** (tanpa karakter khusus dan spasi diganti dengan underscore). Semua file teks disimpan dalam folder `Manhwa`.

**Contoh format isi file:**

```
Title: The Villain's Daughter-in-Law
Status: Publishing
Release: 2024-10-16
Genre: Fantasy, Romance
Theme: Time Travel
Author: Na, Reuyan, Kim, Dael
```

**&#128161; Hint**

Contoh Penggunaan Simple API:
1. Kunjungi situs **MyAnimeList**.

2. Cari **manhwa** yang diinginkan.

3. Sebagai contoh:

    `https://myanimelist.net/manga/154063/The_Perks_of_Being_a_Villainess`

3. Gunakan **154063** sebagai **ID** untuk melakukan pengambilan data (scraping).

4. Sehingga **endpoint API** akan menjadi seperti berikut:

    `https://api.jikan.moe/v4/manga/154063`

### **b. Seal the Scrolls**

Cella ingin agar setiap file `.txt` tadi di-**zip** satu per satu dan disimpan ke dalam folder baru bernama `Archive`. Yang dimana nama masing masing dari zip diambil dari **huruf kapital nama file**.

### **c. Making the Waifu Gallery**

Setiap manhwa memiliki heroine alias **Female Main Character (FMC)**. Cella ingin mengunduh gambar heroine dari internet, dengan jumlah unduhan sesuai dengan **bulan rilis manhwa**.

**Contoh:**

- Jika rilis bulan Februari → unduh **2 foto**
- Jika rilis bulan Desember → unduh **12 foto**
- Format nama file: `Heroine_1.jpg`, `Heroine_2.jpg`, dst.

Selain itu, Cella ingin melakukan pengunduhan **sesuai urutan** daftar manhwa yang tertera pada deskripsi di atas, dan proses pengunduhan harus menggunakan **thread**, karena Cella malas menunggu. Sebagai contohnya, gambar heroine dari manhwa Mistaken as the Monster Duke's Wife harus diunduh terlebih dahulu dan tidak boleh didahului oleh gambar heroine dari manhwa lainnya.

Seluruh gambar akan disimpan dalam folder Heroines. Di dalam folder Heroines, akan terdapat subfolder dengan nama depan atau nama panggilan heroine dari masing-masing manhwa.

Struktur folder yang diinginkan:

```
Heroines/
├── Alisha/
│   ├── Alisha_1.jpg
│   └── Alisha_2.jpg
└── Dorothea/
    ├── Dorothea_1.jpg
    └── Dorothea_2.jpg
```

### **d. Zip. Save. Goodbye**

Setelah semua gambar heroine berhasil diunduh, Cella ingin mengarsipkannya:

- Setiap folder heroine di-zip dengan format:
  ```
  [HURUFKAPITALNAMAMANHWA]_[namaheroine].zip
  ```
- Disimpan di folder `Archive/Images`
- Setelah zip selesai, gambar pada masing masing folder Heroine akan dihapus secara **urut dengan abjad**.

### Notes &#9888;

- Gunakan `fork()` dan `exec()` untuk soal a, b, dan, d.

- `system()` **HANYA BOLEH DIGUNAKAN (bila ingin)** untuk soal c.

- **Dilarang keras menggunakan external script!**.

- Dilarang menggunakan `mkdir()`.

- Hanya `solver.c` yang dikumpulkan pada GitHub.

---

# **Cella’s Manhwa**

Cella, the queen of Facebook scrolling, suddenly got inspired to collect information and photos from her favorite **manhwa**. However, her coding skills are still basic, so she needs your help to create an automated script to make everything run smoothly. Your task is to assist Cella in processing manhwa data and its heroines.

The following is a list of shoujo/josei genre manhwa most favored by Cella:

|    No     |      Manhwa      |
| :--------: | :------------: |
| 1 | Mistaken as the Monster Duke's Wife |
| 2 | The Villainess Lives Again |
| 3 | No, I Only Charmed the Princess! |
| 4 | Darling, Why Can't We Divorce? |

### **a. Summoning the Manhwa Stats**

Cella wants to retrieve detailed data about **manhwa** using the [Jikan API](https://docs.api.jikan.moe/). The information to be retrieved includes:

- Title
- Status
- Release date
- Genre
- Theme
- Author

Once the data is successfully retrieved, the results must be saved into a text file, with the file name based on the **English title** (special characters removed and spaces replaced with underscores). All text files are stored in the `Manhwa` folder.

**Example file content format:**

```
Title: The Villain's Daughter-in-Law
Status: Publishing
Release: 2024-10-16
Genre: Fantasy, Romance
Theme: Time Travel
Author: Na, Reuyan, Kim, Dael
```

**&#128161; Hint**

Example of Simple API Usage:
1. Visit the **MyAnimeList** website.

2. Search for the desired **manhwa**.

3. For example:

    `https://myanimelist.net/manga/154063/The_Perks_of_Being_a_Villainess`

4. Use **154063** as the **ID** for scraping the data.

5. Therefore, the **API endpoint** will look like this:

    `https://api.jikan.moe/v4/manga/154063`

### **b. Seal the Scrolls**

Cella wants each `.txt` file to be **zipped** individually and stored in a new folder named `Archive`. The name of each zip file should be derived from the **uppercase letters of the file name**.

### **c. Making the Waifu Gallery**

Each manhwa has a heroine, also known as the **Female Main Character (FMC)**. Cella wants to download heroine images from the internet, with the number of downloads corresponding to the **release month of the manhwa**.

**Example:**

- If released in February → download **2 photos**
- If released in December → download **12 photos**
- File name format: `Heroine_1.jpg`, `Heroine_2.jpg`, and so on.

Additionally, Cella wants the downloads to be performed **in order** based on the manhwa list described above, and the download process must use **threads**, as Cella doesn’t want to wait. For example, the heroine images from the manhwa Mistaken as the Monster Duke's Wife must be downloaded first and cannot be preceded by images from other manhwa.

All images will be stored in the Heroines folder. Inside the Heroines folder, there will be subfolders named after the first name or nickname of the heroine from each manhwa.

Desired folder structure:

```
Heroines/
├── Alisha/
│   ├── Alisha_1.jpg
│   └── Alisha_2.jpg
└── Dorothea/
    ├── Dorothea_1.jpg
    └── Dorothea_2.jpg
```

### **d. Zip. Save. Goodbye**

After all heroine images are successfully downloaded, Cella wants them archived:

- Each heroine folder is zipped with the format:
  ```
  [UPPERCASEMANHWANAME]_[heroineName].zip
  ```
- Stored in the `Archive/Images` folder
- Once the zipping is complete, the images in each Heroine folder will be deleted **in alphabetical order**.

### Notes &#9888;

- Use `fork()` and `exec()` for questions a, b, and d.

- `system()` **MAY ONLY BE USED (if desired)** for question c.

- **Strictly prohibited from using external scripts!**

- Using `mkdir()` is not allowed.

- Only `solver.c` should be submitted on GitHub.


# Jawaban
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>
#include <unistd.h>
#include <sys/types.h>
#include <sys/wait.h>
#include <dirent.h>      
#include <pthread.h>

void Folder(const char *foldername){
    pid_t pid = fork();
    if (pid == 0) {
        execlp("mkdir", "mkdir", "-p", foldername, NULL);
        perror("mkdir failed");
        exit(EXIT_FAILURE);
    } 
    else wait(NULL);
}

void fetchJSON(const char *id){
    pid_t pid = fork();
    if (pid == 0){
        char url[256];
        snprintf(url, sizeof(url), "https://api.jikan.moe/v4/manga/%s/full", id);
        execlp("curl", "curl", "-s", "-o", "response.json", url, NULL);
        perror("execlp failed");
        exit(EXIT_FAILURE);
    } 
    else wait(NULL);
}

void cleanTitle(char *dest, const char *src){
    while (*src){
        if (isalnum(*src))*dest++ = *src;
        else if (*src == ' ')*dest++ = '_';
        src++;
    }
    *dest = '\0';
}

void parseAndSave(){
    FILE *fp = fopen("response.json", "r");
    if (!fp) {
        perror("Buka response.json gagal");
        return;
    }
    char buffer[8192];
    fread(buffer, 1, sizeof(buffer), fp);
    fclose(fp);
    // Title
    char *judulPtr = strstr(buffer, "\"title\"");
    char title[256] = "Unknown";
    if (judulPtr) sscanf(judulPtr, "\"title\": \"%[^\"]", title);
    // Status
    char *statusPtr = strstr(buffer, "\"status\"");
    char status[128] = "Unknown";
    if (statusPtr) sscanf(statusPtr, "\"status\": \"%[^\"]", status);
    // Release Date
    char *tglPtr = strstr(buffer, "\"from\"");
    char release[128] = "Unknown";
    if (tglPtr){
        char fullDate[128];
        sscanf(tglPtr, "\"from\": \"%[^\"]", fullDate);
        // ambil cmn 10 karakter pertama
        strncpy(release, fullDate, 10);
        release[10] = '\0'; 
    }
    // Genre
    char *genrePtr = strstr(buffer, "\"genres\":");
    char genre[512] = "";
    if (genrePtr){
        char *g = strstr(genrePtr, "\"name\":");
        while (g && g < strstr(buffer, "\"themes\"")){
            char temp[64];
            sscanf(g, "\"name\": \"%[^\"]", temp);
            strcat(genre, temp);
            strcat(genre, ", ");
            g = strstr(g + 1, "\"name\":");
        }
        if (strlen(genre)) genre[strlen(genre) - 2] = '\0';  
    }
    // Theme
    char *themePtr = strstr(buffer, "\"themes\":");
    char theme[256] = "";
    if (themePtr){
        char *themeEnd = strstr(themePtr, "\"demographics\"");
        char *t = strstr(themePtr, "\"name\":");
        while (t && (!themeEnd || t < themeEnd)){
            char temp[64];
            sscanf(t, "\"name\": \"%[^\"]", temp);
            strcat(theme, temp);
            strcat(theme, ", ");
            t = strstr(t + 1, "\"name\":");
        }
        if (strlen(theme)) theme[strlen(theme) - 2] = '\0'; 
    }
    // Author
    char *authorPtr = strstr(buffer, "\"authors\":");
    char authors[256] = "";
    if (authorPtr){
        char *authorEnd = strstr(authorPtr, "\"serializations\"");
        char *a = strstr(authorPtr, "\"name\":");
        while (a && (!authorEnd || a < authorEnd)){
            char temp[64];
            sscanf(a, "\"name\": \"%[^\"]", temp);
            strcat(authors, temp);
            strcat(authors, ", ");
            a = strstr(a + 1, "\"name\":");
        }
        if (strlen(authors)) authors[strlen(authors) - 2] = '\0';
    }

    // Save ke file
    char filename[256];
    cleanTitle(filename, title);
    char filepath[300];
    sprintf(filepath, "Manhwa/%s.txt", filename);
    FILE *out = fopen(filepath, "w");
    if (!out){
        perror("Gagal menulis file output");
        return;
    }
    fprintf(out, "Title: %s\n", title);
    fprintf(out, "Status: %s\n", status);
    fprintf(out, "Release: %s\n", release);
    fprintf(out, "Genre: %s\n", genre);
    fprintf(out, "Theme: %s\n", theme);
    fprintf(out, "Author: %s\n", authors);
    fclose(out);
}

void Uppercase(char *dest, const char *src) {
    int j = 0;
    for (int i = 0; src[i] != '\0'; i++) if (isupper(src[i]))dest[j++] = src[i];
    dest[j] = '\0';
}

// Upprcase_Heroin
typedef struct {
    const char* heroine;
    const char* manhwa_code;
} HeroineInfo;
HeroineInfo heroines[] = {{"Adelia",  "NIOCTP"}, {"Artezia", "TVLA"}, {"Lia",     "MMDW"}, {"Ophelia", "DWCD"}};

void Zipmanga() {
    Folder("Archive");
    
    // Buka direct
    DIR *dir = opendir("Manhwa");
    if (!dir){
        perror("Cannot open Manhwa directory");
        return;
    }
    
   struct dirent *entry;
    while ((entry = readdir(dir)) != NULL){
        if (entry->d_type == DT_DIR || !strstr(entry->d_name, ".txt"))continue;

        printf("Found file: %s\n", entry->d_name);

        char filename[256];
        // delete ekstensi file
        strncpy(filename, entry->d_name, sizeof(filename) - 1);
        filename[sizeof(filename) - 1] = '\0';
        // path
        char source[512];
        snprintf(source, sizeof(source), "Manhwa/%s", entry->d_name);
        char *dot = strrchr(filename, '.');
        if (dot) *dot = '\0';
        char uppercase[256] = {0};
        Uppercase(uppercase, filename);
        char dest[512];
        snprintf(dest, sizeof(dest), "Archive/%s.zip", uppercase);
        printf("Zipping %s to %s\n", source, dest);

        // fork & exec untuk zip
        pid_t pid = fork();
        if (pid == 0) {
            execlp("zip", "zip", "-j", dest, source, NULL);
            perror("Zip failed");
            exit(EXIT_FAILURE);
        } 
        else wait(NULL);
    }
}

void ZipAkhir() {
    Folder("Archive/Images");

    const int n = sizeof(heroines) / sizeof(HeroineInfo);

    for (int i = 0; i < n; i++) {
        const char* heroine = heroines[i].heroine;
        const char* manhwa_code = heroines[i].manhwa_code;
        char zipname[256];
        snprintf(zipname, sizeof(zipname), "Archive/Images/%s_%s.zip", manhwa_code, heroine);
        char folder[256];
        snprintf(folder, sizeof(folder), "Heroines/%s", heroine);

        // fork & exec untuk zip
        pid_t pid = fork();
        if (pid == 0){
            execlp("zip", "zip", "-r", zipname, folder, NULL);
            perror("Zip failed");
            exit(EXIT_FAILURE);
        } 
        else wait(NULL);
    }
    for (int i = 0; i < n; i++) {
        const char* heroine = heroines[i].heroine;

        char folder[256];
        snprintf(folder, sizeof(folder), "Heroines/%s", heroine);

        DIR* dir = opendir(folder);
        if (!dir) {
            perror("opendir failed");
            continue;
        }

        struct dirent* entry;
        // delete isi direct
        while ((entry = readdir(dir)) != NULL) {
            if (entry->d_type == DT_REG && strstr(entry->d_name, ".jpg")) {
                char filepath[512];
                snprintf(filepath, sizeof(filepath), "%s/%s", folder, entry->d_name);
                remove(filepath); 
            }
        }

        closedir(dir);
    }
}

// Buat folder (Soal C only)
void makeFolder(const char* path) {
    char cmd[256];
    snprintf(cmd, sizeof(cmd), "mkdir -p \"%s\"", path);
    system(cmd);
}

// Link" Heroine
typedef struct {
    const char* heroine;   
    const char* image_url; 
    int count;             
} DownloadTask;

void* downloadImages(void* arg) {
    DownloadTask* task = (DownloadTask*)arg;
    // utk folder heroine
    char folder[256];
    snprintf(folder, sizeof(folder), "Heroines/%s", task->heroine);
    makeFolder(folder);
    // donlod
    for (int i = 0; i < task->count; i++) {
        char filename[300];
        snprintf(filename, sizeof(filename), "Heroines/%s/%s_%d.jpg",
                 task->heroine, task->heroine, i + 1);
        char cmd[512];
        snprintf(cmd, sizeof(cmd), "curl -s %s -o \"%s\"",
                 task->image_url, filename);
        system(cmd);
    }
    pthread_exit(NULL);
}

int main() {
    fetchJSON("168827");  // Mistake
    parseAndSave();
    fetchJSON("147205");  // The vilainess
    parseAndSave();
    fetchJSON("169731");  // No, i charmed
    parseAndSave();
    fetchJSON("175521");  // Divorce
    parseAndSave();
    Zipmanga();
    makeFolder("Heroines");
    const char* url_lia     = "https://i.imgur.com/CJuHmrb.png";
    const char* url_artezia = "https://i.imgur.com/5c9Lcs5.png";
    const char* url_adelia  = "https://i.imgur.com/zF3Jq8s.png";
    const char* url_ophelia = "https://i.imgur.com/5GyLoVN.png";
    Folder("Manhwa");
    DownloadTask tasks[] = {
        {"Lia",     url_lia,     3}, // Maret
        {"Artezia", url_artezia, 6}, // June
        {"Adelia",  url_adelia,  4}, // April
        {"Ophelia", url_ophelia, 10}  // Oktober
    };

    const int n = sizeof(tasks) / sizeof(DownloadTask);

    for (int i = 0; i < n; i++) {
        pthread_t tid;
        pthread_create(&tid, NULL, downloadImages, (void*)&tasks[i]);
        pthread_join(tid, NULL);  // Downloadnya urut
    }

    ZipAkhir();

    return 0;    
}

```
