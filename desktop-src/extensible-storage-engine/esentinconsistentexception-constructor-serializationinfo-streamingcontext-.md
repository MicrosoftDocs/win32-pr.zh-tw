---
description: '深入瞭解： EsentInconsistentException 的函式 (SerializationInfo、StreamingCoNtext) '
title: 'EsentInconsistentException 函式 (SerializationInfo、StreamingCoNtext) '
TOCTitle: EsentInconsistentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentInconsistentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101709
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f907288bd4f88cae0b022a74cf558a65415d214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995876"
---
# <a name="esentinconsistentexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="b7b0f-103">EsentInconsistentException 函式 (SerializationInfo、StreamingCoNtext) </span><span class="sxs-lookup"><span data-stu-id="b7b0f-103">EsentInconsistentException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="b7b0f-104">初始化 EsentInconsistentException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="b7b0f-104">Initializes a new instance of the EsentInconsistentException class.</span></span> <span data-ttu-id="b7b0f-105">這個函式是用來將序列化的例外狀況還原序列化。</span><span class="sxs-lookup"><span data-stu-id="b7b0f-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="b7b0f-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7b0f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7b0f-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b7b0f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b0f-108">語法</span><span class="sxs-lookup"><span data-stu-id="b7b0f-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentInconsistentException(info, context)
```

``` csharp
protected EsentInconsistentException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="b7b0f-109">參數</span><span class="sxs-lookup"><span data-stu-id="b7b0f-109">Parameters</span></span>

  - <span data-ttu-id="b7b0f-110">info</span><span class="sxs-lookup"><span data-stu-id="b7b0f-110">info</span></span>  
    <span data-ttu-id="b7b0f-111">類型： [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。</span><span class="sxs-lookup"><span data-stu-id="b7b0f-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="b7b0f-112">還原序列化物件所需的資料。</span><span class="sxs-lookup"><span data-stu-id="b7b0f-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7b0f-113">內容</span><span class="sxs-lookup"><span data-stu-id="b7b0f-113">context</span></span>  
    <span data-ttu-id="b7b0f-114">類型： [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) 。</span><span class="sxs-lookup"><span data-stu-id="b7b0f-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="b7b0f-115">還原序列化內容。</span><span class="sxs-lookup"><span data-stu-id="b7b0f-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7b0f-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7b0f-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7b0f-117">參考</span><span class="sxs-lookup"><span data-stu-id="b7b0f-117">Reference</span></span>

[<span data-ttu-id="b7b0f-118">EsentInconsistentException 類別</span><span class="sxs-lookup"><span data-stu-id="b7b0f-118">EsentInconsistentException class</span></span>](./esentinconsistentexception-class.md)

[<span data-ttu-id="b7b0f-119">EsentInconsistentException 成員</span><span class="sxs-lookup"><span data-stu-id="b7b0f-119">EsentInconsistentException members</span></span>](./esentinconsistentexception-members.md)

[<span data-ttu-id="b7b0f-120">EsentInconsistentException 多載</span><span class="sxs-lookup"><span data-stu-id="b7b0f-120">EsentInconsistentException overload</span></span>](./esentinconsistentexception-constructor.md)

[<span data-ttu-id="b7b0f-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b7b0f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
