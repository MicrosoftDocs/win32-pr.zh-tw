---
description: 深入瞭解： JetReadFileInstance 方法
title: JetReadFileInstance 方法
TOCTitle: 'JetReadFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetreadfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100781
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80eaf61fd9cd07fce80d32fddf7056f6bff683c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000329"
---
# <a name="apijetreadfileinstance-method"></a><span data-ttu-id="a3589-103">JetReadFileInstance 方法</span><span class="sxs-lookup"><span data-stu-id="a3589-103">Api.JetReadFileInstance method</span></span>

<span data-ttu-id="a3589-104">抓取以 [JetOpenFileInstance (JET_INSTANCE、String、JET_HANDLE、int64、int64) ](./api.jetopenfileinstance-method.md)開啟的檔案內容。</span><span class="sxs-lookup"><span data-stu-id="a3589-104">Retrieves the contents of a file opened with [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md).</span></span>

<span data-ttu-id="a3589-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a3589-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a3589-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a3589-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a3589-107">語法</span><span class="sxs-lookup"><span data-stu-id="a3589-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetReadFileInstance ( _
    instance As JET_INSTANCE, _
    file As JET_HANDLE, _
    buffer As Byte(), _
    bufferSize As Integer, _
    <OutAttribute> ByRef bytesRead As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As JET_HANDLE
Dim buffer As Byte()
Dim bufferSize As Integer
Dim bytesRead As IntegerApi.JetReadFileInstance(instance, _
    file, buffer, bufferSize, bytesRead)
```

``` csharp
public static void JetReadFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE file,
    byte[] buffer,
    int bufferSize,
    out int bytesRead
)
```

#### <a name="parameters"></a><span data-ttu-id="a3589-108">參數</span><span class="sxs-lookup"><span data-stu-id="a3589-108">Parameters</span></span>

  - <span data-ttu-id="a3589-109">instance</span><span class="sxs-lookup"><span data-stu-id="a3589-109">instance</span></span>  
    <span data-ttu-id="a3589-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a3589-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="a3589-111">要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="a3589-111">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a3589-112">file</span><span class="sxs-lookup"><span data-stu-id="a3589-112">file</span></span>  
    <span data-ttu-id="a3589-113">類型： [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a3589-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="a3589-114">要從中讀取的檔案。</span><span class="sxs-lookup"><span data-stu-id="a3589-114">The file to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="a3589-115">緩衝區</span><span class="sxs-lookup"><span data-stu-id="a3589-115">buffer</span></span>  
    <span data-ttu-id="a3589-116">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="a3589-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="a3589-117">要讀入的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a3589-117">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="a3589-118">bufferSize</span><span class="sxs-lookup"><span data-stu-id="a3589-118">bufferSize</span></span>  
    <span data-ttu-id="a3589-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a3589-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a3589-120">緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="a3589-120">The size of the buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="a3589-121">bytesRead</span><span class="sxs-lookup"><span data-stu-id="a3589-121">bytesRead</span></span>  
    <span data-ttu-id="a3589-122">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a3589-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a3589-123">傳回讀入緩衝區的資料量。</span><span class="sxs-lookup"><span data-stu-id="a3589-123">Returns the amount of data read into the buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3589-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3589-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a3589-125">參考</span><span class="sxs-lookup"><span data-stu-id="a3589-125">Reference</span></span>

[<span data-ttu-id="a3589-126">Api 類別</span><span class="sxs-lookup"><span data-stu-id="a3589-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a3589-127">Api 成員</span><span class="sxs-lookup"><span data-stu-id="a3589-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a3589-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a3589-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
