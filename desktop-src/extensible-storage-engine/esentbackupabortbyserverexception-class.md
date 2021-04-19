---
description: 深入瞭解： EsentBackupAbortByServerException 類別
title: EsentBackupAbortByServerException 類別
TOCTitle: EsentBackupAbortByServerException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupabortbyserverexception(v=EXCHG.10)
ms:contentKeyID: 55101070
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be5f1fca4cfdbfe880288b66d3d6c8a439666384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980623"
---
# <a name="esentbackupabortbyserverexception-class"></a><span data-ttu-id="7d8c8-103">EsentBackupAbortByServerException 類別</span><span class="sxs-lookup"><span data-stu-id="7d8c8-103">EsentBackupAbortByServerException class</span></span>

<span data-ttu-id="7d8c8-104">JET_err 的基類。BackupAbortByServer 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7d8c8-104">Base class for JET_err.BackupAbortByServer exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7d8c8-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="7d8c8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7d8c8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7d8c8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7d8c8-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="7d8c8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7d8c8-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="7d8c8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7d8c8-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="7d8c8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7d8c8-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="7d8c8-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="7d8c8-111">EsentBackupAbortByServerException （.）</span><span class="sxs-lookup"><span data-stu-id="7d8c8-111">Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException</span></span>  

<span data-ttu-id="7d8c8-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d8c8-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7d8c8-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7d8c8-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d8c8-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d8c8-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupAbortByServerException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentBackupAbortByServerException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupAbortByServerException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="7d8c8-115">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="7d8c8-115">Thread safety</span></span>

<span data-ttu-id="7d8c8-116">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="7d8c8-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7d8c8-117">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="7d8c8-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d8c8-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d8c8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d8c8-119">參考</span><span class="sxs-lookup"><span data-stu-id="7d8c8-119">Reference</span></span>

[<span data-ttu-id="7d8c8-120">EsentBackupAbortByServerException 成員</span><span class="sxs-lookup"><span data-stu-id="7d8c8-120">EsentBackupAbortByServerException members</span></span>](./esentbackupabortbyserverexception-members.md)

[<span data-ttu-id="7d8c8-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7d8c8-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
