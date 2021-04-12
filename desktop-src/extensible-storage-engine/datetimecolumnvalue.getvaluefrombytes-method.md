---
description: 深入瞭解： DateTimeColumnValue. GetValueFromBytes 方法
title: DateTimeColumnValue. GetValueFromBytes 方法
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.DateTimeColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.datetimecolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55101200
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b30acf865a31c7dcaccffab0d156eacbb0e59ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695816"
---
# <a name="datetimecolumnvaluegetvaluefrombytes-method"></a><span data-ttu-id="6f061-103">DateTimeColumnValue. GetValueFromBytes 方法</span><span class="sxs-lookup"><span data-stu-id="6f061-103">DateTimeColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="6f061-104">從 ESENT 取出資料，將資料解碼，並設定 ColumnValue 物件中的值。</span><span class="sxs-lookup"><span data-stu-id="6f061-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="6f061-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6f061-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6f061-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6f061-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6f061-107">語法</span><span class="sxs-lookup"><span data-stu-id="6f061-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a><span data-ttu-id="6f061-108">參數</span><span class="sxs-lookup"><span data-stu-id="6f061-108">Parameters</span></span>

  - <span data-ttu-id="6f061-109">value</span><span class="sxs-lookup"><span data-stu-id="6f061-109">value</span></span>  
    <span data-ttu-id="6f061-110">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="6f061-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="6f061-111">位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="6f061-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="6f061-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="6f061-112">startIndex</span></span>  
    <span data-ttu-id="6f061-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6f061-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6f061-114">位元組內的開始位置。</span><span class="sxs-lookup"><span data-stu-id="6f061-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="6f061-115">count</span><span class="sxs-lookup"><span data-stu-id="6f061-115">count</span></span>  
    <span data-ttu-id="6f061-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6f061-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6f061-117">要解碼的位元組數。</span><span class="sxs-lookup"><span data-stu-id="6f061-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="6f061-118">err</span><span class="sxs-lookup"><span data-stu-id="6f061-118">err</span></span>  
    <span data-ttu-id="6f061-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6f061-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6f061-120">從 ESENT 傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6f061-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f061-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f061-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6f061-122">參考</span><span class="sxs-lookup"><span data-stu-id="6f061-122">Reference</span></span>

[<span data-ttu-id="6f061-123">DateTimeColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="6f061-123">DateTimeColumnValue class</span></span>](./datetimecolumnvalue-class.md)

[<span data-ttu-id="6f061-124">DateTimeColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="6f061-124">DateTimeColumnValue members</span></span>](./datetimecolumnvalue-members.md)

[<span data-ttu-id="6f061-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6f061-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
