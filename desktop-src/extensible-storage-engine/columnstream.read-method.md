---
description: 深入瞭解： ColumnStream. Read 方法
title: ColumnStream. Read 方法
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e407a9069807d10eaabf4f7ac3fce3919576bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980015"
---
# <a name="columnstreamread-method"></a><span data-ttu-id="18e4f-103">ColumnStream. Read 方法</span><span class="sxs-lookup"><span data-stu-id="18e4f-103">ColumnStream.Read method</span></span>

<span data-ttu-id="18e4f-104">從目前的資料流讀取位元組序列，並依讀取的位元組數將資料流中的位置往前移。</span><span class="sxs-lookup"><span data-stu-id="18e4f-104">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span>

<span data-ttu-id="18e4f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="18e4f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="18e4f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="18e4f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="18e4f-107">語法</span><span class="sxs-lookup"><span data-stu-id="18e4f-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="18e4f-108">參數</span><span class="sxs-lookup"><span data-stu-id="18e4f-108">Parameters</span></span>

  - <span data-ttu-id="18e4f-109">緩衝區</span><span class="sxs-lookup"><span data-stu-id="18e4f-109">buffer</span></span>  
    <span data-ttu-id="18e4f-110">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="18e4f-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="18e4f-111">要讀入的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="18e4f-111">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="18e4f-112">Offset</span><span class="sxs-lookup"><span data-stu-id="18e4f-112">offset</span></span>  
    <span data-ttu-id="18e4f-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="18e4f-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="18e4f-114">緩衝區中要讀入的位移。</span><span class="sxs-lookup"><span data-stu-id="18e4f-114">The offset in the buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="18e4f-115">count</span><span class="sxs-lookup"><span data-stu-id="18e4f-115">count</span></span>  
    <span data-ttu-id="18e4f-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="18e4f-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="18e4f-117">要讀取的位元組數。</span><span class="sxs-lookup"><span data-stu-id="18e4f-117">The number of bytes to read.</span></span>

#### <a name="return-value"></a><span data-ttu-id="18e4f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="18e4f-118">Return value</span></span>

<span data-ttu-id="18e4f-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="18e4f-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="18e4f-120">讀入緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="18e4f-120">The number of bytes read into the buffer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="18e4f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18e4f-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="18e4f-122">參考</span><span class="sxs-lookup"><span data-stu-id="18e4f-122">Reference</span></span>

[<span data-ttu-id="18e4f-123">ColumnStream 類別</span><span class="sxs-lookup"><span data-stu-id="18e4f-123">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="18e4f-124">ColumnStream 成員</span><span class="sxs-lookup"><span data-stu-id="18e4f-124">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="18e4f-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="18e4f-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
