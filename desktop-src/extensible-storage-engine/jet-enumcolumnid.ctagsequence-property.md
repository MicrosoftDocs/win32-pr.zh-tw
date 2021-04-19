---
description: 深入瞭解： JET_ENUMCOLUMNID ctagSequence 屬性
title: JET_ENUMCOLUMNID ctagSequence 屬性
TOCTitle: 'ctagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.ctagsequence(v=EXCHG.10)
ms:contentKeyID: 55107537
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_ctagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e12c8c6a102cbb20862b3cc9859f7e632ade8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972627"
---
# <a name="jet_enumcolumnidctagsequence-property"></a><span data-ttu-id="afd57-103">JET_ENUMCOLUMNID ctagSequence 屬性</span><span class="sxs-lookup"><span data-stu-id="afd57-103">JET_ENUMCOLUMNID.ctagSequence property</span></span>

<span data-ttu-id="afd57-104">取得或設定以一為基礎的索引) 所 (的資料行值計數，以列舉指定的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="afd57-104">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="afd57-105">如果 ctagSequence 為 0 (零) 則會忽略 rgtagSequence，並且會列舉指定之資料行識別碼的所有資料行值。</span><span class="sxs-lookup"><span data-stu-id="afd57-105">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="afd57-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="afd57-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="afd57-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="afd57-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="afd57-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="afd57-108">Syntax</span></span>

``` vb
'Declaration
Public Property ctagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer

value = instance.ctagSequence

instance.ctagSequence = value
```

``` csharp
public int ctagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="afd57-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="afd57-109">Property value</span></span>

<span data-ttu-id="afd57-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="afd57-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="afd57-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afd57-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="afd57-112">參考</span><span class="sxs-lookup"><span data-stu-id="afd57-112">Reference</span></span>

[<span data-ttu-id="afd57-113">JET_ENUMCOLUMNID 類別</span><span class="sxs-lookup"><span data-stu-id="afd57-113">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="afd57-114">JET_ENUMCOLUMNID 成員</span><span class="sxs-lookup"><span data-stu-id="afd57-114">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="afd57-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="afd57-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
