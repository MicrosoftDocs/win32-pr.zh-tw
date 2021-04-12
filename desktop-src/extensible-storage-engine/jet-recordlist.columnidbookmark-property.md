---
description: 深入瞭解： JET_RECORDLIST columnidBookmark 屬性
title: JET_RECORDLIST columnidBookmark 屬性
TOCTitle: 'columnidBookmark property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recordlist.columnidbookmark(v=EXCHG.10)
ms:contentKeyID: 55103827
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.get_columnidBookmark
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.set_columnidBookmark
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2069a274c5d89b3198113985a11a5d8af26fd1a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194882"
---
# <a name="jet_recordlistcolumnidbookmark-property"></a><span data-ttu-id="7e61d-103">JET_RECORDLIST columnidBookmark 屬性</span><span class="sxs-lookup"><span data-stu-id="7e61d-103">JET_RECORDLIST.columnidBookmark property</span></span>

<span data-ttu-id="7e61d-104">取得臨時表中的資料行 columnid，此資料行會儲存記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="7e61d-104">Gets the columnid of the column in the temporary table which stores the bookmark of the record.</span></span> <span data-ttu-id="7e61d-105">資料行的類型為 JET_coltyp。文本。</span><span class="sxs-lookup"><span data-stu-id="7e61d-105">The column is of type JET_coltyp.Text.</span></span>

<span data-ttu-id="7e61d-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e61d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e61d-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7e61d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e61d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e61d-108">Syntax</span></span>

``` vb
'Declaration
Public Property columnidBookmark As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_RECORDLIST
Dim value As JET_COLUMNID

value = instance.columnidBookmark
```

``` csharp
public JET_COLUMNID columnidBookmark { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="7e61d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="7e61d-109">Property value</span></span>

<span data-ttu-id="7e61d-110">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e61d-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e61d-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e61d-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e61d-112">參考</span><span class="sxs-lookup"><span data-stu-id="7e61d-112">Reference</span></span>

[<span data-ttu-id="7e61d-113">JET_RECORDLIST 類別</span><span class="sxs-lookup"><span data-stu-id="7e61d-113">JET_RECORDLIST class</span></span>](./jet-recordlist-class.md)

[<span data-ttu-id="7e61d-114">JET_RECORDLIST 成員</span><span class="sxs-lookup"><span data-stu-id="7e61d-114">JET_RECORDLIST members</span></span>](./jet-recordlist-members.md)

[<span data-ttu-id="7e61d-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7e61d-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
