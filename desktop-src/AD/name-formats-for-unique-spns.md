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
ms.openlocfilehash: 3bda13cf5a095f8f2fd7ef1a209c6f3aeebd6654
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183002"
---
# <a name="name-formats-for-unique-spns"></a><span data-ttu-id="8e9bb-105">唯一 Spn 的名稱格式</span><span class="sxs-lookup"><span data-stu-id="8e9bb-105">Name Formats for Unique SPNs</span></span>

<span data-ttu-id="8e9bb-106">SPN 在註冊的樹系中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-106">An SPN must be unique in the forest in which it is registered.</span></span> <span data-ttu-id="8e9bb-107">如果不是唯一的，驗證將會失敗。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-107">If it is not unique, authentication will fail.</span></span> <span data-ttu-id="8e9bb-108">SPN 語法有四個元素：必須有兩個必要元素和兩個額外的元素，才能產生下表所列的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-108">The SPN syntax has four elements: two required elements and two additional elements that you can use, if necessary, to produce a unique name as listed in the following table.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e9bb-109">元素</span><span class="sxs-lookup"><span data-stu-id="8e9bb-109">Element</span></span></th>
<th><span data-ttu-id="8e9bb-110">描述</span><span class="sxs-lookup"><span data-stu-id="8e9bb-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e9bb-111">&quot;&lt;服務類別&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="8e9bb-111">&quot;&lt;service class&gt;&quot;</span></span></td>
<td><span data-ttu-id="8e9bb-112">識別服務之一般類別的字串。例如， &quot; SqlServer &quot; 。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-112">A string that identifies the general class of service; for example, &quot;SqlServer&quot;.</span></span> <span data-ttu-id="8e9bb-113">有已知的服務類別名稱，例如 &quot; web 服務的 www &quot; 或 &quot; &quot; 目錄服務的 ldap。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-113">There are well-known service class names, such as &quot;www&quot; for a web service or &quot;ldap&quot; for a directory service.</span></span> <span data-ttu-id="8e9bb-114">一般而言，這可以是服務類別唯一的任何字串。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-114">In general, this can be any string that is unique to the service class.</span></span> <span data-ttu-id="8e9bb-115">請注意，SPN 語法會使用正斜線 (/) 來分隔元素，因此此字元不能出現在服務類別名稱中。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-115">Be aware that the SPN syntax uses a forward slash (/) to separate elements, so this character cannot appear in a service class name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9bb-116">&quot;&lt;主機&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="8e9bb-116">&quot;&lt;host&gt;&quot;</span></span></td>
<td><span data-ttu-id="8e9bb-117">正在執行服務的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-117">The name of the computer on which the service is running.</span></span> <span data-ttu-id="8e9bb-118">這可以是完整的 DNS 名稱或 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-118">This can be a fully qualified DNS name or a NetBIOS name.</span></span> <span data-ttu-id="8e9bb-119">請注意，樹系中可能會有重複的 NetBIOS 名稱，如此包含 NetBIOS 名稱的 SPN 也可能不是唯一的 SPN。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-119">Be aware that NetBIOS names are not guaranteed to be unique in a forest, so an SPN that contains a NetBIOS name may not be unique.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e9bb-120">&quot;&lt;連接埠&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="8e9bb-120">&quot;&lt;port&gt;&quot;</span></span></td>
<td><span data-ttu-id="8e9bb-121">選擇性的埠號碼，可區別單一主機電腦上相同服務類別的多個實例。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-121">An optional port number to differentiate between multiple instances of the same service class on a single host computer.</span></span> <span data-ttu-id="8e9bb-122">如果服務針對其服務類別使用預設通訊埠，請省略此元件。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-122">Omit this component if the service uses the default port for its service class.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9bb-123">&quot;&lt;服務名稱&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="8e9bb-123">&quot;&lt;service name&gt;&quot;</span></span></td>
<td><span data-ttu-id="8e9bb-124">可複製服務的 Spn 中使用的選擇性名稱，用來識別服務或服務所服務之網域所提供的資料或服務。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-124">An optional name used in the SPNs of a replicable service to identify the data or services provided by the service or the domain served by the service.</span></span> <span data-ttu-id="8e9bb-125">此元件可以具有下列其中一種格式：</span><span class="sxs-lookup"><span data-stu-id="8e9bb-125">This component can have one of the following formats:</span></span>
<ul>
<li><span data-ttu-id="8e9bb-126">Active Directory Domain Services 中物件的辨別名稱或 objectGUID，例如服務連接點 (SCP) 。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-126">The distinguished name or objectGUID of an object in Active Directory Domain Services, such as a service connection point (SCP).</span></span></li>
<li><span data-ttu-id="8e9bb-127">服務之網域的 DNS 名稱，可為整個網域提供指定的服務。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-127">The DNS name of the domain for a service that provides a specified service for a domain as a whole.</span></span></li>
<li><span data-ttu-id="8e9bb-128">SRV 或 MX 記錄的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-128">The DNS name of an SRV or MX record.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8e9bb-129">存在於服務 Spn 中的元件，取決於服務的識別和複寫方式。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-129">The components present in a service's SPNs depend on how the service is identified and replicated.</span></span> <span data-ttu-id="8e9bb-130">有兩個基本案例：以主機為基礎的服務和可複製服務。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-130">There are two basic scenarios: host-based services and replicable services.</span></span>

