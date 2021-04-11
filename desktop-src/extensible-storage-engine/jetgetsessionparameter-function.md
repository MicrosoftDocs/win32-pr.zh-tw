---
description: 深入瞭解： JetGetSessionParameter 函數
title: JetGetSessionParameter 函式
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0ac02142d48009d668d903b39163b425d738b55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847698"
---
# <a name="jetgetsessionparameter-function"></a><span data-ttu-id="115fd-103">JetGetSessionParameter 函式</span><span class="sxs-lookup"><span data-stu-id="115fd-103">JetGetSessionParameter Function</span></span>


<span data-ttu-id="115fd-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="115fd-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="115fd-105">**JetGetSessionParameter** 函式會讀取指定會話的 session 參數。</span><span class="sxs-lookup"><span data-stu-id="115fd-105">The **JetGetSessionParameter** function reads the session parameter for the given session.</span></span>

<span data-ttu-id="115fd-106">**JetGetSessionParameter** 函式是在 Windows 8 作業系統中引進的。</span><span class="sxs-lookup"><span data-stu-id="115fd-106">The **JetGetSessionParameter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a><span data-ttu-id="115fd-107">參數</span><span class="sxs-lookup"><span data-stu-id="115fd-107">Parameters</span></span>

<span data-ttu-id="115fd-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="115fd-108">*sesid*</span></span>

<span data-ttu-id="115fd-109">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="115fd-109">The session to use for this call.</span></span>

<span data-ttu-id="115fd-110">指定時，會忽略指定的實例，並使用與會話相關聯的實例。</span><span class="sxs-lookup"><span data-stu-id="115fd-110">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="115fd-111">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="115fd-111">*sesparamid*</span></span>

<span data-ttu-id="115fd-112">要設定之會話參數的識別碼。</span><span class="sxs-lookup"><span data-stu-id="115fd-112">The ID of the session parameter to set.</span></span>

<span data-ttu-id="115fd-113">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="115fd-113">*pvParam*</span></span>

<span data-ttu-id="115fd-114">此會話參數中的資料。</span><span class="sxs-lookup"><span data-stu-id="115fd-114">Data in this session parameter.</span></span>

<span data-ttu-id="115fd-115">*cbParamMax*</span><span class="sxs-lookup"><span data-stu-id="115fd-115">*cbParamMax*</span></span>

<span data-ttu-id="115fd-116">此會話參數中資料集的大小上限。</span><span class="sxs-lookup"><span data-stu-id="115fd-116">The maximum size of the data set in this session parameter.</span></span>

<span data-ttu-id="115fd-117">*pcbParamActual*</span><span class="sxs-lookup"><span data-stu-id="115fd-117">*pcbParamActual*</span></span>

<span data-ttu-id="115fd-118">此會話參數中資料集的實際大小。</span><span class="sxs-lookup"><span data-stu-id="115fd-118">The actual size of the data set in this session parameter.</span></span>

### <a name="return-value"></a><span data-ttu-id="115fd-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="115fd-119">Return value</span></span>

<span data-ttu-id="115fd-120">成功時，適用于所要求會話參數的輸出緩衝區將會設定為該會話參數的值。</span><span class="sxs-lookup"><span data-stu-id="115fd-120">On success, the output buffer appropriate for the requested session parameter will be set to the value of that session parameter.</span></span>

<span data-ttu-id="115fd-121">失敗時，輸出緩衝區的狀態將會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="115fd-121">On failure, the state of the output buffers will be undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="115fd-122">備註</span><span class="sxs-lookup"><span data-stu-id="115fd-122">Remarks</span></span>

<span data-ttu-id="115fd-123">Session 參數會用於會話的存留期，或在重設值之前使用。</span><span class="sxs-lookup"><span data-stu-id="115fd-123">The session parameter is used for the lifetime of the session or until the value is reset.</span></span>

#### <a name="requirements"></a><span data-ttu-id="115fd-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="115fd-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="115fd-125"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="115fd-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="115fd-126">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="115fd-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="115fd-127"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="115fd-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="115fd-128">需要 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="115fd-128">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="115fd-129"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="115fd-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="115fd-130">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="115fd-130">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="115fd-131"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="115fd-131"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="115fd-132">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="115fd-132">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="115fd-133"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="115fd-133"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="115fd-134">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="115fd-134">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="115fd-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="115fd-135">See also</span></span>

[<span data-ttu-id="115fd-136">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="115fd-136">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="115fd-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="115fd-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="115fd-138">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="115fd-138">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="115fd-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="115fd-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="115fd-140">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="115fd-140">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="115fd-141">JetInit</span><span class="sxs-lookup"><span data-stu-id="115fd-141">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="115fd-142">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="115fd-142">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="115fd-143">JetStopService</span><span class="sxs-lookup"><span data-stu-id="115fd-143">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="115fd-144">系統參數</span><span class="sxs-lookup"><span data-stu-id="115fd-144">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
