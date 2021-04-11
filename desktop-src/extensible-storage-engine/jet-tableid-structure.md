---
description: 深入瞭解： JET_TABLEID 結構
title: JET_TABLEID 結構
TOCTitle: JET_TABLEID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid(v=EXCHG.10)
ms:contentKeyID: 39516503
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLEID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a72713007ace7fb93b3f01ec8e5fc25cbe127298
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027217"
---
# <a name="jet_tableid-structure"></a><span data-ttu-id="982c7-103">JET_TABLEID 結構</span><span class="sxs-lookup"><span data-stu-id="982c7-103">JET_TABLEID structure</span></span>

<span data-ttu-id="982c7-104">JET_TABLEID 包含資料庫資料指標的控制碼，可用於呼叫 JET API。</span><span class="sxs-lookup"><span data-stu-id="982c7-104">A JET_TABLEID contains a handle to the database cursor to use for a call to the JET API.</span></span> <span data-ttu-id="982c7-105">資料指標只能搭配用來開啟該資料指標的會話使用。</span><span class="sxs-lookup"><span data-stu-id="982c7-105">A cursor can only be used with the session that was used to open that cursor.</span></span>

<span data-ttu-id="982c7-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="982c7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="982c7-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="982c7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="982c7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="982c7-108">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_TABLEID _
    Implements IEquatable(Of JET_TABLEID), IFormattable
'Usage
Dim instance As JET_TABLEID
```

``` csharp
public struct JET_TABLEID : IEquatable<JET_TABLEID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="982c7-109">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="982c7-109">Thread safety</span></span>

<span data-ttu-id="982c7-110">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="982c7-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="982c7-111">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="982c7-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="982c7-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="982c7-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="982c7-113">參考</span><span class="sxs-lookup"><span data-stu-id="982c7-113">Reference</span></span>

[<span data-ttu-id="982c7-114">JET_TABLEID 成員</span><span class="sxs-lookup"><span data-stu-id="982c7-114">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="982c7-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="982c7-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
