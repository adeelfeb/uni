<img src="./tk2ygs0a.png"
style="width:3.6525in;height:1.86917in" /><img src="./n1fro0st.png"
style="width:5.07569in;height:1.27147in" />

> <u>CLOUD CONCEPTS S3</u>
>
> (Simple Storage Service)
>
> • **Amazon** **S3** is a virtual storage service provided by Amazon,
> which can be accessed from anywhere at any time through internet
> access. Common examples of such types of storage are Dropbox, OneDrive
> and google drive (provide 15GB of free space for storage). Just as in
> google drive only software is stored or saved but it cannot be
> installed. Likewise, S3 is also object level storage.
>
> • **Max** **Storage** **of** **a** **bucket** **is** **5TB.** •
> **Types** **of** **Storage:**
>
> o Block Level Storage: Can be used as a storage device and allows the
> installation of software. E.g., Hard disk drive and in cloud context
> the default hard drive (30GB) attached to EC2 (windows server) is
> block level storage.
>
> o Object Level Storage: Do not provide operation level access
> (installation) only storage is provided.
>
> • Objects are stored in buckets. The bucket in cloud is same as folder
> and object could be any file type say media file, image, or any type
> of document. Buckets must not have the same names. Multiple objects
> can be stored in a bucket.
>
> ✓ Key has the folder, file name and the extension which is an object
> to be stored in a bucket.

• Say you are in the North Virginia Region with 6 availability zones
(physical data centers) and you want to store an object. Whenever you
store an object, it is spread amongst multiple AZ. Now, if you want to
delete any stored object, it won’t be deleted immediately because copies
of that object are in various AZs. First all the copies are deleted, and
the object is deleted. Same is the case with modification or updating an
object. This is **<u>an eventual consistency model</u>** in which any
operation performed on an object will take time as all the changes in an
object will be replicated amongst all the copies.

> o In context of Data Redundancy Model there are two types of models: ▪
> Eventual consistency model
>
> ▪ Read after write model. (Access the data as it is created e.g.,
> renaming of file in a bucket)

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./3ppmd3us.png"
style="width:5.7525in;height:3.20917in" /><img src="./xqddn2zr.png"
style="width:5.01528in;height:2.46722in" /><img src="./t2mktpv5.png"
style="width:4.3925in;height:2.1975in" /><img src="./yimskkfn.png"
style="width:4.9775in;height:1.20917in" />

> ➢ The data is only shared in all the AZs of that region, but it will
> not be shared outside the region. This can be done and known as CORS
> (Cross origin resource sharing).
>
>  How cost can be minimized?  How data can be made secure?
>
> • S3 is designed for seamless scaling it will automatically handle
> high volume of requests. S3 can manage the data storage behind your
> bucket if data size exceeds 5TB and allows you to put more data.
>
> • Data can be accessed anywhere through Dashboard, Command Line
> Interface, or AWS SDK.

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./ilp1mtlj.png"
style="width:5.22083in;height:1.0025in" /><img src="./nyffpvqt.png"
style="width:5.32083in;height:1.02918in" /><img src="./gdc1xqli.png"
style="width:5.31083in;height:1.01251in" /><img src="./u3x0uvnl.png"
style="width:5.20167in;height:1.6868in" /><img src="./0vlvbogb.png"
style="width:4.57847in;height:1.06317in" />

> <img src="./r1aojqls.png"
> style="width:2.7775in;height:1.07585in" />• **S3** **Storage**
> **Classes:** There are 6 types of storage classes. o **<u>Standard
> Storage:</u>** This is the default storage in
>
> S3. The data kept in this storage can be accessed as soon as it is
> created. Since it makes data available immediately it costs a lot.
> Hence it is recommended to use this storage for testing purposes not
> as permanent storage.
>
> o **<u>Standard Infrequent Access:</u>** If data is to be accessed
> frequently this type of class is recommended. Say if you want to
> access the data once a week or once a month put the data in IA bucket.
> This way the cost for storage is minimized and you will be charged
> when you access the data.
>
> o **<u>One zone Infrequent Access:</u>** It is just like *Standard*
> *Infrequent* *Access,* but the difference is when data is stored in
> *Standard* *Storages,* they spread the data in all the zones in a
> region while in *one* *zone* *IA*, data is kept in one Availability
> Zone only. Problem with one zone IA is that in case of accidental
> deletion all the data is lost. Since there is no back up it is less
> recommended and has a very low cost.
>
> o **<u>Intelligent Tiering:</u>** It is an intelligent class which
> automatically moves the data to low-cost solutions. E.g., if stored
> data is not accessed for a long period of time, it will automatically
> move that data to the low-cost storage class. Main limitation for this
> feature is that file size must be equal to or greater than 120 KB.
>
> o **<u>Glacier:</u>** If the data is to be stored for long term and
> the access time is very low this class is recommended. In this class
> stored data cannot be accessed before 90 days (min). In case of an
> emergency access, a request must be generated before 3 – 5 hours. A
> new modification in this class allows <u>expedited retrieval
> access</u> which is charged.
>
> o **<u>Glacier Deep Archive:</u>** It is same as Glacier class, but
> the access time is 180days or 6 months (min). Data in this storage can
> also be accessed through expedited retrieval or access request.

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./1qo15b34.png"
style="width:3.91417in;height:2.6875in" /><img src="./gclc5mv0.png"
style="width:3.11417in;height:1.93083in" /><img src="./cwpd2eaz.png"
style="width:3.25917in;height:1.94583in" />

