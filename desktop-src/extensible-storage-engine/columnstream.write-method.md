---
description: 深入瞭解： ColumnStream 撰寫方法
title: ColumnStream 撰寫方法
TOCTitle: 'Write method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Write(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.write(v=EXCHG.10)
ms:contentKeyID: 55100987
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77b62e7dd028da3452082c973690ce0c0210b438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027388"
---
# <a name="columnstreamwrite-method"></a><span data-ttu-id="fd7ca-103">ColumnStream 撰寫方法</span><span class="sxs-lookup"><span data-stu-id="fd7ca-103">ColumnStream.Write method</span></span>

<span data-ttu-id="fd7ca-104">將位元組序列寫入至目前的資料流，並依寫入的位元組數將資料流中目前的位置往前移。</span><span class="sxs-lookup"><span data-stu-id="fd7ca-104">Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.</span></span>

<span data-ttu-id="fd7ca-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fd7ca-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fd7ca-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fd7ca-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7ca-107">語法</span><span class="sxs-lookup"><span data-stu-id="fd7ca-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Sub Write ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
)
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer

instance.Write(buffer, offset, count)
```

``` csharp
public override void Write(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="fd7ca-108">參數</span><span class="sxs-lookup"><span data-stu-id="fd7ca-108">Parameters</span></span>

  - <span data-ttu-id="fd7ca-109">緩衝區</span><span class="sxs-lookup"><span data-stu-id="fd7ca-109">buffer</span></span>  
    <span data-ttu-id="fd7ca-110">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="fd7ca-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="fd7ca-111">要寫入的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fd7ca-111">The buffer to write from.</span></span>

<!-- end list -->

  - <span data-ttu-id="fd7ca-112">Offset</span><span class="sxs-lookup"><span data-stu-id="fd7ca-112">offset</span></span>  
    <span data-ttu-id="fd7ca-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fd7ca-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fd7ca-114">緩衝區中要寫入的位移。</span><span class="sxs-lookup"><span data-stu-id="fd7ca-114">The offset in the buffer to write.</span></span>

<!-- end list -->

  - <span data-ttu-id="fd7ca-115">count</span><span class="sxs-lookup"><span data-stu-id="fd7ca-115">count</span></span>  
    <span data-ttu-id="fd7ca-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fd7ca-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fd7ca-117">要寫入的位元組數。</span><span class="sxs-lookup"><span data-stu-id="fd7ca-117">The number of bytes to write.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd7ca-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd7ca-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fd7ca-119">參考</span><span class="sxs-lookup"><span data-stu-id="fd7ca-119">Reference</span></span>

[<span data-ttu-id="fd7ca-120">ColumnStream 類別</span><span class="sxs-lookup"><span data-stu-id="fd7ca-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="fd7ca-121">ColumnStream 成員</span><span class="sxs-lookup"><span data-stu-id="fd7ca-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="fd7ca-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="fd7ca-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
