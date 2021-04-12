---
description: '深入瞭解： EsentDiskException 的函式 (SerializationInfo、StreamingCoNtext) '
title: 'EsentDiskException 函式 (SerializationInfo、StreamingCoNtext) '
TOCTitle: EsentDiskException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDiskException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101228
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4abe19b16d9e6eb6d94d5b4fe1dd067b68c2c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320791"
---
# <a name="esentdiskexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="cf35c-103">EsentDiskException 函式 (SerializationInfo、StreamingCoNtext) </span><span class="sxs-lookup"><span data-stu-id="cf35c-103">EsentDiskException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="cf35c-104">初始化 EsentDiskException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="cf35c-104">Initializes a new instance of the EsentDiskException class.</span></span> <span data-ttu-id="cf35c-105">這個函式是用來將序列化的例外狀況還原序列化。</span><span class="sxs-lookup"><span data-stu-id="cf35c-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="cf35c-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cf35c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cf35c-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="cf35c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cf35c-108">語法</span><span class="sxs-lookup"><span data-stu-id="cf35c-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentDiskException(info, context)
```

``` csharp
protected EsentDiskException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="cf35c-109">參數</span><span class="sxs-lookup"><span data-stu-id="cf35c-109">Parameters</span></span>

  - <span data-ttu-id="cf35c-110">info</span><span class="sxs-lookup"><span data-stu-id="cf35c-110">info</span></span>  
    <span data-ttu-id="cf35c-111">類型： [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。</span><span class="sxs-lookup"><span data-stu-id="cf35c-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="cf35c-112">還原序列化物件所需的資料。</span><span class="sxs-lookup"><span data-stu-id="cf35c-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="cf35c-113">內容</span><span class="sxs-lookup"><span data-stu-id="cf35c-113">context</span></span>  
    <span data-ttu-id="cf35c-114">類型： [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) 。</span><span class="sxs-lookup"><span data-stu-id="cf35c-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="cf35c-115">還原序列化內容。</span><span class="sxs-lookup"><span data-stu-id="cf35c-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf35c-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf35c-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cf35c-117">參考</span><span class="sxs-lookup"><span data-stu-id="cf35c-117">Reference</span></span>

[<span data-ttu-id="cf35c-118">EsentDiskException 類別</span><span class="sxs-lookup"><span data-stu-id="cf35c-118">EsentDiskException class</span></span>](./esentdiskexception-class.md)

[<span data-ttu-id="cf35c-119">EsentDiskException 成員</span><span class="sxs-lookup"><span data-stu-id="cf35c-119">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="cf35c-120">EsentDiskException 多載</span><span class="sxs-lookup"><span data-stu-id="cf35c-120">EsentDiskException overload</span></span>](./esentdiskexception-constructor.md)

[<span data-ttu-id="cf35c-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="cf35c-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
