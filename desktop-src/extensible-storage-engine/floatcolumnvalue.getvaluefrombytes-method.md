---
description: 深入瞭解： FloatColumnValue. GetValueFromBytes 方法
title: FloatColumnValue. GetValueFromBytes 方法
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.floatcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103242
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.FloatColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21fade2ca6c2febc5c28bdad217f450f81c2673f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974983"
---
# <a name="floatcolumnvaluegetvaluefrombytes-method"></a><span data-ttu-id="f51a4-103">FloatColumnValue. GetValueFromBytes 方法</span><span class="sxs-lookup"><span data-stu-id="f51a4-103">FloatColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="f51a4-104">從 ESENT 取出資料，將資料解碼，並設定 ColumnValue 物件中的值。</span><span class="sxs-lookup"><span data-stu-id="f51a4-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="f51a4-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f51a4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f51a4-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f51a4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f51a4-107">語法</span><span class="sxs-lookup"><span data-stu-id="f51a4-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="f51a4-108">參數</span><span class="sxs-lookup"><span data-stu-id="f51a4-108">Parameters</span></span>

  - <span data-ttu-id="f51a4-109">value</span><span class="sxs-lookup"><span data-stu-id="f51a4-109">value</span></span>  
    <span data-ttu-id="f51a4-110">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="f51a4-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="f51a4-111">位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="f51a4-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="f51a4-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="f51a4-112">startIndex</span></span>  
    <span data-ttu-id="f51a4-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f51a4-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f51a4-114">位元組內的開始位置。</span><span class="sxs-lookup"><span data-stu-id="f51a4-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="f51a4-115">count</span><span class="sxs-lookup"><span data-stu-id="f51a4-115">count</span></span>  
    <span data-ttu-id="f51a4-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f51a4-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f51a4-117">要解碼的位元組數。</span><span class="sxs-lookup"><span data-stu-id="f51a4-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="f51a4-118">err</span><span class="sxs-lookup"><span data-stu-id="f51a4-118">err</span></span>  
    <span data-ttu-id="f51a4-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f51a4-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f51a4-120">從 ESENT 傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f51a4-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="f51a4-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f51a4-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f51a4-122">參考</span><span class="sxs-lookup"><span data-stu-id="f51a4-122">Reference</span></span>

[<span data-ttu-id="f51a4-123">FloatColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="f51a4-123">FloatColumnValue class</span></span>](./floatcolumnvalue-class.md)

[<span data-ttu-id="f51a4-124">FloatColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="f51a4-124">FloatColumnValue members</span></span>](./floatcolumnvalue-members.md)

[<span data-ttu-id="f51a4-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f51a4-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
