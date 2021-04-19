---
description: '深入瞭解： EsentException 的函式 (SerializationInfo、StreamingCoNtext) '
title: EsentException 函式 (SerializationInfo、StreamingCoNtext)  (Microsoft) 。
TOCTitle: EsentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100719
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bdcfe5c3b37746f50926850b45763f9d70de893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992107"
---
# <a name="esentexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="38c3b-103">EsentException 函式 (SerializationInfo、StreamingCoNtext) </span><span class="sxs-lookup"><span data-stu-id="38c3b-103">EsentException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="38c3b-104">初始化 EsentException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="38c3b-104">Initializes a new instance of the EsentException class.</span></span> <span data-ttu-id="38c3b-105">這個函式是用來將序列化的例外狀況還原序列化。</span><span class="sxs-lookup"><span data-stu-id="38c3b-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="38c3b-106">**命名空間：**  [Microsoft. Isam. Esent](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="38c3b-106">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="38c3b-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="38c3b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="38c3b-108">語法</span><span class="sxs-lookup"><span data-stu-id="38c3b-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentException(info, context)
```

``` csharp
protected EsentException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="38c3b-109">參數</span><span class="sxs-lookup"><span data-stu-id="38c3b-109">Parameters</span></span>

  - <span data-ttu-id="38c3b-110">info</span><span class="sxs-lookup"><span data-stu-id="38c3b-110">info</span></span>  
    <span data-ttu-id="38c3b-111">類型： [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。</span><span class="sxs-lookup"><span data-stu-id="38c3b-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="38c3b-112">還原序列化物件所需的資料。</span><span class="sxs-lookup"><span data-stu-id="38c3b-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="38c3b-113">內容</span><span class="sxs-lookup"><span data-stu-id="38c3b-113">context</span></span>  
    <span data-ttu-id="38c3b-114">類型： [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) 。</span><span class="sxs-lookup"><span data-stu-id="38c3b-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="38c3b-115">還原序列化內容。</span><span class="sxs-lookup"><span data-stu-id="38c3b-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="38c3b-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38c3b-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="38c3b-117">參考</span><span class="sxs-lookup"><span data-stu-id="38c3b-117">Reference</span></span>

[<span data-ttu-id="38c3b-118">EsentException 類別</span><span class="sxs-lookup"><span data-stu-id="38c3b-118">EsentException class</span></span>](./esentexception-class.md)

[<span data-ttu-id="38c3b-119">EsentException 成員</span><span class="sxs-lookup"><span data-stu-id="38c3b-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="38c3b-120">EsentException 多載</span><span class="sxs-lookup"><span data-stu-id="38c3b-120">EsentException overload</span></span>](./esentexception-constructor.md)

[<span data-ttu-id="38c3b-121">Microsoft Isam 命名空間</span><span class="sxs-lookup"><span data-stu-id="38c3b-121">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
