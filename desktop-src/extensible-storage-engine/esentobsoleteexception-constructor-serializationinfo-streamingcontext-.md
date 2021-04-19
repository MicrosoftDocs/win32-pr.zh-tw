---
description: '深入瞭解： EsentObsoleteException 的函式 (SerializationInfo、StreamingCoNtext) '
title: 'EsentObsoleteException 函式 (SerializationInfo、StreamingCoNtext) '
TOCTitle: EsentObsoleteException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102167
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b287a61396f0d908c888b84553e5dc67df907be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975042"
---
# <a name="esentobsoleteexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="bf999-103">EsentObsoleteException 函式 (SerializationInfo、StreamingCoNtext) </span><span class="sxs-lookup"><span data-stu-id="bf999-103">EsentObsoleteException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="bf999-104">初始化 EsentObsoleteException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="bf999-104">Initializes a new instance of the EsentObsoleteException class.</span></span> <span data-ttu-id="bf999-105">這個函式是用來將序列化的例外狀況還原序列化。</span><span class="sxs-lookup"><span data-stu-id="bf999-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="bf999-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bf999-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bf999-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="bf999-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bf999-108">語法</span><span class="sxs-lookup"><span data-stu-id="bf999-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentObsoleteException(info, context)
```

``` csharp
protected EsentObsoleteException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="bf999-109">參數</span><span class="sxs-lookup"><span data-stu-id="bf999-109">Parameters</span></span>

  - <span data-ttu-id="bf999-110">info</span><span class="sxs-lookup"><span data-stu-id="bf999-110">info</span></span>  
    <span data-ttu-id="bf999-111">類型： [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。</span><span class="sxs-lookup"><span data-stu-id="bf999-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="bf999-112">還原序列化物件所需的資料。</span><span class="sxs-lookup"><span data-stu-id="bf999-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf999-113">內容</span><span class="sxs-lookup"><span data-stu-id="bf999-113">context</span></span>  
    <span data-ttu-id="bf999-114">類型： [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) 。</span><span class="sxs-lookup"><span data-stu-id="bf999-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="bf999-115">還原序列化內容。</span><span class="sxs-lookup"><span data-stu-id="bf999-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf999-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf999-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bf999-117">參考</span><span class="sxs-lookup"><span data-stu-id="bf999-117">Reference</span></span>

[<span data-ttu-id="bf999-118">EsentObsoleteException 類別</span><span class="sxs-lookup"><span data-stu-id="bf999-118">EsentObsoleteException class</span></span>](./esentobsoleteexception-class.md)

[<span data-ttu-id="bf999-119">EsentObsoleteException 成員</span><span class="sxs-lookup"><span data-stu-id="bf999-119">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="bf999-120">EsentObsoleteException 多載</span><span class="sxs-lookup"><span data-stu-id="bf999-120">EsentObsoleteException overload</span></span>](./esentobsoleteexception-constructor.md)

[<span data-ttu-id="bf999-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bf999-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
