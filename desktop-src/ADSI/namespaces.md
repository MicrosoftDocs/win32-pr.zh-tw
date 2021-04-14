---
title: 命名空間
description: 位於指定命名空間內的物件是由唯一名稱所識別。
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- 命名空間 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371839"
---
# <a name="namespaces"></a><span data-ttu-id="e4738-104">命名空間</span><span class="sxs-lookup"><span data-stu-id="e4738-104">Namespaces</span></span>

<span data-ttu-id="e4738-105">位於指定命名空間內的物件是由唯一名稱所識別。</span><span class="sxs-lookup"><span data-stu-id="e4738-105">Objects that reside within a given namespace are identified by a unique name.</span></span> <span data-ttu-id="e4738-106">例如，儲存在電腦磁片磁碟機上的檔案位於檔案系統命名空間中。</span><span class="sxs-lookup"><span data-stu-id="e4738-106">For example, files stored on a PC disk drive reside in the file system namespace.</span></span> <span data-ttu-id="e4738-107">檔案的唯一名稱是以檔案系統命名空間中儲存的位置為基礎。</span><span class="sxs-lookup"><span data-stu-id="e4738-107">The unique name of a file is based on where it is stored in the file system namespace.</span></span> <span data-ttu-id="e4738-108">例如：</span><span class="sxs-lookup"><span data-stu-id="e4738-108">For example:</span></span>


```C++
C:\public\documents\adsi\adsi_spec.doc
```



<span data-ttu-id="e4738-109">目錄服務命名空間也會以唯一的名稱來識別它們所包含的物件，這些物件通常是以可找到物件的目錄中的位置為基礎。</span><span class="sxs-lookup"><span data-stu-id="e4738-109">Directory service namespaces also identify the objects they contain by unique names which are usually based on the location in the directory where the object can be found.</span></span> <span data-ttu-id="e4738-110">例如，在 X-y 目錄中，指定的物件可能會有如下的名稱：</span><span class="sxs-lookup"><span data-stu-id="e4738-110">For example, in an X.500 directory, a given object might have a name like this:</span></span>


```C++
CN=John,OU=Marketing,O=Fabrikam
```



<span data-ttu-id="e4738-111">不同的目錄服務會使用不同的格式來命名其所包含的物件。</span><span class="sxs-lookup"><span data-stu-id="e4738-111">Different directory services use different forms for naming the objects they contain.</span></span> <span data-ttu-id="e4738-112">這會處理不同的命名空間，特別是針對開發人員，考慮程式碼可能正在執行的所有不同環境。</span><span class="sxs-lookup"><span data-stu-id="e4738-112">This makes dealing with different namespaces challenging, especially for developers, considering all of the different environments on which the code might be running.</span></span>

<span data-ttu-id="e4738-113">Active Directory 服務介面 (ADSI) 的目標是要提供命名架構，以允許存取不同目錄服務提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="e4738-113">A goal of Active Directory Service Interfaces (ADSI) is to provide a naming framework that allows access to namespaces of different directory service providers.</span></span>

<span data-ttu-id="e4738-114">ADSI 定義可以在異類環境中唯一識別物件的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="e4738-114">ADSI defines a naming convention that can uniquely identify an object in a heterogeneous environment.</span></span> <span data-ttu-id="e4738-115">這些名稱稱為 ADsPath 字串。</span><span class="sxs-lookup"><span data-stu-id="e4738-115">These names are called ADsPath strings.</span></span> <span data-ttu-id="e4738-116">ADsPath 字串採用數種形式：</span><span class="sxs-lookup"><span data-stu-id="e4738-116">ADsPath strings take several forms:</span></span>


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



<span data-ttu-id="e4738-117">其他的 ADsPath 格式可由不同的 ADSI 提供者引進 (例如 Internet Information Services server 的 ADSI 提供者，它支援 "IIS://" ADsPaths) 。</span><span class="sxs-lookup"><span data-stu-id="e4738-117">Additional ADsPath formats can be introduced by different ADSI providers (such as the ADSI provider for the Internet Information Services server, which support the "IIS://" ADsPaths).</span></span>

 

 




