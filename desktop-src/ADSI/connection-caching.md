---
title: 連接快取
description: 當連接到伺服器時，會在用戶端電腦上快取連接控制碼，直到該連線關閉為止。
ms.assetid: 927afd35-8703-4234-b6a8-6320a3667532
ms.tgt_platform: multiple
keywords:
- 連接快取 ADSI
- 連接快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857d102a52be9c7ccf40f9076892a85d5b3b8683
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020803"
---
# <a name="connection-caching"></a><span data-ttu-id="8e957-105">連接快取</span><span class="sxs-lookup"><span data-stu-id="8e957-105">Connection Caching</span></span>

<span data-ttu-id="8e957-106">當連接到伺服器時，會在用戶端電腦上快取連接控制碼，直到該連線關閉為止。</span><span class="sxs-lookup"><span data-stu-id="8e957-106">When a connection to a server is made, the connection handle is cached on the client computer for that process until that connection is closed.</span></span> <span data-ttu-id="8e957-107">如果在後續連線中使用相同的伺服器、埠和認證，而且只有 **ads \_ 快速 \_** 系結或 **ads \_ 伺服器 \_** 系結驗證旗標不同，ADSI 將會重複使用現有的連接。</span><span class="sxs-lookup"><span data-stu-id="8e957-107">If the same server, port, and credentials are used in a subsequent connection, and only the **ADS\_FAST\_BIND** or **ADS\_SERVER\_BIND** authentication flags differ, ADSI will reuse the existing connection.</span></span> <span data-ttu-id="8e957-108">ADSI 會以每個進程為基礎執行此連接快取。</span><span class="sxs-lookup"><span data-stu-id="8e957-108">ADSI performs this connection caching on a per-process basis.</span></span>

<span data-ttu-id="8e957-109">若要提高效能，請盡可能重複使用現有的連接。</span><span class="sxs-lookup"><span data-stu-id="8e957-109">To increase performance, reuse existing connections when possible.</span></span>

<span data-ttu-id="8e957-110">下列程式碼範例示範連接快取的運作方式。</span><span class="sxs-lookup"><span data-stu-id="8e957-110">The following code example shows how connection caching works.</span></span>


```VB
Dim cachedConn As IADs
Dim obj As IADs
Dim cachedName As String
Dim objName As String
 
' Connect to the server and maintain this handle to cache the connection.
Set cachedConn = GetObject("LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com")
 
cachedName = cachedConn.Get("distinguishedName")
Debug.Print (cachedName)
 
' Reuse the connection to MyMachine opened by cachedConn.
' Be aware that this line executes quickly because it is not required
' to transmit over the network again.
Set obj = GetObject("LDAP://MyMachine/CN=Bob,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection.
Set obj = Nothing
 
' Reuse the connection to MyMachine opened by cachedConn again.
Set obj = GetObject("LDAP://MyMachine/CN=Administrator,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection again.
Set obj = Nothing
 
' Release the first connection.
Set cachedConn = Nothing
 
' The connection to MyMachine is closed.
```



 

 




