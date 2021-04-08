---
description: '深入瞭解： EsentUsageException 的函式 (SerializationInfo、StreamingCoNtext) '
title: 'EsentUsageException 函式 (SerializationInfo、StreamingCoNtext) '
TOCTitle: EsentUsageException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103026
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46100a5f359616b18e5eae0d7b9d9a04b0c2fc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695699"
---
# <a name="esentusageexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="bb2fc-103">EsentUsageException 函式 (SerializationInfo、StreamingCoNtext) </span><span class="sxs-lookup"><span data-stu-id="bb2fc-103">EsentUsageException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="bb2fc-104">初始化 EsentUsageException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="bb2fc-104">Initializes a new instance of the EsentUsageException class.</span></span> <span data-ttu-id="bb2fc-105">這個函式是用來將序列化的例外狀況還原序列化。</span><span class="sxs-lookup"><span data-stu-id="bb2fc-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="bb2fc-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bb2fc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bb2fc-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="bb2fc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bb2fc-108">語法</span><span class="sxs-lookup"><span data-stu-id="bb2fc-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentUsageException(info, context)
```

``` csharp
protected EsentUsageException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="bb2fc-109">參數</span><span class="sxs-lookup"><span data-stu-id="bb2fc-109">Parameters</span></span>

  - <span data-ttu-id="bb2fc-110">info</span><span class="sxs-lookup"><span data-stu-id="bb2fc-110">info</span></span>  
    <span data-ttu-id="bb2fc-111">類型： [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。</span><span class="sxs-lookup"><span data-stu-id="bb2fc-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="bb2fc-112">還原序列化物件所需的資料。</span><span class="sxs-lookup"><span data-stu-id="bb2fc-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="bb2fc-113">內容</span><span class="sxs-lookup"><span data-stu-id="bb2fc-113">context</span></span>  
    <span data-ttu-id="bb2fc-114">類型： [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) 。</span><span class="sxs-lookup"><span data-stu-id="bb2fc-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="bb2fc-115">還原序列化內容。</span><span class="sxs-lookup"><span data-stu-id="bb2fc-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb2fc-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb2fc-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bb2fc-117">參考</span><span class="sxs-lookup"><span data-stu-id="bb2fc-117">Reference</span></span>

[<span data-ttu-id="bb2fc-118">EsentUsageException 類別</span><span class="sxs-lookup"><span data-stu-id="bb2fc-118">EsentUsageException class</span></span>](./esentusageexception-class.md)

[<span data-ttu-id="bb2fc-119">EsentUsageException 成員</span><span class="sxs-lookup"><span data-stu-id="bb2fc-119">EsentUsageException members</span></span>](./esentusageexception-members.md)

[<span data-ttu-id="bb2fc-120">EsentUsageException 多載</span><span class="sxs-lookup"><span data-stu-id="bb2fc-120">EsentUsageException overload</span></span>](./esentusageexception-constructor.md)

[<span data-ttu-id="bb2fc-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bb2fc-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
