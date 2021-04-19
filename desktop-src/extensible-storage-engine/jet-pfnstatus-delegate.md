---
description: 深入瞭解： JET_PFNSTATUS 委派
title: JET_PFNSTATUS 委派
TOCTitle: JET_PFNSTATUS delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnstatus(v=EXCHG.10)
ms:contentKeyID: 39515654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.BeginInvoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16cc5807d858f964f995b449a0a0eee78659aefd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984634"
---
# <a name="jet_pfnstatus-delegate"></a><span data-ttu-id="a20ea-103">JET_PFNSTATUS 委派</span><span class="sxs-lookup"><span data-stu-id="a20ea-103">JET_PFNSTATUS delegate</span></span>

<span data-ttu-id="a20ea-104">接收長時間執行之作業進度的相關資訊，例如磁碟重組、備份或還原作業。</span><span class="sxs-lookup"><span data-stu-id="a20ea-104">Receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="a20ea-105">在這類作業期間，資料庫引擎會呼叫此回呼函數，以提供作業進度的更新。</span><span class="sxs-lookup"><span data-stu-id="a20ea-105">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

<span data-ttu-id="a20ea-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a20ea-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a20ea-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a20ea-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a20ea-108">語法</span><span class="sxs-lookup"><span data-stu-id="a20ea-108">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_PFNSTATUS ( _
    sesid As JET_SESID, _
    snp As JET_SNP, _
    snt As JET_SNT, _
    data As Object _
) As JET_err
'Usage
Dim instance As New JET_PFNSTATUS(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNSTATUS(
    JET_SESID sesid,
    JET_SNP snp,
    JET_SNT snt,
    Object data
)
```

#### <a name="parameters"></a><span data-ttu-id="a20ea-109">參數</span><span class="sxs-lookup"><span data-stu-id="a20ea-109">Parameters</span></span>

  - <span data-ttu-id="a20ea-110">sesid</span><span class="sxs-lookup"><span data-stu-id="a20ea-110">sesid</span></span>  
    <span data-ttu-id="a20ea-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a20ea-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a20ea-112">呼叫長時間執行作業所使用的會話。</span><span class="sxs-lookup"><span data-stu-id="a20ea-112">The session with which the long running operation was called.</span></span>

<!-- end list -->

  - <span data-ttu-id="a20ea-113">Snp</span><span class="sxs-lookup"><span data-stu-id="a20ea-113">snp</span></span>  
    <span data-ttu-id="a20ea-114">類型： [Microsoft.Isam.Esent.Interop.JET_SNP](./jet-snp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a20ea-114">Type: [Microsoft.Isam.Esent.Interop.JET_SNP](./jet-snp-enumeration.md)</span></span>  
    
    <span data-ttu-id="a20ea-115">作業的類型。</span><span class="sxs-lookup"><span data-stu-id="a20ea-115">The type of operation.</span></span>

<!-- end list -->

  - <span data-ttu-id="a20ea-116">snt</span><span class="sxs-lookup"><span data-stu-id="a20ea-116">snt</span></span>  
    <span data-ttu-id="a20ea-117">類型： [Microsoft.Isam.Esent.Interop.JET_SNT](./jet-snt-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a20ea-117">Type: [Microsoft.Isam.Esent.Interop.JET_SNT](./jet-snt-enumeration.md)</span></span>  
    
    <span data-ttu-id="a20ea-118">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="a20ea-118">The status of the operation.</span></span>

<!-- end list -->

  - <span data-ttu-id="a20ea-119">data</span><span class="sxs-lookup"><span data-stu-id="a20ea-119">data</span></span>  
    <span data-ttu-id="a20ea-120">類型： [system.object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="a20ea-120">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="a20ea-121">選用資料。</span><span class="sxs-lookup"><span data-stu-id="a20ea-121">Optional data.</span></span> <span data-ttu-id="a20ea-122">可能是 [JET_SNPROG](./jet-snprog-class.md)。</span><span class="sxs-lookup"><span data-stu-id="a20ea-122">May be a [JET_SNPROG](./jet-snprog-class.md).</span></span>

#### <a name="return-value"></a><span data-ttu-id="a20ea-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="a20ea-123">Return value</span></span>

<span data-ttu-id="a20ea-124">類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a20ea-124">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a20ea-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a20ea-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a20ea-126">參考</span><span class="sxs-lookup"><span data-stu-id="a20ea-126">Reference</span></span>

[<span data-ttu-id="a20ea-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a20ea-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
