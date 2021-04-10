---
description: 深入瞭解： JET_SETCOLUMN ibLongValue 屬性
title: JET_SETCOLUMN ibLongValue 屬性
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103931
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_ibLongValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d98f1b49f5e4815f2ffaeb5d796c6139ad582e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689932"
---
# <a name="jet_setcolumniblongvalue-property"></a><span data-ttu-id="3f731-103">JET_SETCOLUMN ibLongValue 屬性</span><span class="sxs-lookup"><span data-stu-id="3f731-103">JET_SETCOLUMN.ibLongValue property</span></span>

<span data-ttu-id="3f731-104">取得或設定要在 [LongBinary](./jet-coltyp-enumeration.md) 或 [LongText](./jet-coltyp-enumeration.md)類型的資料行中設定之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="3f731-104">Gets or sets offset to the first byte to be set in a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="3f731-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3f731-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3f731-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3f731-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3f731-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f731-107">Syntax</span></span>

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As Integer

value = instance.ibLongValue

instance.ibLongValue = value
```

``` csharp
public int ibLongValue { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="3f731-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="3f731-108">Property value</span></span>

<span data-ttu-id="3f731-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3f731-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="3f731-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f731-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3f731-111">參考</span><span class="sxs-lookup"><span data-stu-id="3f731-111">Reference</span></span>

[<span data-ttu-id="3f731-112">JET_SETCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="3f731-112">JET_SETCOLUMN class</span></span>](./jet-setcolumn-class.md)

[<span data-ttu-id="3f731-113">JET_SETCOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="3f731-113">JET_SETCOLUMN members</span></span>](./jet-setcolumn-members.md)

[<span data-ttu-id="3f731-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3f731-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
