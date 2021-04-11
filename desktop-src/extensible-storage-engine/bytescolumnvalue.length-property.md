---
description: 深入瞭解： BytesColumnValue。 Length 屬性
title: BytesColumnValue. Length 屬性
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BytesColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55107234
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Length
- Microsoft.Isam.Esent.Interop.BytesColumnValue.get_Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f49b38cdab8d5e4a7b3554651a7dc2f97f651b59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320327"
---
# <a name="bytescolumnvaluelength-property"></a><span data-ttu-id="bd922-103">BytesColumnValue. Length 屬性</span><span class="sxs-lookup"><span data-stu-id="bd922-103">BytesColumnValue.Length property</span></span>

<span data-ttu-id="bd922-104">取得資料行值的位元組長度，如果資料行是 null，則為零，否則會符合位元組陣列的實際長度。</span><span class="sxs-lookup"><span data-stu-id="bd922-104">Gets the byte length of a column value, which is zero if column is null, otherwise matches the actual length of the byte array.</span></span>

<span data-ttu-id="bd922-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bd922-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bd922-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="bd922-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bd922-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd922-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As BytesColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="bd922-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="bd922-108">Property value</span></span>

<span data-ttu-id="bd922-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bd922-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="bd922-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd922-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bd922-111">參考</span><span class="sxs-lookup"><span data-stu-id="bd922-111">Reference</span></span>

[<span data-ttu-id="bd922-112">BytesColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="bd922-112">BytesColumnValue class</span></span>](./bytescolumnvalue-class.md)

[<span data-ttu-id="bd922-113">BytesColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="bd922-113">BytesColumnValue members</span></span>](./bytescolumnvalue-members.md)

[<span data-ttu-id="bd922-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bd922-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
