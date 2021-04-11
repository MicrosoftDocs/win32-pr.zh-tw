---
description: 深入瞭解： StringColumnValue。 Length 屬性
title: StringColumnValue. Length 屬性
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55104090
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Length
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed7313f66bd25653a66ebd8567a21c0ad5431ec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193978"
---
# <a name="stringcolumnvaluelength-property"></a><span data-ttu-id="a0362-103">StringColumnValue. Length 屬性</span><span class="sxs-lookup"><span data-stu-id="a0362-103">StringColumnValue.Length property</span></span>

<span data-ttu-id="a0362-104">取得資料行值的位元組長度，如果資料行是 null，則為零，否則會符合字串值的位元組長度。</span><span class="sxs-lookup"><span data-stu-id="a0362-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the byte length of the string value.</span></span> <span data-ttu-id="a0362-105">位元組長度的判斷方式是假設每個字元有兩個位元組。</span><span class="sxs-lookup"><span data-stu-id="a0362-105">The byte length is determined in assumption of two bytes per character.</span></span>

<span data-ttu-id="a0362-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a0362-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a0362-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a0362-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a0362-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0362-108">Syntax</span></span>

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As StringColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="a0362-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="a0362-109">Property value</span></span>

<span data-ttu-id="a0362-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a0362-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a0362-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0362-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a0362-112">參考</span><span class="sxs-lookup"><span data-stu-id="a0362-112">Reference</span></span>

[<span data-ttu-id="a0362-113">StringColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="a0362-113">StringColumnValue class</span></span>](./stringcolumnvalue-class.md)

[<span data-ttu-id="a0362-114">StringColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="a0362-114">StringColumnValue members</span></span>](./stringcolumnvalue-members.md)

[<span data-ttu-id="a0362-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a0362-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
