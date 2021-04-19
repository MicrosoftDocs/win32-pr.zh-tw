---
description: 深入瞭解： JET_RETINFO ibLongValue 屬性
title: JET_RETINFO ibLongValue 屬性
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103801
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ibLongValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39b2ed312f7db54ff799ce2aa52554349d020dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972448"
---
# <a name="jet_retinfoiblongvalue-property"></a><span data-ttu-id="17aac-103">JET_RETINFO ibLongValue 屬性</span><span class="sxs-lookup"><span data-stu-id="17aac-103">JET_RETINFO.ibLongValue property</span></span>

<span data-ttu-id="17aac-104">取得或設定要從 [LongBinary](./jet-coltyp-enumeration.md)或 [LongText](./jet-coltyp-enumeration.md)類型的資料行中抓取之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="17aac-104">Gets or sets the offset to the first byte to be retrieved from a column of type [LongBinary](./jet-coltyp-enumeration.md), or [LongText](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="17aac-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="17aac-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="17aac-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="17aac-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="17aac-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="17aac-107">Syntax</span></span>

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
Dim value As Integer

value = instance.ibLongValue

instance.ibLongValue = value
```

``` csharp
public int ibLongValue { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="17aac-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="17aac-108">Property value</span></span>

<span data-ttu-id="17aac-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="17aac-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="17aac-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17aac-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="17aac-111">參考</span><span class="sxs-lookup"><span data-stu-id="17aac-111">Reference</span></span>

[<span data-ttu-id="17aac-112">JET_RETINFO 類別</span><span class="sxs-lookup"><span data-stu-id="17aac-112">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="17aac-113">JET_RETINFO 成員</span><span class="sxs-lookup"><span data-stu-id="17aac-113">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="17aac-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="17aac-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
