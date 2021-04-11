---
description: 深入瞭解： JET_ENUMCOLUMNID columnid 屬性
title: JET_ENUMCOLUMNID columnid 屬性
TOCTitle: 'columnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.columnid(v=EXCHG.10)
ms:contentKeyID: 55103623
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_columnid
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.columnid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1c456a4eb208ba8c9f2ac39ea0b4dad410ee270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112100"
---
# <a name="jet_enumcolumnidcolumnid-property"></a><span data-ttu-id="fb602-103">JET_ENUMCOLUMNID columnid 屬性</span><span class="sxs-lookup"><span data-stu-id="fb602-103">JET_ENUMCOLUMNID.columnid property</span></span>

<span data-ttu-id="fb602-104">取得或設定要列舉的 columnid 識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb602-104">Gets or sets the columnid ID to enumerate.</span></span>

<span data-ttu-id="fb602-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fb602-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fb602-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fb602-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fb602-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb602-107">Syntax</span></span>

``` vb
'Declaration
Public Property columnid As JET_COLUMNID
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As JET_COLUMNID

value = instance.columnid

instance.columnid = value
```

``` csharp
public JET_COLUMNID columnid { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="fb602-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="fb602-108">Property value</span></span>

<span data-ttu-id="fb602-109">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fb602-109">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="remarks"></a><span data-ttu-id="fb602-110">備註</span><span class="sxs-lookup"><span data-stu-id="fb602-110">Remarks</span></span>

<span data-ttu-id="fb602-111">如果資料行識別碼為 0 (零) 則會略過此資料行的列舉，而 JET_ENUMCOLUMN 結構輸出陣列中的對應位置將會產生 JET_wrnColumnSkipped 的資料行狀態。</span><span class="sxs-lookup"><span data-stu-id="fb602-111">If the column ID is 0 (zero) then the enumeration of this column is skipped and a corresponding slot in the output array of JET_ENUMCOLUMN structures will be generated with a column state of JET_wrnColumnSkipped.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb602-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb602-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fb602-113">參考</span><span class="sxs-lookup"><span data-stu-id="fb602-113">Reference</span></span>

[<span data-ttu-id="fb602-114">JET_ENUMCOLUMNID 類別</span><span class="sxs-lookup"><span data-stu-id="fb602-114">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="fb602-115">JET_ENUMCOLUMNID 成員</span><span class="sxs-lookup"><span data-stu-id="fb602-115">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="fb602-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="fb602-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
