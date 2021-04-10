---
description: '深入瞭解： EsentFatalException 的函式 (SerializationInfo、StreamingCoNtext) '
title: 'EsentFatalException 函式 (SerializationInfo、StreamingCoNtext) '
TOCTitle: EsentFatalException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFatalException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101554
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2264e3852eb6809f321b9bae162a833e86d7b513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026313"
---
# <a name="esentfatalexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="5fb16-103">EsentFatalException 函式 (SerializationInfo、StreamingCoNtext) </span><span class="sxs-lookup"><span data-stu-id="5fb16-103">EsentFatalException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="5fb16-104">初始化 EsentFatalException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="5fb16-104">Initializes a new instance of the EsentFatalException class.</span></span> <span data-ttu-id="5fb16-105">這個函式是用來將序列化的例外狀況還原序列化。</span><span class="sxs-lookup"><span data-stu-id="5fb16-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="5fb16-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5fb16-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5fb16-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5fb16-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb16-108">語法</span><span class="sxs-lookup"><span data-stu-id="5fb16-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentFatalException(info, context)
```

``` csharp
protected EsentFatalException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="5fb16-109">參數</span><span class="sxs-lookup"><span data-stu-id="5fb16-109">Parameters</span></span>

  - <span data-ttu-id="5fb16-110">info</span><span class="sxs-lookup"><span data-stu-id="5fb16-110">info</span></span>  
    <span data-ttu-id="5fb16-111">類型： [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。</span><span class="sxs-lookup"><span data-stu-id="5fb16-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="5fb16-112">還原序列化物件所需的資料。</span><span class="sxs-lookup"><span data-stu-id="5fb16-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="5fb16-113">內容</span><span class="sxs-lookup"><span data-stu-id="5fb16-113">context</span></span>  
    <span data-ttu-id="5fb16-114">類型： [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) 。</span><span class="sxs-lookup"><span data-stu-id="5fb16-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="5fb16-115">還原序列化內容。</span><span class="sxs-lookup"><span data-stu-id="5fb16-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fb16-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5fb16-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5fb16-117">參考</span><span class="sxs-lookup"><span data-stu-id="5fb16-117">Reference</span></span>

[<span data-ttu-id="5fb16-118">EsentFatalException 類別</span><span class="sxs-lookup"><span data-stu-id="5fb16-118">EsentFatalException class</span></span>](./esentfatalexception-class.md)

[<span data-ttu-id="5fb16-119">EsentFatalException 成員</span><span class="sxs-lookup"><span data-stu-id="5fb16-119">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="5fb16-120">EsentFatalException 多載</span><span class="sxs-lookup"><span data-stu-id="5fb16-120">EsentFatalException overload</span></span>](./esentfatalexception-constructor.md)

[<span data-ttu-id="5fb16-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5fb16-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
