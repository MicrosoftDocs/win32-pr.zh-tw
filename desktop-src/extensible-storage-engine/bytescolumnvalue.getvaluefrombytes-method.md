---
description: 深入瞭解： BytesColumnValue. GetValueFromBytes 方法
title: BytesColumnValue. GetValueFromBytes 方法
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.BytesColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55101193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f4651851d6dea72663d002b5f4269f33919e836
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194686"
---
# <a name="bytescolumnvaluegetvaluefrombytes-method"></a><span data-ttu-id="fac2f-103">BytesColumnValue. GetValueFromBytes 方法</span><span class="sxs-lookup"><span data-stu-id="fac2f-103">BytesColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="fac2f-104">從 ESENT 取出資料，將資料解碼，並設定 ColumnValue 物件中的值。</span><span class="sxs-lookup"><span data-stu-id="fac2f-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="fac2f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fac2f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fac2f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fac2f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fac2f-107">語法</span><span class="sxs-lookup"><span data-stu-id="fac2f-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="fac2f-108">參數</span><span class="sxs-lookup"><span data-stu-id="fac2f-108">Parameters</span></span>

  - <span data-ttu-id="fac2f-109">value</span><span class="sxs-lookup"><span data-stu-id="fac2f-109">value</span></span>  
    <span data-ttu-id="fac2f-110">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="fac2f-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="fac2f-111">位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="fac2f-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="fac2f-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="fac2f-112">startIndex</span></span>  
    <span data-ttu-id="fac2f-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fac2f-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fac2f-114">位元組內的開始位置。</span><span class="sxs-lookup"><span data-stu-id="fac2f-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="fac2f-115">count</span><span class="sxs-lookup"><span data-stu-id="fac2f-115">count</span></span>  
    <span data-ttu-id="fac2f-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fac2f-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fac2f-117">要解碼的位元組數。</span><span class="sxs-lookup"><span data-stu-id="fac2f-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="fac2f-118">err</span><span class="sxs-lookup"><span data-stu-id="fac2f-118">err</span></span>  
    <span data-ttu-id="fac2f-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fac2f-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fac2f-120">從 ESENT 傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="fac2f-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="fac2f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fac2f-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fac2f-122">參考</span><span class="sxs-lookup"><span data-stu-id="fac2f-122">Reference</span></span>

[<span data-ttu-id="fac2f-123">BytesColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="fac2f-123">BytesColumnValue class</span></span>](./bytescolumnvalue-class.md)

[<span data-ttu-id="fac2f-124">BytesColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="fac2f-124">BytesColumnValue members</span></span>](./bytescolumnvalue-members.md)

[<span data-ttu-id="fac2f-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="fac2f-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
