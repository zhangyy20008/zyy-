因为之前在测试登录那块，所以没把新闻news表放到该数据库，现在进行了修改。自己对flask_Migrate刚上手，防止报错，所以在之前给哥的代码基础models.py加了两个类表示新闻和公司两个表。
自己很小白，不确定只有这一种方法，怕耽误哥时间，还是把这部分也复制上来了。



class CompanyModel(db.Model):
    __tablename__ = "company"
    c_id = db.Column(db.String(200),primary_key=True)
    c_name = db.Column(db.String(200), nullable=False)
    city = db.Column(db.String(20))

class NewsModel(db.Model):
    __tablename__ = "news"
    nid = db.Column(db.String(200),primary_key=True)
    c_id = db.Column(db.String(200), nullable=False)
    title = db.Column(db.String(200), nullable=False)
    author = db.Column(db.String(100), nullable=False)
    website = db.Column(db.String(200), nullable=False)
    time = db.Column(db.String(100), nullable=False)
    read = db.Column(db.Integer, nullable=False)
    comment = db.Column(db.Integer, nullable=False)
    sort = db.Column(db.String(100))
