---
description: 深入瞭解： JET_COLUMNDEF 的 cp 屬性
title: JET_COLUMNDEF cp 屬性
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.cp(v=EXCHG.10)
ms:contentKeyID: 55103411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.get_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df383b212105a4b871f0c44d341d6113abf94d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114433"
---
# <a name="jet_columndefcp-property"></a><span data-ttu-id="19400-103">JET_COLUMNDEF cp 屬性</span><span class="sxs-lookup"><span data-stu-id="19400-103">JET_COLUMNDEF.cp property</span></span>

<span data-ttu-id="19400-104">取得或設定資料行的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="19400-104">Gets or sets code page of the column.</span></span> <span data-ttu-id="19400-105">只有 [Text](./jet-coltyp-enumeration.md) 和 [LongText](./jet-coltyp-enumeration.md)類型的資料行才有意義。</span><span class="sxs-lookup"><span data-stu-id="19400-105">This is only meaningful for columns of type [Text](./jet-coltyp-enumeration.md) and [LongText](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="19400-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="19400-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="19400-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="19400-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="19400-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="19400-108">Syntax</span></span>

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Set
'Usage
Dim instance As JET_COLUMNDEF
Dim value As JET_CP

value = instance.cp

instance.cp = value
```

``` csharp
public JET_CP cp { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="19400-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="19400-109">Property value</span></span>

<span data-ttu-id="19400-110">類型： [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="19400-110">Type: [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="19400-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19400-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="19400-112">參考</span><span class="sxs-lookup"><span data-stu-id="19400-112">Reference</span></span>

[<span data-ttu-id="19400-113">JET_COLUMNDEF 類別</span><span class="sxs-lookup"><span data-stu-id="19400-113">JET_COLUMNDEF class</span></span>](./jet-columndef-class.md)

[<span data-ttu-id="19400-114">JET_COLUMNDEF 成員</span><span class="sxs-lookup"><span data-stu-id="19400-114">JET_COLUMNDEF members</span></span>](./jet-columndef-members.md)

[<span data-ttu-id="19400-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="19400-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
