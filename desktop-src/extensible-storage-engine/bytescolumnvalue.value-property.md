---
description: 深入瞭解： BytesColumnValue。 Value 屬性
title: BytesColumnValue。 Value 屬性
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.value(v=EXCHG.10)
ms:contentKeyID: 55107249
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.set_Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.get_Value
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0804a7a05640336be77e5f446ad99227db592f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996875"
---
# <a name="bytescolumnvaluevalue-property"></a><span data-ttu-id="b450a-103">BytesColumnValue。 Value 屬性</span><span class="sxs-lookup"><span data-stu-id="b450a-103">BytesColumnValue.Value property</span></span>

<span data-ttu-id="b450a-104">取得或設定資料行的值。</span><span class="sxs-lookup"><span data-stu-id="b450a-104">Gets or sets the value of the column.</span></span> <span data-ttu-id="b450a-105">使用[SetColumns (JET_SESID、JET_TABLEID \[ \]) ](./api.setcolumns-method.md)來更新具有資料行值的記錄。</span><span class="sxs-lookup"><span data-stu-id="b450a-105">Use [SetColumns(JET_SESID, JET_TABLEID, \[\])](./api.setcolumns-method.md) to update a record with the column value.</span></span>

<span data-ttu-id="b450a-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b450a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b450a-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b450a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b450a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b450a-108">Syntax</span></span>

``` vb
'Declaration
Public Property Value As Byte()
    Get
    Set
'Usage
Dim instance As BytesColumnValue
Dim value As Byte()

value = instance.Value

instance.Value = value
```

``` csharp
public byte[] Value { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="b450a-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="b450a-109">Property value</span></span>

<span data-ttu-id="b450a-110">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="b450a-110">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="b450a-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b450a-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b450a-112">參考</span><span class="sxs-lookup"><span data-stu-id="b450a-112">Reference</span></span>

[<span data-ttu-id="b450a-113">BytesColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="b450a-113">BytesColumnValue class</span></span>](./bytescolumnvalue-class.md)

[<span data-ttu-id="b450a-114">BytesColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="b450a-114">BytesColumnValue members</span></span>](./bytescolumnvalue-members.md)

[<span data-ttu-id="b450a-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b450a-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
