---
description: 深入瞭解： EsentMakeBackupDirectoryFailException 類別
title: EsentMakeBackupDirectoryFailException 類別
TOCTitle: EsentMakeBackupDirectoryFailException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmakebackupdirectoryfailexception(v=EXCHG.10)
ms:contentKeyID: 55102252
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae8fdbf432656d5b75619c00b7aa230d2e22ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943972"
---
# <a name="esentmakebackupdirectoryfailexception-class"></a><span data-ttu-id="2ae0d-103">EsentMakeBackupDirectoryFailException 類別</span><span class="sxs-lookup"><span data-stu-id="2ae0d-103">EsentMakeBackupDirectoryFailException class</span></span>

<span data-ttu-id="2ae0d-104">JET_err 的基類。MakeBackupDirectoryFail 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="2ae0d-104">Base class for JET_err.MakeBackupDirectoryFail exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2ae0d-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="2ae0d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2ae0d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2ae0d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2ae0d-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2ae0d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2ae0d-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="2ae0d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2ae0d-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="2ae0d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2ae0d-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="2ae0d-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="2ae0d-111">EsentIOException （.）</span><span class="sxs-lookup"><span data-stu-id="2ae0d-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
            <span data-ttu-id="2ae0d-112">EsentMakeBackupDirectoryFailException （.）</span><span class="sxs-lookup"><span data-stu-id="2ae0d-112">Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException</span></span>  

<span data-ttu-id="2ae0d-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2ae0d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2ae0d-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2ae0d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae0d-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ae0d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMakeBackupDirectoryFailException _
    Inherits EsentIOException
'Usage
Dim instance As EsentMakeBackupDirectoryFailException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMakeBackupDirectoryFailException : EsentIOException
```

## <a name="thread-safety"></a><span data-ttu-id="2ae0d-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="2ae0d-116">Thread safety</span></span>

<span data-ttu-id="2ae0d-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2ae0d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2ae0d-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="2ae0d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ae0d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ae0d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2ae0d-120">參考</span><span class="sxs-lookup"><span data-stu-id="2ae0d-120">Reference</span></span>

[<span data-ttu-id="2ae0d-121">EsentMakeBackupDirectoryFailException 成員</span><span class="sxs-lookup"><span data-stu-id="2ae0d-121">EsentMakeBackupDirectoryFailException members</span></span>](./esentmakebackupdirectoryfailexception-members.md)

[<span data-ttu-id="2ae0d-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2ae0d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
