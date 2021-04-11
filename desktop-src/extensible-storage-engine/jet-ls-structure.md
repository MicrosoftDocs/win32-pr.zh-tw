---
description: 深入瞭解： JET_LS 結構
title: JET_LS 結構
TOCTitle: JET_LS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_LS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls(v=EXCHG.10)
ms:contentKeyID: 39510760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d32c1a6815cfa7552fed0d8f1a01376ae0eacaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193813"
---
# <a name="jet_ls-structure"></a><span data-ttu-id="c5792-103">JET_LS 結構</span><span class="sxs-lookup"><span data-stu-id="c5792-103">JET_LS structure</span></span>

<span data-ttu-id="c5792-104">ESENT 控制碼的本機儲存體。</span><span class="sxs-lookup"><span data-stu-id="c5792-104">Local storage for an ESENT handle.</span></span> <span data-ttu-id="c5792-105">由 [JetGetLS (JET_SESID、JET_TABLEID、JET_LS、LsGrbit) ](./api.jetgetls-method.md) 和 [JetSetLS (JET_SESID、JET_TABLEID、JET_LS、LsGrbit) ](./api.jetsetls-method.md)使用。</span><span class="sxs-lookup"><span data-stu-id="c5792-105">Used by [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md) and [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span></span>

<span data-ttu-id="c5792-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c5792-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c5792-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c5792-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c5792-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5792-108">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_LS _
    Implements IEquatable(Of JET_LS), IFormattable
'Usage
Dim instance As JET_LS
```

``` csharp
public struct JET_LS : IEquatable<JET_LS>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="c5792-109">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="c5792-109">Thread safety</span></span>

<span data-ttu-id="c5792-110">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c5792-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c5792-111">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c5792-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5792-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5792-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c5792-113">參考</span><span class="sxs-lookup"><span data-stu-id="c5792-113">Reference</span></span>

[<span data-ttu-id="c5792-114">JET_LS 成員</span><span class="sxs-lookup"><span data-stu-id="c5792-114">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="c5792-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c5792-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
