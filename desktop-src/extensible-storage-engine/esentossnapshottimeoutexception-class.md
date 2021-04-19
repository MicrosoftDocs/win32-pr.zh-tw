---
description: 深入瞭解： EsentOSSnapshotTimeOutException 類別
title: EsentOSSnapshotTimeOutException 類別
TOCTitle: EsentOSSnapshotTimeOutException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentossnapshottimeoutexception(v=EXCHG.10)
ms:contentKeyID: 55102393
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ee86c466c827211072f8345f05af2c1df5bf721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988752"
---
# <a name="esentossnapshottimeoutexception-class"></a><span data-ttu-id="baec5-103">EsentOSSnapshotTimeOutException 類別</span><span class="sxs-lookup"><span data-stu-id="baec5-103">EsentOSSnapshotTimeOutException class</span></span>

<span data-ttu-id="baec5-104">JET_err 的基類。OSSnapshotTimeOut 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="baec5-104">Base class for JET_err.OSSnapshotTimeOut exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="baec5-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="baec5-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="baec5-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="baec5-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="baec5-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="baec5-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="baec5-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="baec5-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="baec5-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="baec5-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="baec5-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="baec5-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="baec5-111">EsentOSSnapshotTimeOutException （.）</span><span class="sxs-lookup"><span data-stu-id="baec5-111">Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException</span></span>  

<span data-ttu-id="baec5-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="baec5-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="baec5-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="baec5-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="baec5-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="baec5-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOSSnapshotTimeOutException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentOSSnapshotTimeOutException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOSSnapshotTimeOutException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="baec5-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="baec5-115">Thread safety</span></span>

<span data-ttu-id="baec5-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="baec5-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="baec5-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="baec5-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="baec5-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="baec5-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="baec5-119">參考</span><span class="sxs-lookup"><span data-stu-id="baec5-119">Reference</span></span>

[<span data-ttu-id="baec5-120">EsentOSSnapshotTimeOutException 成員</span><span class="sxs-lookup"><span data-stu-id="baec5-120">EsentOSSnapshotTimeOutException members</span></span>](./esentossnapshottimeoutexception-members.md)

[<span data-ttu-id="baec5-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="baec5-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
