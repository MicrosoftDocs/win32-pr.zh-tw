---
description: 深入瞭解： JET_RETRIEVECOLUMN columnidNextTagged 屬性
title: JET_RETRIEVECOLUMN columnidNextTagged 屬性
TOCTitle: 'columnidNextTagged property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.columnidNextTagged
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.columnidnexttagged(v=EXCHG.10)
ms:contentKeyID: 55103812
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.columnidNextTagged
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_columnidNextTagged
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_columnidNextTagged
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b900d03e43f0d7b172b09e0928110222e909df3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113716"
---
# <a name="jet_retrievecolumncolumnidnexttagged-property"></a><span data-ttu-id="7be53-103">JET_RETRIEVECOLUMN columnidNextTagged 屬性</span><span class="sxs-lookup"><span data-stu-id="7be53-103">JET_RETRIEVECOLUMN.columnidNextTagged property</span></span>

<span data-ttu-id="7be53-104">藉由將0傳遞為 columnid，取得已標記、多重值或稀疏資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="7be53-104">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span>

<span data-ttu-id="7be53-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7be53-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7be53-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7be53-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7be53-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7be53-107">Syntax</span></span>

``` vb
'Declaration
Public Property columnidNextTagged As JET_COLUMNID
    Get
    Private Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As JET_COLUMNID

value = instance.columnidNextTagged
```

``` csharp
public JET_COLUMNID columnidNextTagged { get; private set; }
```

#### <a name="property-value"></a><span data-ttu-id="7be53-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="7be53-108">Property value</span></span>

<span data-ttu-id="7be53-109">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7be53-109">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7be53-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7be53-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7be53-111">參考</span><span class="sxs-lookup"><span data-stu-id="7be53-111">Reference</span></span>

[<span data-ttu-id="7be53-112">JET_RETRIEVECOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="7be53-112">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="7be53-113">JET_RETRIEVECOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="7be53-113">JET_RETRIEVECOLUMN members</span></span>](./jet-retrievecolumn-members.md)

[<span data-ttu-id="7be53-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7be53-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
