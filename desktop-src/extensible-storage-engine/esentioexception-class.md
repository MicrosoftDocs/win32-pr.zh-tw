---
description: 深入瞭解： EsentIOException 類別
title: EsentIOException 類別
TOCTitle: EsentIOException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIOException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102033
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIOException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5fbcbf38ae60ae17f74e650c403611a88d89662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992106"
---
# <a name="esentioexception-class"></a><span data-ttu-id="d79ed-103">EsentIOException 類別</span><span class="sxs-lookup"><span data-stu-id="d79ed-103">EsentIOException class</span></span>

<span data-ttu-id="d79ed-104">IO 例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="d79ed-104">Base class for IO exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d79ed-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="d79ed-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d79ed-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d79ed-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d79ed-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d79ed-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d79ed-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="d79ed-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d79ed-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="d79ed-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d79ed-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="d79ed-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="d79ed-111">EsentIOException （.）</span><span class="sxs-lookup"><span data-stu-id="d79ed-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>  
            [<span data-ttu-id="d79ed-112">EsentDeleteBackupFileFailException （.）</span><span class="sxs-lookup"><span data-stu-id="d79ed-112">Microsoft.Isam.Esent.Interop.EsentDeleteBackupFileFailException</span></span>](./esentdeletebackupfilefailexception-class.md)  
            [<span data-ttu-id="d79ed-113">EsentDiskIOException （.）</span><span class="sxs-lookup"><span data-stu-id="d79ed-113">Microsoft.Isam.Esent.Interop.EsentDiskIOException</span></span>](./esentdiskioexception-class.md)  
            [<span data-ttu-id="d79ed-114">EsentFileAccessDeniedException （.）</span><span class="sxs-lookup"><span data-stu-id="d79ed-114">Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException</span></span>](./esentfileaccessdeniedexception-class.md)  
            [<span data-ttu-id="d79ed-115">EsentLogWriteFailException （.）</span><span class="sxs-lookup"><span data-stu-id="d79ed-115">Microsoft.Isam.Esent.Interop.EsentLogWriteFailException</span></span>](./esentlogwritefailexception-class.md)  
            [<span data-ttu-id="d79ed-116">EsentMakeBackupDirectoryFailException （.）</span><span class="sxs-lookup"><span data-stu-id="d79ed-116">Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException</span></span>](./esentmakebackupdirectoryfailexception-class.md)  

<span data-ttu-id="d79ed-117">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d79ed-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d79ed-118">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d79ed-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d79ed-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="d79ed-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentIOException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentIOException
```

``` csharp
[SerializableAttribute]
public abstract class EsentIOException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="d79ed-120">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="d79ed-120">Thread safety</span></span>

<span data-ttu-id="d79ed-121">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="d79ed-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d79ed-122">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="d79ed-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d79ed-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d79ed-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d79ed-124">參考</span><span class="sxs-lookup"><span data-stu-id="d79ed-124">Reference</span></span>

[<span data-ttu-id="d79ed-125">EsentIOException 成員</span><span class="sxs-lookup"><span data-stu-id="d79ed-125">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="d79ed-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="d79ed-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
