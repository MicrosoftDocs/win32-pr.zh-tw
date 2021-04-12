---
description: 深入瞭解： ColumnStream 類別
title: ColumnStream 類別
TOCTitle: ColumnStream class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100939
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eea249347acd18ec71f03fcdc82b8a2baa1da9ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193438"
---
# <a name="columnstream-class"></a><span data-ttu-id="ec6b1-103">ColumnStream 類別</span><span class="sxs-lookup"><span data-stu-id="ec6b1-103">ColumnStream class</span></span>

<span data-ttu-id="ec6b1-104">這個類別會提供 long 值資料行的串流介面 (亦即 [LongBinary](./jet-coltyp-enumeration.md) 或) [LongText](./jet-coltyp-enumeration.md) 類型的資料行。</span><span class="sxs-lookup"><span data-stu-id="ec6b1-104">This class provides a streaming interface to a long-value column (i.e. a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md)).</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ec6b1-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="ec6b1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ec6b1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ec6b1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ec6b1-107">System.MarshalByRefObject</span><span class="sxs-lookup"><span data-stu-id="ec6b1-107">System.MarshalByRefObject</span></span>](/dotnet/api/system.marshalbyrefobject)  
    [<span data-ttu-id="ec6b1-108">System.object</span><span class="sxs-lookup"><span data-stu-id="ec6b1-108">System.IO.Stream</span></span>](/dotnet/api/system.io.stream)  
      <span data-ttu-id="ec6b1-109">ColumnStream （.）</span><span class="sxs-lookup"><span data-stu-id="ec6b1-109">Microsoft.Isam.Esent.Interop.ColumnStream</span></span>  

<span data-ttu-id="ec6b1-110">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ec6b1-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ec6b1-111">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ec6b1-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ec6b1-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec6b1-112">Syntax</span></span>

``` vb
'Declaration
Public Class ColumnStream _
    Inherits Stream
'Usage
Dim instance As ColumnStream
```

``` csharp
public class ColumnStream : Stream
```

## <a name="thread-safety"></a><span data-ttu-id="ec6b1-113">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="ec6b1-113">Thread safety</span></span>

<span data-ttu-id="ec6b1-114">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec6b1-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ec6b1-115">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec6b1-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec6b1-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec6b1-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ec6b1-117">參考</span><span class="sxs-lookup"><span data-stu-id="ec6b1-117">Reference</span></span>

[<span data-ttu-id="ec6b1-118">ColumnStream 成員</span><span class="sxs-lookup"><span data-stu-id="ec6b1-118">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="ec6b1-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ec6b1-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
