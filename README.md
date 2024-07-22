### RabbitMQ Projesi README

# RabbitMQ Projesi

Bu proje, Udemy kurs materyallerine dayanarak RabbitMQ'nun çeşitli özelliklerini ve desenlerini gösteren örneklerin bir koleksiyonudur. Her örnek, farklı mesajlaşma desenlerini ve kullanım durumlarını gösteren bir konsol uygulaması olarak yapılandırılmıştır. Aşağıda, ele alınan konuların ve ilgili uygulamaların ayrıntılı bir açıklaması bulunmaktadır.

## İçindekiler

1. [HelloWorld](#helloworld)
2. [Work Queues](#work-queues)
3. [Publish/Subscribe](#publishsubscribe)
4. [Routing](#routing)
5. [Topics](#topics)

## HelloWorld

**HelloWorld** örneğinde, RabbitMQ'ya basit bir mesaj gönderen ve bu mesajı alan temel bir yapı oluşturulmuştur. Bu derste, bir mesaj gönderici (producer) ve bir mesaj alıcı (consumer) oluşturulmuştur. Mesaj gönderici "Hello World!" mesajını RabbitMQ kuyruğuna gönderirken, mesaj alıcı bu mesajı kuyruktan alıp ekrana yazdırır.

## Work Queues

![Screenshot_6](https://github.com/user-attachments/assets/77a0e304-2d41-4398-801f-f8ab986d1803)


**Work Queues** örneğinde, iş yükünü birden fazla çalışan arasında dağıtmak için iş kuyrukları kullanılmıştır. Bir mesaj gönderici, "task_queue" isimli bir kuyrukta görevler oluşturur ve bu görevler bir veya daha fazla çalışan (worker) tarafından işlenir. Görevlerin işlenme süresi, mesajın içeriğine bağlı olarak dinamik bir şekilde belirlenir.

## Publish/Subscribe

![Screenshot_1](https://github.com/user-attachments/assets/70bc10a3-2dc4-453d-b87a-64c4bb050be6)


**Publish/Subscribe** örneğinde, birden fazla alıcıya (subscriber) aynı mesajı göndermek için "fanout" değişim tipi kullanılmıştır. Mesaj gönderici (producer) bir mesaj yayınlar ve bu mesaj tüm bağlı alıcılara gönderilir. Bu senaryoda, mesajlar bir log sistemine veya birden fazla servise dağıtılabilir.

## Routing

![routing](https://github.com/user-attachments/assets/24c84f2b-05d2-44be-8061-271ccfb98bc1)


**Routing** örneğinde, mesajların belirli rotalar üzerinden yönlendirilmesi sağlanmıştır. Bu örnekte, "direct" değişim tipi kullanılarak mesajlar belirli bir anahtar kelime (routing key) ile yönlendirilir. Mesaj gönderici, belirli bir anahtar kelime ile bir mesaj gönderir ve bu mesaj, yalnızca ilgili anahtar kelimeye sahip alıcılar tarafından alınır.

## Topics

![topics](https://github.com/user-attachments/assets/bd7e290a-648f-42f7-9089-d7a173ddc7b7)


**Topics** örneğinde, mesajların konulara göre yönlendirilmesi sağlanmıştır. Bu örnekte, "topic" değişim tipi kullanılarak mesajlar belirli bir desen (pattern) ile yönlendirilir. Mesaj gönderici, belirli bir konu (topic) ile bir mesaj gönderir ve bu mesaj, ilgili desenle eşleşen alıcılar tarafından alınır. Bu, daha esnek ve dinamik bir mesaj yönlendirme sağlar.

---

Bu proje, RabbitMQ'nun temel kavramlarını ve kullanım senaryolarını anlamak için pratik bir rehber sunmaktadır. Her ders, belirli bir mesajlaşma desenini ve RabbitMQ'nun sunduğu farklı özellikleri açıklamaktadır.
