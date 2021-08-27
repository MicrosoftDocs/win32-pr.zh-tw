---
title: 唯一 Spn 的名稱格式
description: SPN 在註冊的樹系中必須是唯一的。
ms.assetid: dd3f9f7c-b64c-4bd8-924f-a8880ee3b71e
ms.tgt_platform: multiple
keywords:
- 唯一 Spn AD 的名稱格式
- 服務主體名稱 AD、名稱格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b041f88bc025c604ec5f0ad9a6bf5ba7f4cdabc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472333"
---
# <a name="name-formats-for-unique-spns"></a>唯一 Spn 的名稱格式

SPN 在註冊的樹系中必須是唯一的。 如果不是唯一的，驗證將會失敗。 SPN 語法有四個元素：必須有兩個必要元素和兩個額外的元素，才能產生下表所列的唯一名稱。


```C++
<service class>/<host>:<port>/<service name>
```






| 元素 | 描述 | 
|---------|-------------|
| "<service class>" | 識別服務之一般類別的字串。例如，"SqlServer"。 有已知的服務類別名稱，例如 web 服務的 "www" 或目錄服務的 "ldap"。 一般而言，這可以是服務類別唯一的任何字串。 請注意，SPN 語法會使用正斜線 (/) 來分隔元素，因此此字元不能出現在服務類別名稱中。 | 
| "<host>" | 正在執行服務的電腦名稱稱。 這可以是完整的 DNS 名稱或 NetBIOS 名稱。 請注意，樹系中可能會有重複的 NetBIOS 名稱，如此包含 NetBIOS 名稱的 SPN 也可能不是唯一的 SPN。 | 
| "<port>" | 選擇性的埠號碼，可區別單一主機電腦上相同服務類別的多個實例。 如果服務針對其服務類別使用預設通訊埠，請省略此元件。 | 
| "<service name>" | 可複製服務的 Spn 中使用的選擇性名稱，用來識別服務或服務所服務之網域所提供的資料或服務。 此元件可以具有下列其中一種格式：<ul><li>Active Directory Domain Services 中物件的辨別名稱或 objectGUID，例如服務連接點 (SCP) 。</li><li>服務之網域的 DNS 名稱，可為整個網域提供指定的服務。</li><li>SRV 或 MX 記錄的 DNS 名稱。</li></ul> | 




 

存在於服務 Spn 中的元件，取決於服務的識別和複寫方式。 有兩個基本案例：以主機為基礎的服務和可複製服務。

## <a name="host-based-services"></a>以主機為基礎的服務

如果是以主機為基礎的服務，則 &lt; 會省略「服務名稱」 &gt; 元件，因為服務類別會唯一識別服務，以及安裝服務的主電腦名稱稱。


```C++
<service class>/<host>
```



服務類別只是用來識別用戶端服務所提供之功能的用戶端。 您可以在多部電腦上安裝服務類別的實例，而且每個實例都會提供使用其主機電腦識別的服務。 FTP 和 Telnet 是以主機為基礎的服務範例。 如果服務使用非預設的埠，或主機上的服務有多個實例，則主機服務實例的 Spn 可以包含埠號碼。


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a>可複製服務

若為可複製服務，服務 (複本) 的一或多個實例，而且用戶端不會區分它們所連接的複本，因為每一個都提供相同的服務。 每個複本的 Spn 都有相同的「 &lt; 服務類別」 &gt; 和「 &lt; 服務名稱」 &gt; 元件，其中「 &lt; 服務名稱」 &gt; 更明確地識別服務所提供的功能。 只有 " &lt; host &gt; " 和選擇性的「 &lt; 埠」 &gt; 元件會因 spn 而異。


```C++
<service class>/<host>:<port>/<service name>
```



可複製服務的其中一個範例，就是提供指定資料庫存取權的資料庫服務實例。 在此情況下，「 &lt; 服務類別」會 &gt; 識別資料庫應用程式，而「 &lt; 服務名稱」會 &gt; 識別特定的資料庫。 「 &lt; 服務名稱」 &gt; 可能是服務連接點的分辨名稱 (SCP) 包含資料庫的連接資料。


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



如果用戶端將使用 NetBIOS 名稱來撰寫服務的 SPN，則每個複本也必須註冊包含 NetBIOS 名稱的 SPN。


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



可複製服務的另一個範例是提供服務給整個網域。 在此情況下，「 &lt; 服務名稱」 &gt; 元件是所服務之網域的 DNS 名稱。 Kerberos KDC 是這類可複製服務的範例。

請注意，如果電腦的 DNS 名稱有所變更，系統 &lt; &gt; 就會為樹系中該主機的所有已註冊 spn 更新 "host" 元素。

 

 




