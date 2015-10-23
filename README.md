# gradle-mvn-push
上传aar到更美Maven库

### 1.在gradle.properties文件中增加描述信息【全局gradle.properties或Module的gradle.properties文件中均可】

    GROUP=xxx.xxx.xxx
    VERSION_NAME=1.0.0
    POM_ARTIFACT_ID=xxx
    SNAPSHOT_REPOSITORY_URL=http://xxx.xxx.xxx/nexus/content/repositories/gengmei-android-snapshots/
    RELEASE_REPOSITORY_URL=http://xxx.xxx.xxx/nexus/content/repositories/gengmei-android/
  
### 2.在local.properties文件中填写用户名和密码
  
    user=xxxx
    password=xxxx
  
### 3.在需要打包aar并上传到Maven仓库的Module的build.gradle文件末尾添加依赖

    apply from: 'https://raw.githubusercontent.com/GMAndroidTeam/gradle-mvn-push/master/gradle-mvn-push.gradle'
  
### 4.执行上传命令

    ./gradlew upload
