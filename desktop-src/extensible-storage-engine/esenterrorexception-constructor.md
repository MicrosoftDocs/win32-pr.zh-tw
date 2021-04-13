---
description: 深入瞭解： EsentErrorException 的函式
title: EsentErrorException 函式
TOCTitle: 'EsentErrorException constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.esenterrorexception(v=EXCHG.10)
ms:contentKeyID: 55101320
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.EsentErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0728eb316c7d5a5d3cf4a1ad13c2e35451318225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319784"
---
# <a name="esenterrorexception-constructor"></a><span data-ttu-id="26b80-103">EsentErrorException 函式</span><span class="sxs-lookup"><span data-stu-id="26b80-103">EsentErrorException constructor</span></span>

<span data-ttu-id="26b80-104">初始化 EsentErrorException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="26b80-104">Initializes a new instance of the EsentErrorException class.</span></span> <span data-ttu-id="26b80-105">這個函式是用來將序列化的例外狀況還原序列化。</span><span class="sxs-lookup"><span data-stu-id="26b80-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="26b80-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="26b80-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="26b80-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="26b80-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="26b80-108">語法</span><span class="sxs-lookup"><span data-stu-id="26b80-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentErrorException(info, context)
```

``` csharp
protected EsentErrorException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="26b80-109">參數</span><span class="sxs-lookup"><span data-stu-id="26b80-109">Parameters</span></span>

  - <span data-ttu-id="26b80-110">info</span><span class="sxs-lookup"><span data-stu-id="26b80-110">info</span></span>  
    <span data-ttu-id="26b80-111">類型： [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。</span><span class="sxs-lookup"><span data-stu-id="26b80-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="26b80-112">還原序列化物件所需的資料。</span><span class="sxs-lookup"><span data-stu-id="26b80-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="26b80-113">內容</span><span class="sxs-lookup"><span data-stu-id="26b80-113">context</span></span>  
    <span data-ttu-id="26b80-114">類型： [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) 。</span><span class="sxs-lookup"><span data-stu-id="26b80-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="26b80-115">還原序列化內容。</span><span class="sxs-lookup"><span data-stu-id="26b80-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="26b80-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26b80-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="26b80-117">參考</span><span class="sxs-lookup"><span data-stu-id="26b80-117">Reference</span></span>

[<span data-ttu-id="26b80-118">EsentErrorException 類別</span><span class="sxs-lookup"><span data-stu-id="26b80-118">EsentErrorException class</span></span>](./esenterrorexception-class.md)

[<span data-ttu-id="26b80-119">EsentErrorException 成員</span><span class="sxs-lookup"><span data-stu-id="26b80-119">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="26b80-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="26b80-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