>  If any class is not selected at the time of storage creation the
> default storage i.e., standard storage is created which can be changed
> later.
>
> <img src="./am3xwfgs.png"
> style="width:2.61583in;height:2.52083in" /> Versioning is enabled for
> backup not enabled by default. It is recommended for Disaster
> Recovery.  Other Applications:

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./4dzv4jnj.png" style="width:5.8875in;height:1.97in" /><img src="./temdpz2i.png"
style="width:6.49833in;height:1.74444in" /><img src="./4ujifs1n.png"
style="width:4.72833in;height:1.36042in" />

> <u>DEMO</u>
>
> <img src="./o1rtuxtv.png"
> style="width:3.03917in;height:1.33751in" /><img src="./us1n3ukt.png"
> style="width:1.15418in;height:0.53753in" /><img src="./xkbtugqt.png"
> style="width:1.15585in;height:0.53753in" /><img src="./jmgmdd0c.png"
> style="width:1.15417in;height:0.53753in" /><u>(Lab creating a bucket
> with object and access it through browser.)</u>
>
> Create a bucket

Upload File Images

Access through Browser

> • Search for S3 or go through Services.
>
> • Dashboard for storage S3
>
> • AWS Market place

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./kwxt5jml.png"
style="width:6.49792in;height:1.75694in" /><img src="./twqylzhd.png"
style="width:6.49847in;height:2.00833in" /><img src="./ix5mlpyi.png"
style="width:6.49681in;height:2.36528in" /><img src="./ssfqkw3j.png"
style="width:6.49639in;height:0.48055in" />

> • Create a bucket.
>
> • Enter the bucket name. Bucket name must be unique and can be as long
> as 63 characters (digit only, alphabets or alphanumeric can be used).
> There must not be a capital letter. As each object is accessed through
> a specific URL.
>
> • It is a global service that can be accessed from any region.
> *Region* *selection* *option* *is* *optional*.
>
> • Existing buckets can be used *(optional)*.

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./ltdsk2ef.png"
style="width:6.49903in;height:2.04236in" /><img src="./cpnlzonr.png"
style="width:6.49722in;height:2.56111in" /><img src="./xqexcsk3.png"
style="width:6.49819in;height:2.08472in" />

> • Public access option can be checked or unchecked.
>
> • Bucket Versioning is disabled by default and works as a backup. It
> is used to create different versions of a file. In case of accidental
> deletion, different versions of a file will be available.
>
> • Tagging (naming) can be done.

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./k4lm211a.png"
style="width:6.49708in;height:1.30556in" /><img src="./bzsafvce.png"
style="width:6.49847in;height:1.77847in" />

> • Default encryption is disabled. Can be enabled.
>
> <img src="./g0jrv3rt.png"
> style="width:6.49764in;height:2.14375in" />• In advanced setings
> objects can be locked which disables the access of the object by any
> other. After that click on create bucket.
>
> <img src="./p5tr2ckk.png"
> style="width:6.49764in;height:2.13958in" />• **Name** **error:** Name
> already exists it means that there exists a bucket around somewhere
> with same name though we do not have any bucket in our bucket list.
>
> ’

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./y03owuhs.png"
style="width:6.49917in;height:1.67639in" /><img src="./neimjfao.png"
style="width:6.49736in;height:2.07569in" /><img src="./qhltcks3.png"
style="width:6.49708in;height:2.35625in" />

> • Change the name and create the new bucket.
>
> • To store the object, click on the bucket name.
>
> • See the properties tab to explore different configurations like
> tagging, intelligent tiering, static web hosting, encryption, bucket
> versioning, object locking etc.
>
> • In permission public access is managed and bucket level permissions.
>
> • Now click on object. You can add object directly or can place an
> object in a folder. Click on upload.

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./0x5mt54r.png"
style="width:6.49764in;height:2.10555in" /><img src="./emcc4xyl.png"
style="width:6.49792in;height:1.95278in" /><img src="./ztg1bsvf.png"
style="width:6.49778in;height:0.90208in" />

> • Click on files and upload any image file and file is added.
>
> • Destination is the bucket name.
>
> <img src="./nvmwiqxo.png"
> style="width:6.49722in;height:2.38611in" /><img src="./00m0vgpr.png"
> style="width:6.49875in;height:0.57014in" />• Click on upload. File
> will be uploaded. Disturbing internet connection will result in
> unsuccessful upload or any other problem.

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./s1tm1w5u.png"
style="width:6.48389in;height:0.29305in" /><img src="./1hoi4zwt.png"
style="width:6.49931in;height:2.37417in" /><img src="./xbzmojlr.png"
style="width:6.49764in;height:2.14861in" /><img src="./enbbd4ay.png"
style="width:6.49986in;height:1.23403in" />

> • Click on file name.
>
> • Object is created with default setings.
>
> • Click on URL and open it in browser.
>
> <img src="./03a0qlcs.png"
> style="width:6.49653in;height:1.05486in" />• Access denied error is
> due to setings that public access of bucket is blocked. Change the
> setings by allowing public access and try again.
>
> Go-to permissions click on edit uncheck the option and click save
> changes.

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./rimi1ris.png"
style="width:6.49819in;height:2.05486in" /><img src="./11wojual.png"
style="width:6.4975in;height:2.44653in" /><img src="./4t0m3sdb.png"
style="width:6.49931in;height:1.47639in" />

> • And type confirm.
>
> <img src="./gudm44ml.png"
> style="width:6.4975in;height:1.06319in" />• Next step is to make
> object publicly accessible. Click on object then click on Permissions
> and click on edit.

E & OE

*Handouts:* *Drakhshan* *Bokhat*

<img src="./hlnpyqdw.png"
style="width:6.49847in;height:2.22917in" /><img src="./r5l2smu4.png"
style="width:6.49653in;height:1.33958in" />

> • Check the options and save the changes and refresh the browser page
> to view the file.

E & OE

*Handouts:* *Drakhshan* *Bokhat*
