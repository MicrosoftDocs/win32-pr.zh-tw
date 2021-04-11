---
description: 深入瞭解： JET_RETRIEVECOLUMN ibLongValue 屬性
title: JET_RETRIEVECOLUMN ibLongValue 屬性
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103819
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.ibLongValue
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_ibLongValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbe403553acb3305b538d6f35f837ca7feab97db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113712"
---
# <a name="jet_retrievecolumniblongvalue-property"></a><span data-ttu-id="5210b-103">JET_RETRIEVECOLUMN ibLongValue 屬性</span><span class="sxs-lookup"><span data-stu-id="5210b-103">JET_RETRIEVECOLUMN.ibLongValue property</span></span>

<span data-ttu-id="5210b-104">取得或設定要從 [LongBinary](./jet-coltyp-enumeration.md) 或 [LongText](./jet-coltyp-enumeration.md)類型的資料行中抓取之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="5210b-104">Gets or sets the offset to the first byte to be retrieved from a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="5210b-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5210b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5210b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5210b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5210b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5210b-107">Syntax</span></span>

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Integer

value = instance.ibLongValue

instance.ibLongValue = value
```

``` csharp
public int ibLongValue { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="5210b-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="5210b-108">Property value</span></span>

<span data-ttu-id="5210b-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5210b-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5210b-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5210b-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5210b-111">參考</span><span class="sxs-lookup"><span data-stu-id="5210b-111">Reference</span></span>

[<span data-ttu-id="5210b-112">JET_RETRIEVECOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="5210b-112">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="5210b-113">JET_RETRIEVECOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="5210b-113">JET_RETRIEVECOLUMN members</span></span>](./jet-retrievecolumn-members.md)

[<span data-ttu-id="5210b-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5210b-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
