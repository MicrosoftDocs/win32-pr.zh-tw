---
description: 深入瞭解： JET_OBJECTINFO objtyp 屬性
title: JET_OBJECTINFO objtyp 屬性
TOCTitle: 'objtyp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.objtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_objectinfo.objtyp(v=EXCHG.10)
ms:contentKeyID: 55103799
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.objtyp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.set_objtyp
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.get_objtyp
- Microsoft.Isam.Esent.Interop.JET_OBJECTINFO.objtyp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 541a9b3561c43a9b339c731a1b93302e6c8c46a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984220"
---
# <a name="jet_objectinfoobjtyp-property"></a><span data-ttu-id="e133d-103">JET_OBJECTINFO objtyp 屬性</span><span class="sxs-lookup"><span data-stu-id="e133d-103">JET_OBJECTINFO.objtyp property</span></span>

<span data-ttu-id="e133d-104">取得資料表的 JET_OBJTYP。</span><span class="sxs-lookup"><span data-stu-id="e133d-104">Gets the JET_OBJTYP of the table.</span></span> <span data-ttu-id="e133d-105">目前只會傳回資料表， (也就是 [資料表](./jet-objtyp-enumeration.md)) 。</span><span class="sxs-lookup"><span data-stu-id="e133d-105">Currently only tables will be returned (that is, [Table](./jet-objtyp-enumeration.md)).</span></span>

<span data-ttu-id="e133d-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e133d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e133d-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e133d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e133d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e133d-108">Syntax</span></span>

``` vb
'Declaration
Public Property objtyp As JET_objtyp
    Get
    Private Set
'Usage
Dim instance As JET_OBJECTINFO
Dim value As JET_objtyp

value = instance.objtyp
```

``` csharp
public JET_objtyp objtyp { get; private set; }
```

#### <a name="property-value"></a><span data-ttu-id="e133d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e133d-109">Property value</span></span>

<span data-ttu-id="e133d-110">類型： [Microsoft.Isam.Esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e133d-110">Type: [Microsoft.Isam.Esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e133d-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e133d-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e133d-112">參考</span><span class="sxs-lookup"><span data-stu-id="e133d-112">Reference</span></span>

[<span data-ttu-id="e133d-113">JET_OBJECTINFO 類別</span><span class="sxs-lookup"><span data-stu-id="e133d-113">JET_OBJECTINFO class</span></span>](./jet-objectinfo-class.md)

[<span data-ttu-id="e133d-114">JET_OBJECTINFO 成員</span><span class="sxs-lookup"><span data-stu-id="e133d-114">JET_OBJECTINFO members</span></span>](./jet-objectinfo-members.md)

[<span data-ttu-id="e133d-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e133d-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
