# django-template

1. **イメージを作成する**  
```
docker build -t <image_name> .
```

1. **プロジェクトを作成する**  
```
docker run --rm -v $(pwd):/app <image_name> django-admin startproject <project_name> .
```

1. **アプリ（機能）を作成する**  
```
docker run --rm -v $(pwd):/app <image_name> python manage.py startapp <app_name>
```

1. **アプリを起動する**  
```
docker run --rm -v $(pwd):/app -p 8000:8000 <image_name>
```

### 備考
- 適宜settings.pyのデータベース情報を更新する必要がある。
- 初期設定のまま起動すると、db.sqlite3ファイルが自動作成される。
- デタッチドモードで起動する場合はオプションで`-d`をつける
