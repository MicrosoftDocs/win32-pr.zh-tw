---
description: '深入瞭解： EsentIOException 的函式 (SerializationInfo、StreamingCoNtext) '
title: 'EsentIOException 函式 (SerializationInfo、StreamingCoNtext) '
TOCTitle: EsentIOException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentIOException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102032
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29d6b0666f4a1b38441c4f9878575b9867ae10c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971665"
---
# <a name="esentioexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="0b1fd-103">EsentIOException 函式 (SerializationInfo、StreamingCoNtext) </span><span class="sxs-lookup"><span data-stu-id="0b1fd-103">EsentIOException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="0b1fd-104">初始化 EsentIOException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="0b1fd-104">Initializes a new instance of the EsentIOException class.</span></span> <span data-ttu-id="0b1fd-105">這個函式是用來將序列化的例外狀況還原序列化。</span><span class="sxs-lookup"><span data-stu-id="0b1fd-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="0b1fd-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b1fd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0b1fd-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0b1fd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b1fd-108">語法</span><span class="sxs-lookup"><span data-stu-id="0b1fd-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentIOException(info, context)
```

``` csharp
protected EsentIOException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="0b1fd-109">參數</span><span class="sxs-lookup"><span data-stu-id="0b1fd-109">Parameters</span></span>

  - <span data-ttu-id="0b1fd-110">info</span><span class="sxs-lookup"><span data-stu-id="0b1fd-110">info</span></span>  
    <span data-ttu-id="0b1fd-111">類型： [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。</span><span class="sxs-lookup"><span data-stu-id="0b1fd-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="0b1fd-112">還原序列化物件所需的資料。</span><span class="sxs-lookup"><span data-stu-id="0b1fd-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="0b1fd-113">內容</span><span class="sxs-lookup"><span data-stu-id="0b1fd-113">context</span></span>  
    <span data-ttu-id="0b1fd-114">類型： [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) 。</span><span class="sxs-lookup"><span data-stu-id="0b1fd-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="0b1fd-115">還原序列化內容。</span><span class="sxs-lookup"><span data-stu-id="0b1fd-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b1fd-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b1fd-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b1fd-117">參考</span><span class="sxs-lookup"><span data-stu-id="0b1fd-117">Reference</span></span>

[<span data-ttu-id="0b1fd-118">EsentIOException 類別</span><span class="sxs-lookup"><span data-stu-id="0b1fd-118">EsentIOException class</span></span>](./esentioexception-class.md)

[<span data-ttu-id="0b1fd-119">EsentIOException 成員</span><span class="sxs-lookup"><span data-stu-id="0b1fd-119">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="0b1fd-120">EsentIOException 多載</span><span class="sxs-lookup"><span data-stu-id="0b1fd-120">EsentIOException overload</span></span>](./esentioexception-constructor.md)

[<span data-ttu-id="0b1fd-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0b1fd-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
