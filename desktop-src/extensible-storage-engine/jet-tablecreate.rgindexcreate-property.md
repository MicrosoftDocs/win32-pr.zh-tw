---
description: 深入瞭解： JET_TABLECREATE rgindexcreate 屬性
title: JET_TABLECREATE rgindexcreate 屬性
TOCTitle: 'rgindexcreate property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgindexcreate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.rgindexcreate(v=EXCHG.10)
ms:contentKeyID: 55103970
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgindexcreate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgindexcreate
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_rgindexcreate
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_rgindexcreate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 305db4e84c8ac08396217c8278042ab40a846952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979341"
---
# <a name="jet_tablecreatergindexcreate-property"></a><span data-ttu-id="30951-103">JET_TABLECREATE rgindexcreate 屬性</span><span class="sxs-lookup"><span data-stu-id="30951-103">JET_TABLECREATE.rgindexcreate property</span></span>

<span data-ttu-id="30951-104">取得或設定要建立之索引的陣列，其類型為 [JET_INDEXCREATE](./jet-indexcreate-class.md)。</span><span class="sxs-lookup"><span data-stu-id="30951-104">Gets or sets an array of indices to create, of type [JET_INDEXCREATE](./jet-indexcreate-class.md).</span></span>

<span data-ttu-id="30951-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="30951-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="30951-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="30951-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="30951-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="30951-107">Syntax</span></span>

``` vb
'Declaration
Public Property rgindexcreate As JET_INDEXCREATE()
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As JET_INDEXCREATE()

value = instance.rgindexcreate

instance.rgindexcreate = value
```

``` csharp
public JET_INDEXCREATE[] rgindexcreate { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="30951-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="30951-108">Property value</span></span>

<span data-ttu-id="30951-109">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="30951-109">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="30951-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30951-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="30951-111">參考</span><span class="sxs-lookup"><span data-stu-id="30951-111">Reference</span></span>

[<span data-ttu-id="30951-112">JET_TABLECREATE 類別</span><span class="sxs-lookup"><span data-stu-id="30951-112">JET_TABLECREATE class</span></span>](./jet-tablecreate-class.md)

[<span data-ttu-id="30951-113">JET_TABLECREATE 成員</span><span class="sxs-lookup"><span data-stu-id="30951-113">JET_TABLECREATE members</span></span>](./jet-tablecreate-members.md)

[<span data-ttu-id="30951-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="30951-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
