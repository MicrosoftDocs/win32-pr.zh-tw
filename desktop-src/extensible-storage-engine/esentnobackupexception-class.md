---
description: 深入瞭解： EsentNoBackupException 類別
title: EsentNoBackupException 類別
TOCTitle: EsentNoBackupException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNoBackupException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnobackupexception(v=EXCHG.10)
ms:contentKeyID: 55102284
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNoBackupException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNoBackupException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 057e9e657c14e0ae0629618e7e7b138e053c5995
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690047"
---
# <a name="esentnobackupexception-class"></a><span data-ttu-id="2e88c-103">EsentNoBackupException 類別</span><span class="sxs-lookup"><span data-stu-id="2e88c-103">EsentNoBackupException class</span></span>

<span data-ttu-id="2e88c-104">JET_err 的基類。NoBackup 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="2e88c-104">Base class for JET_err.NoBackup exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2e88c-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="2e88c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2e88c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2e88c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2e88c-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2e88c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2e88c-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="2e88c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2e88c-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="2e88c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2e88c-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="2e88c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2e88c-111">EsentStateException （.）</span><span class="sxs-lookup"><span data-stu-id="2e88c-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="2e88c-112">EsentNoBackupException （.）</span><span class="sxs-lookup"><span data-stu-id="2e88c-112">Microsoft.Isam.Esent.Interop.EsentNoBackupException</span></span>  

<span data-ttu-id="2e88c-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2e88c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2e88c-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2e88c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2e88c-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e88c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNoBackupException _
    Inherits EsentStateException
'Usage
Dim instance As EsentNoBackupException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNoBackupException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="2e88c-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="2e88c-116">Thread safety</span></span>

<span data-ttu-id="2e88c-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2e88c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2e88c-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2e88c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e88c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e88c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2e88c-120">參考</span><span class="sxs-lookup"><span data-stu-id="2e88c-120">Reference</span></span>

[<span data-ttu-id="2e88c-121">EsentNoBackupException 成員</span><span class="sxs-lookup"><span data-stu-id="2e88c-121">EsentNoBackupException members</span></span>](./esentnobackupexception-members.md)

[<span data-ttu-id="2e88c-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2e88c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