## <a name="host-based-services"></a><span data-ttu-id="8e9bb-131">以主機為基礎的服務</span><span class="sxs-lookup"><span data-stu-id="8e9bb-131">Host-based services</span></span>

<span data-ttu-id="8e9bb-132">如果是以主機為基礎的服務，則 &lt; 會省略「服務名稱」 &gt; 元件，因為服務類別會唯一識別服務，以及安裝服務的主電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-132">For a host-based service, the "&lt;service name&gt;" component is omitted because the service is uniquely identified by the service class and the name of the host computer on which the service is installed.</span></span>


```C++
<service class>/<host>
```



<span data-ttu-id="8e9bb-133">服務類別只是用來識別用戶端服務所提供之功能的用戶端。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-133">The service class alone is sufficient to identify for clients the features that the service provides.</span></span> <span data-ttu-id="8e9bb-134">您可以在多部電腦上安裝服務類別的實例，而且每個實例都會提供使用其主機電腦識別的服務。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-134">You can install instances of the service class on many computers and each instance provides services that are identified with its host computer.</span></span> <span data-ttu-id="8e9bb-135">FTP 和 Telnet 是以主機為基礎的服務範例。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-135">FTP and Telnet are examples of host-based services.</span></span> <span data-ttu-id="8e9bb-136">如果服務使用非預設的埠，或主機上的服務有多個實例，則主機服務實例的 Spn 可以包含埠號碼。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-136">The SPNs of a host-based service instance can include the port number if the service uses a non-default port or there are multiple instances of the service on the host.</span></span>


```C++
<service class>/<host>:<port>
```



## <a name="replicable-services"></a><span data-ttu-id="8e9bb-137">可複製服務</span><span class="sxs-lookup"><span data-stu-id="8e9bb-137">Replicable services</span></span>

<span data-ttu-id="8e9bb-138">若為可複製服務，服務 (複本) 的一或多個實例，而且用戶端不會區分它們所連接的複本，因為每一個都提供相同的服務。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-138">For a replicable service there can be one or many instances of the service (replicas), and clients do not differentiate which replica they connect to because each provides the same service.</span></span> <span data-ttu-id="8e9bb-139">每個複本的 Spn 都有相同的「 &lt; 服務類別」 &gt; 和「 &lt; 服務名稱」 &gt; 元件，其中「 &lt; 服務名稱」 &gt; 更明確地識別服務所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-139">The SPNs for each replica have the same "&lt;service class&gt;" and "&lt;service name&gt;" components, where "&lt;service name&gt;" identifies more specifically the features provided by the service.</span></span> <span data-ttu-id="8e9bb-140">只有 " &lt; host &gt; " 和選擇性的「 &lt; 埠」 &gt; 元件會因 spn 而異。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-140">Only the "&lt;host&gt;" and optional "&lt;port&gt;" components would vary from SPN to SPN.</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="8e9bb-141">可複製服務的其中一個範例，就是提供指定資料庫存取權的資料庫服務實例。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-141">An example of a replicable service would be an instance of a database service that provides access to a specified database.</span></span> <span data-ttu-id="8e9bb-142">在此情況下，「 &lt; 服務類別」會 &gt; 識別資料庫應用程式，而「 &lt; 服務名稱」會 &gt; 識別特定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-142">In this case, "&lt;service class&gt;" identifies the database application and "&lt;service name&gt;" identifies the specific database.</span></span> <span data-ttu-id="8e9bb-143">「 &lt; 服務名稱」 &gt; 可能是服務連接點的分辨名稱 (SCP) 包含資料庫的連接資料。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-143">"&lt;service name&gt;" could be the distinguished name of a service connection point (SCP) containing connection data for the database.</span></span>


```C++
MyDBService/host1.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3.example.com/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="8e9bb-144">如果用戶端將使用 NetBIOS 名稱來撰寫服務的 SPN，則每個複本也必須註冊包含 NetBIOS 名稱的 SPN。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-144">If clients will use the NetBIOS name to compose a service's SPN, each replica must also register an SPN containing the NetBIOS name.</span></span>


```C++
MyDBService/host1/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host2/CN=hrdb,OU=mktg,DC=example,DC=com
MyDBService/host3/CN=hrdb,OU=mktg,DC=example,DC=com
```



<span data-ttu-id="8e9bb-145">可複製服務的另一個範例是提供服務給整個網域。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-145">Another example of a replicable service is one that provides services to an entire domain.</span></span> <span data-ttu-id="8e9bb-146">在此情況下，「 &lt; 服務名稱」 &gt; 元件是所服務之網域的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-146">In this case, the "&lt;service name&gt;" component is the DNS name of the domain being served.</span></span> <span data-ttu-id="8e9bb-147">Kerberos KDC 是這類可複製服務的範例。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-147">A Kerberos KDC is an example of this type of replicable service.</span></span>

<span data-ttu-id="8e9bb-148">請注意，如果電腦的 DNS 名稱有所變更，系統 &lt; &gt; 就會為樹系中該主機的所有已註冊 spn 更新 "host" 元素。</span><span class="sxs-lookup"><span data-stu-id="8e9bb-148">Be aware that if the DNS name of a computer changes, the system updates the "&lt;host&gt;" element for all registered SPNs for that host in the forest.</span></span>

 

 




