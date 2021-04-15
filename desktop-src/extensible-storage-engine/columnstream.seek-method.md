---
description: 深入瞭解： ColumnStream. Seek 方法
title: ColumnStream. Seek 方法
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5489bb0ee9a4a1550166e14a945a2a6d58c45af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512368"
---
# <a name="columnstreamseek-method"></a><span data-ttu-id="258aa-103">ColumnStream. Seek 方法</span><span class="sxs-lookup"><span data-stu-id="258aa-103">ColumnStream.Seek method</span></span>

<span data-ttu-id="258aa-104">在目前資料流中設定位置。</span><span class="sxs-lookup"><span data-stu-id="258aa-104">Sets the position in the current stream.</span></span>

<span data-ttu-id="258aa-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="258aa-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="258aa-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="258aa-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="258aa-107">語法</span><span class="sxs-lookup"><span data-stu-id="258aa-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a><span data-ttu-id="258aa-108">參數</span><span class="sxs-lookup"><span data-stu-id="258aa-108">Parameters</span></span>

  - <span data-ttu-id="258aa-109">Offset</span><span class="sxs-lookup"><span data-stu-id="258aa-109">offset</span></span>  
    <span data-ttu-id="258aa-110">類型： [Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="258aa-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="258aa-111">相對於原始參數的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="258aa-111">Byte offset relative to the origin parameter.</span></span>

<!-- end list -->

  - <span data-ttu-id="258aa-112">原始</span><span class="sxs-lookup"><span data-stu-id="258aa-112">origin</span></span>  
    <span data-ttu-id="258aa-113">類型： [SeekOrigin](/dotnet/api/system.io.seekorigin)</span><span class="sxs-lookup"><span data-stu-id="258aa-113">Type: [System.IO.SeekOrigin](/dotnet/api/system.io.seekorigin)</span></span>  
    
    <span data-ttu-id="258aa-114">SeekOrigin，表示新位置的參考點。</span><span class="sxs-lookup"><span data-stu-id="258aa-114">A SeekOrigin indicating the reference point for the new position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="258aa-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="258aa-115">Return value</span></span>

<span data-ttu-id="258aa-116">類型： [Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="258aa-116">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
<span data-ttu-id="258aa-117">目前資料流程中的新位置。</span><span class="sxs-lookup"><span data-stu-id="258aa-117">The new position in the current stream.</span></span>  

## <a name="see-also"></a><span data-ttu-id="258aa-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="258aa-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="258aa-119">參考</span><span class="sxs-lookup"><span data-stu-id="258aa-119">Reference</span></span>

[<span data-ttu-id="258aa-120">ColumnStream 類別</span><span class="sxs-lookup"><span data-stu-id="258aa-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="258aa-121">ColumnStream 成員</span><span class="sxs-lookup"><span data-stu-id="258aa-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="258aa-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="258aa-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
