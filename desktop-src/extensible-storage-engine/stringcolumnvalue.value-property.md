---
description: 深入瞭解： StringColumnValue。 Value 屬性
title: StringColumnValue。 Value 屬性
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Value
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.value(v=EXCHG.10)
ms:contentKeyID: 55104098
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Value
- Microsoft.Isam.Esent.Interop.StringColumnValue.set_Value
- Microsoft.Isam.Esent.Interop.StringColumnValue.Value
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b1f5dc65f41e1714858c75bed2c22e23680b60cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997964"
---
# <a name="stringcolumnvaluevalue-property"></a><span data-ttu-id="ccd16-103">StringColumnValue。 Value 屬性</span><span class="sxs-lookup"><span data-stu-id="ccd16-103">StringColumnValue.Value property</span></span>

<span data-ttu-id="ccd16-104">取得或設定資料行的值。</span><span class="sxs-lookup"><span data-stu-id="ccd16-104">Gets or sets the value of the column.</span></span> <span data-ttu-id="ccd16-105">使用[SetColumns (JET_SESID、JET_TABLEID \[ \]) ](./api.setcolumns-method.md)來更新具有資料行值的記錄。</span><span class="sxs-lookup"><span data-stu-id="ccd16-105">Use [SetColumns(JET_SESID, JET_TABLEID, \[\])](./api.setcolumns-method.md) to update a record with the column value.</span></span>

<span data-ttu-id="ccd16-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ccd16-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ccd16-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ccd16-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd16-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccd16-108">Syntax</span></span>

``` vb
'Declaration
Public Property Value As String
    Get
    Set
'Usage
Dim instance As StringColumnValue
Dim value As String

value = instance.Value

instance.Value = value
```

``` csharp
public string Value { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="ccd16-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="ccd16-109">Property value</span></span>

<span data-ttu-id="ccd16-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ccd16-110">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="ccd16-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccd16-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ccd16-112">參考</span><span class="sxs-lookup"><span data-stu-id="ccd16-112">Reference</span></span>

[<span data-ttu-id="ccd16-113">StringColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="ccd16-113">StringColumnValue class</span></span>](./stringcolumnvalue-class.md)

[<span data-ttu-id="ccd16-114">StringColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="ccd16-114">StringColumnValue members</span></span>](./stringcolumnvalue-members.md)

[<span data-ttu-id="ccd16-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ccd16-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
