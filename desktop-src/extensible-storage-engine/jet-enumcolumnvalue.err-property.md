---
description: 深入瞭解： JET_ENUMCOLUMNVALUE err 屬性
title: JET_ENUMCOLUMNVALUE err 屬性
TOCTitle: 'err property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue.err(v=EXCHG.10)
ms:contentKeyID: 55103626
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.get_err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.set_err
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f797d82ad09b75d961be24f2382b0895880427f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194299"
---
# <a name="jet_enumcolumnvalueerr-property"></a><span data-ttu-id="dd58b-103">JET_ENUMCOLUMNVALUE err 屬性</span><span class="sxs-lookup"><span data-stu-id="dd58b-103">JET_ENUMCOLUMNVALUE.err property</span></span>

<span data-ttu-id="dd58b-104">取得資料行值的列舉所產生的資料行狀態碼。</span><span class="sxs-lookup"><span data-stu-id="dd58b-104">Gets the column status code resulting from the enumeration of the column value.</span></span>

<span data-ttu-id="dd58b-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dd58b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dd58b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="dd58b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dd58b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd58b-107">Syntax</span></span>

``` vb
'Declaration
Public Property err As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMNVALUE
Dim value As JET_wrn

value = instance.err
```

``` csharp
public JET_wrn err { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="dd58b-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="dd58b-108">Property value</span></span>

<span data-ttu-id="dd58b-109">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="dd58b-109">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="dd58b-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd58b-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dd58b-111">參考</span><span class="sxs-lookup"><span data-stu-id="dd58b-111">Reference</span></span>

[<span data-ttu-id="dd58b-112">JET_ENUMCOLUMNVALUE 類別</span><span class="sxs-lookup"><span data-stu-id="dd58b-112">JET_ENUMCOLUMNVALUE class</span></span>](./jet-enumcolumnvalue-class.md)

[<span data-ttu-id="dd58b-113">JET_ENUMCOLUMNVALUE 成員</span><span class="sxs-lookup"><span data-stu-id="dd58b-113">JET_ENUMCOLUMNVALUE members</span></span>](./jet-enumcolumnvalue-members.md)

[<span data-ttu-id="dd58b-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="dd58b-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="dd58b-115">ColumnNull</span><span class="sxs-lookup"><span data-stu-id="dd58b-115">ColumnNull</span></span>](./jet-wrn-enumeration.md)

[<span data-ttu-id="dd58b-116">ColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="dd58b-116">ColumnSkipped</span></span>](./jet-wrn-enumeration.md)

[<span data-ttu-id="dd58b-117">ColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="dd58b-117">ColumnTruncated</span></span>](./jet-wrn-enumeration.md)
