---
description: 深入瞭解： JET_COLUMNBASE 的 cp 屬性
title: JET_COLUMNBASE cp 屬性
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.cp(v=EXCHG.10)
ms:contentKeyID: 55103468
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8928ba3ae46283f856359b36d8f7c4c12f5891b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027556"
---
# <a name="jet_columnbasecp-property"></a><span data-ttu-id="25bbc-103">JET_COLUMNBASE cp 屬性</span><span class="sxs-lookup"><span data-stu-id="25bbc-103">JET_COLUMNBASE.cp property</span></span>

<span data-ttu-id="25bbc-104">取得資料行的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="25bbc-104">Gets code page of the column.</span></span> <span data-ttu-id="25bbc-105">只有 [Text](./jet-coltyp-enumeration.md) 和 [LongText](./jet-coltyp-enumeration.md)類型的資料行才有意義。</span><span class="sxs-lookup"><span data-stu-id="25bbc-105">This is only meaningful for columns of type [Text](./jet-coltyp-enumeration.md) and [LongText](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="25bbc-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25bbc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25bbc-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="25bbc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25bbc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="25bbc-108">Syntax</span></span>

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As JET_CP

value = instance.cp
```

``` csharp
public JET_CP cp { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="25bbc-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="25bbc-109">Property value</span></span>

<span data-ttu-id="25bbc-110">類型： [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="25bbc-110">Type: [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="25bbc-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25bbc-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25bbc-112">參考</span><span class="sxs-lookup"><span data-stu-id="25bbc-112">Reference</span></span>

[<span data-ttu-id="25bbc-113">JET_COLUMNBASE 類別</span><span class="sxs-lookup"><span data-stu-id="25bbc-113">JET_COLUMNBASE class</span></span>](./jet-columnbase-class.md)

[<span data-ttu-id="25bbc-114">JET_COLUMNBASE 成員</span><span class="sxs-lookup"><span data-stu-id="25bbc-114">JET_COLUMNBASE members</span></span>](./jet-columnbase-members.md)

[<span data-ttu-id="25bbc-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="25bbc-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
