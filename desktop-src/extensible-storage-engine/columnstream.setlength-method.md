---
description: 深入瞭解： ColumnStream. SetLength 方法
title: ColumnStream. SetLength 方法
TOCTitle: 'SetLength method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.SetLength(System.Int64)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.setlength(v=EXCHG.10)
ms:contentKeyID: 55100986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.SetLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.SetLength
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fccf32d6494427811c3db8a2d2f4b71a2909a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988983"
---
# <a name="columnstreamsetlength-method"></a><span data-ttu-id="15ca1-103">ColumnStream. SetLength 方法</span><span class="sxs-lookup"><span data-stu-id="15ca1-103">ColumnStream.SetLength method</span></span>

<span data-ttu-id="15ca1-104">設定資料流的長度。</span><span class="sxs-lookup"><span data-stu-id="15ca1-104">Sets the length of the stream.</span></span>

<span data-ttu-id="15ca1-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="15ca1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="15ca1-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="15ca1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="15ca1-107">語法</span><span class="sxs-lookup"><span data-stu-id="15ca1-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Sub SetLength ( _
    value As Long _
)
'Usage
Dim instance As ColumnStream
Dim value As Long

instance.SetLength(value)
```

``` csharp
public override void SetLength(
    long value
)
```

#### <a name="parameters"></a><span data-ttu-id="15ca1-108">參數</span><span class="sxs-lookup"><span data-stu-id="15ca1-108">Parameters</span></span>

  - <span data-ttu-id="15ca1-109">value</span><span class="sxs-lookup"><span data-stu-id="15ca1-109">value</span></span>  
    <span data-ttu-id="15ca1-110">類型： [Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="15ca1-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="15ca1-111">需要的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="15ca1-111">The desired length, in bytes.</span></span>

## <a name="see-also"></a><span data-ttu-id="15ca1-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15ca1-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="15ca1-113">參考</span><span class="sxs-lookup"><span data-stu-id="15ca1-113">Reference</span></span>

[<span data-ttu-id="15ca1-114">ColumnStream 類別</span><span class="sxs-lookup"><span data-stu-id="15ca1-114">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="15ca1-115">ColumnStream 成員</span><span class="sxs-lookup"><span data-stu-id="15ca1-115">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="15ca1-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="15ca1-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
