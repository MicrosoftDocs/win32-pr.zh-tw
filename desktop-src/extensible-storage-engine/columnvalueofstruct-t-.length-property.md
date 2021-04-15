---
description: 深入瞭解： ColumnValueOfStruct <T> 。Length 屬性
title: ColumnValueOfStruct (T) 。Length 屬性
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Length
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334225(v=EXCHG.10)
ms:contentKeyID: 55101009
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.get_Length
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ae3c67ba3dfbdcf8c72e04e75185c835c290e21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512364"
---
# <a name="columnvalueofstructtlength-property"></a><span data-ttu-id="28835-103">ColumnValueOfStruct \<T\> 。Length 屬性</span><span class="sxs-lookup"><span data-stu-id="28835-103">ColumnValueOfStruct\<T\>.Length property</span></span>

<span data-ttu-id="28835-104">取得資料行值的位元組長度，如果資料行是 null，則為零，否則會符合此固定大小資料行的大小。</span><span class="sxs-lookup"><span data-stu-id="28835-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the Size for this fixed-size column.</span></span>

<span data-ttu-id="28835-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="28835-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="28835-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="28835-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="28835-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="28835-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValueOfStruct
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="28835-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="28835-108">Property value</span></span>

<span data-ttu-id="28835-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="28835-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="28835-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28835-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="28835-111">參考</span><span class="sxs-lookup"><span data-stu-id="28835-111">Reference</span></span>

[<span data-ttu-id="28835-112">ColumnValueOfStruct \<T\> 類別</span><span class="sxs-lookup"><span data-stu-id="28835-112">ColumnValueOfStruct\<T\> class</span></span>](./columnvalueofstruct-t-class.md)

[<span data-ttu-id="28835-113">ColumnValueOfStruct \<T\> 成員</span><span class="sxs-lookup"><span data-stu-id="28835-113">ColumnValueOfStruct\<T\> members</span></span>](./columnvalueofstruct-t-members.md)

[<span data-ttu-id="28835-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="28835-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
