---
description: 深入瞭解： EsentMissingFileToBackupException 類別
title: EsentMissingFileToBackupException 類別
TOCTitle: EsentMissingFileToBackupException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingfiletobackupexception(v=EXCHG.10)
ms:contentKeyID: 55102216
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5941140df070abb3a273378f3ec275eaf1c6fdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191990"
---
# <a name="esentmissingfiletobackupexception-class"></a><span data-ttu-id="2e265-103">EsentMissingFileToBackupException 類別</span><span class="sxs-lookup"><span data-stu-id="2e265-103">EsentMissingFileToBackupException class</span></span>

<span data-ttu-id="2e265-104">JET_err 的基類。MissingFileToBackup 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="2e265-104">Base class for JET_err.MissingFileToBackup exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2e265-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="2e265-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2e265-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2e265-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2e265-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2e265-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2e265-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="2e265-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2e265-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="2e265-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2e265-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="2e265-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="2e265-111">EsentInconsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="2e265-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="2e265-112">EsentMissingFileToBackupException （.）</span><span class="sxs-lookup"><span data-stu-id="2e265-112">Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException</span></span>  

<span data-ttu-id="2e265-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2e265-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2e265-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2e265-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2e265-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e265-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingFileToBackupException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingFileToBackupException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingFileToBackupException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="2e265-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="2e265-116">Thread safety</span></span>

<span data-ttu-id="2e265-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2e265-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2e265-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2e265-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e265-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e265-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2e265-120">參考</span><span class="sxs-lookup"><span data-stu-id="2e265-120">Reference</span></span>

[<span data-ttu-id="2e265-121">EsentMissingFileToBackupException 成員</span><span class="sxs-lookup"><span data-stu-id="2e265-121">EsentMissingFileToBackupException members</span></span>](./esentmissingfiletobackupexception-members.md)

[<span data-ttu-id="2e265-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2e265-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
