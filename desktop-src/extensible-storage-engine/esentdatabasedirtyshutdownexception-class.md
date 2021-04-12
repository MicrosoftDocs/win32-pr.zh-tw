---
description: 深入瞭解： EsentDatabaseDirtyShutdownException 類別
title: EsentDatabaseDirtyShutdownException 類別
TOCTitle: EsentDatabaseDirtyShutdownException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasedirtyshutdownexception(v=EXCHG.10)
ms:contentKeyID: 55101339
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7fcb7a3dffd5626bcf8bfc926103951747ee07e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191464"
---
# <a name="esentdatabasedirtyshutdownexception-class"></a><span data-ttu-id="50fba-103">EsentDatabaseDirtyShutdownException 類別</span><span class="sxs-lookup"><span data-stu-id="50fba-103">EsentDatabaseDirtyShutdownException class</span></span>

<span data-ttu-id="50fba-104">JET_err 的基類。DatabaseDirtyShutdown 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="50fba-104">Base class for JET_err.DatabaseDirtyShutdown exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="50fba-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="50fba-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="50fba-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="50fba-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="50fba-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="50fba-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="50fba-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="50fba-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="50fba-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="50fba-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="50fba-110">EsentDataException （.）</span><span class="sxs-lookup"><span data-stu-id="50fba-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="50fba-111">EsentInconsistentException （.）</span><span class="sxs-lookup"><span data-stu-id="50fba-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="50fba-112">EsentDatabaseDirtyShutdownException （.）</span><span class="sxs-lookup"><span data-stu-id="50fba-112">Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException</span></span>  

<span data-ttu-id="50fba-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="50fba-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="50fba-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="50fba-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="50fba-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="50fba-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseDirtyShutdownException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDatabaseDirtyShutdownException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseDirtyShutdownException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="50fba-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="50fba-116">Thread safety</span></span>

<span data-ttu-id="50fba-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="50fba-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="50fba-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="50fba-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="50fba-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50fba-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="50fba-120">參考</span><span class="sxs-lookup"><span data-stu-id="50fba-120">Reference</span></span>

[<span data-ttu-id="50fba-121">EsentDatabaseDirtyShutdownException 成員</span><span class="sxs-lookup"><span data-stu-id="50fba-121">EsentDatabaseDirtyShutdownException members</span></span>](./esentdatabasedirtyshutdownexception-members.md)

[<span data-ttu-id="50fba-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="50fba-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
