---
description: 深入瞭解： JET_COLUMNCREATE 的 cp 屬性
title: JET_COLUMNCREATE cp 屬性
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.cp(v=EXCHG.10)
ms:contentKeyID: 55103400
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.get_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b39c47402a70778543f203777b6e2d0d3fc9ac29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984987"
---
# <a name="jet_columncreatecp-property"></a><span data-ttu-id="04320-103">JET_COLUMNCREATE cp 屬性</span><span class="sxs-lookup"><span data-stu-id="04320-103">JET_COLUMNCREATE.cp property</span></span>

<span data-ttu-id="04320-104">取得或設定資料行的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="04320-104">Gets or sets code page of the column.</span></span> <span data-ttu-id="04320-105">只有 [Text](./jet-coltyp-enumeration.md) 和 [LongText](./jet-coltyp-enumeration.md)類型的資料行才有意義。</span><span class="sxs-lookup"><span data-stu-id="04320-105">This is only meaningful for columns of type [Text](./jet-coltyp-enumeration.md) and [LongText](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="04320-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="04320-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="04320-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="04320-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="04320-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="04320-108">Syntax</span></span>

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Set
'Usage
Dim instance As JET_COLUMNCREATE
Dim value As JET_CP

value = instance.cp

instance.cp = value
```

``` csharp
public JET_CP cp { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="04320-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="04320-109">Property value</span></span>

<span data-ttu-id="04320-110">類型： [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="04320-110">Type: [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="04320-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04320-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="04320-112">參考</span><span class="sxs-lookup"><span data-stu-id="04320-112">Reference</span></span>

[<span data-ttu-id="04320-113">JET_COLUMNCREATE 類別</span><span class="sxs-lookup"><span data-stu-id="04320-113">JET_COLUMNCREATE class</span></span>](./jet-columncreate-class.md)

[<span data-ttu-id="04320-114">JET_COLUMNCREATE 成員</span><span class="sxs-lookup"><span data-stu-id="04320-114">JET_COLUMNCREATE members</span></span>](./jet-columncreate-members.md)

[<span data-ttu-id="04320-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="04320-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
