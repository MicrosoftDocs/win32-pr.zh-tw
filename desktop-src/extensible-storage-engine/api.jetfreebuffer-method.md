---
description: 深入瞭解： JetFreeBuffer 方法
title: JetFreeBuffer 方法
TOCTitle: 'JetFreeBuffer method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer(System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetfreebuffer(v=EXCHG.10)
ms:contentKeyID: 55100694
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a584caf0f7c59c77e7d3c4a058a03780043e0f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973820"
---
# <a name="apijetfreebuffer-method"></a><span data-ttu-id="3e45c-103">JetFreeBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="3e45c-103">Api.JetFreeBuffer method</span></span>

<span data-ttu-id="3e45c-104">釋出由 database engine 呼叫所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3e45c-104">Frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="3e45c-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3e45c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3e45c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3e45c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3e45c-107">語法</span><span class="sxs-lookup"><span data-stu-id="3e45c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetFreeBuffer ( _
    buffer As IntPtr _
)
'Usage
Dim buffer As IntPtrApi.JetFreeBuffer(buffer)
```

``` csharp
public static void JetFreeBuffer(
    IntPtr buffer
)
```

#### <a name="parameters"></a><span data-ttu-id="3e45c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3e45c-108">Parameters</span></span>

  - <span data-ttu-id="3e45c-109">緩衝區</span><span class="sxs-lookup"><span data-stu-id="3e45c-109">buffer</span></span>  
    <span data-ttu-id="3e45c-110">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="3e45c-110">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="3e45c-111">由資料庫引擎的呼叫所配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3e45c-111">The buffer allocated by a call to the database engine.</span></span> <span data-ttu-id="3e45c-112">[零](/dotnet/api/system.intptr.zero) 是可接受的，將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="3e45c-112">[Zero](/dotnet/api/system.intptr.zero) is acceptable, and will be ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e45c-113">備註</span><span class="sxs-lookup"><span data-stu-id="3e45c-113">Remarks</span></span>

<span data-ttu-id="3e45c-114">這個方法是內部的，因為我們絕對不會將 ESENT 所配置的記憶體公開給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="3e45c-114">This method is internal because we never expose the memory allocated by ESENT to our callers.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e45c-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e45c-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3e45c-116">參考</span><span class="sxs-lookup"><span data-stu-id="3e45c-116">Reference</span></span>

[<span data-ttu-id="3e45c-117">Api 類別</span><span class="sxs-lookup"><span data-stu-id="3e45c-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3e45c-118">Api 成員</span><span class="sxs-lookup"><span data-stu-id="3e45c-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3e45c-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3e45c-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
