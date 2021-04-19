---
description: 提供 tablet 執行緒之間共用記憶體的存取。
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: ITabletCoNtextP：： UseSharedMemoryCommunications 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997210"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a><span data-ttu-id="650af-103">ITabletCoNtextP：： UseSharedMemoryCommunications 方法</span><span class="sxs-lookup"><span data-stu-id="650af-103">ITabletContextP::UseSharedMemoryCommunications method</span></span>

<span data-ttu-id="650af-104">提供 tablet 執行緒之間共用記憶體的存取。</span><span class="sxs-lookup"><span data-stu-id="650af-104">Provides access to memory shared between tablet threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="650af-105">語法</span><span class="sxs-lookup"><span data-stu-id="650af-105">Syntax</span></span>


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a><span data-ttu-id="650af-106">參數</span><span class="sxs-lookup"><span data-stu-id="650af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="650af-107">*pid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="650af-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="650af-108">處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="650af-108">Process id.</span></span>

</dd> <dt>

<span data-ttu-id="650af-109">*phEventMoreData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="650af-109">*phEventMoreData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="650af-110">當有新資料可供處理時，發出信號的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="650af-110">Event handle that signals when new data is available to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="650af-111">*phEventClientReady* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="650af-111">*phEventClientReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="650af-112">傳回的事件控制碼，用來指示用戶端已準備好接收資料。</span><span class="sxs-lookup"><span data-stu-id="650af-112">Returned event handle used to signal that the client is ready to receive data.</span></span> <span data-ttu-id="650af-113">在處理新資料之後收到信號。</span><span class="sxs-lookup"><span data-stu-id="650af-113">Signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="650af-114">*phMutexAccess* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="650af-114">*phMutexAccess* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="650af-115">Mutex 授與共享記憶體的存取權。</span><span class="sxs-lookup"><span data-stu-id="650af-115">The mutex granting access to shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="650af-116">*phFileMapping* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="650af-116">*phFileMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="650af-117">共用記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="650af-117">Pointer to the shared memory block.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="650af-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="650af-118">Return value</span></span>

<span data-ttu-id="650af-119">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="650af-119">This method can return one of these values.</span></span>



| <span data-ttu-id="650af-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="650af-120">Return code</span></span>                                                                            | <span data-ttu-id="650af-121">Description</span><span class="sxs-lookup"><span data-stu-id="650af-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="650af-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="650af-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="650af-123">成功。</span><span class="sxs-lookup"><span data-stu-id="650af-123">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="650af-124"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="650af-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="650af-125">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="650af-125">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="650af-126">備註</span><span class="sxs-lookup"><span data-stu-id="650af-126">Remarks</span></span>

<span data-ttu-id="650af-127">**UseSharedMemoryCommunications** 方法是用來做為 Tablet PC 共用記憶體通訊協定的一部分。</span><span class="sxs-lookup"><span data-stu-id="650af-127">The **UseSharedMemoryCommunications** method is used as part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="650af-128">由於 Wisptis 服務具有 (IL) 的高度完整性層級，因此它可以儲存和存取儲存在共用記憶體中的資料，而不需要提升其許可權。</span><span class="sxs-lookup"><span data-stu-id="650af-128">Since the Wisptis service has a high integrity level (IL), it can store and access data stored in shared memory without needing to elevate its privileges.</span></span>

<span data-ttu-id="650af-129">[**SHAREDMEMORY \_ 標頭**](sharedmemory-header.md)結構會從檔案對應所參考的資料進行轉換，而原始封包資料則會遵循 **SHAREDMEMORY \_ 標頭**。</span><span class="sxs-lookup"><span data-stu-id="650af-129">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping and the raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="650af-130">當引發 *pdwEventClientReady* 所參考的事件時，可以從共用記憶體讀取原始的封包資料。</span><span class="sxs-lookup"><span data-stu-id="650af-130">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReady* is raised.</span></span>

<span data-ttu-id="650af-131">下列清單描述用來存取和使用共用記憶體的事件順序。</span><span class="sxs-lookup"><span data-stu-id="650af-131">The following list describes the sequence of events for accessing and using shared memory.</span></span>

-   <span data-ttu-id="650af-132">用戶端會設定 clientReady 事件。</span><span class="sxs-lookup"><span data-stu-id="650af-132">The client sets the clientReady event.</span></span>
-   <span data-ttu-id="650af-133">用戶端會等候 moreData 事件。</span><span class="sxs-lookup"><span data-stu-id="650af-133">The client waits for the moreData event.</span></span>
-   <span data-ttu-id="650af-134">用戶端會取得 mutex。</span><span class="sxs-lookup"><span data-stu-id="650af-134">The client acquires the mutex.</span></span>
-   <span data-ttu-id="650af-135">用戶端會從共用記憶體區段的封包資料，讀取封包之後的標頭和序號之後的封包資料。</span><span class="sxs-lookup"><span data-stu-id="650af-135">The client reads packet data from the section of shared memory after the header and serial numbers after the packets.</span></span>
-   <span data-ttu-id="650af-136">用戶端會根據 **dwEvent** 的值來處理資料。</span><span class="sxs-lookup"><span data-stu-id="650af-136">The client handles data depending on the value of **dwEvent**.</span></span>
-   <span data-ttu-id="650af-137">用戶端寫入-1 (0xFFFFFFFF) **dwEvent**。</span><span class="sxs-lookup"><span data-stu-id="650af-137">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
-   <span data-ttu-id="650af-138">用戶端釋放 mutex。</span><span class="sxs-lookup"><span data-stu-id="650af-138">The client releases the mutex.</span></span>
-   <span data-ttu-id="650af-139">用戶端會設定 clientReady 事件。</span><span class="sxs-lookup"><span data-stu-id="650af-139">The client sets the clientReady event.</span></span>

## <a name="requirements"></a><span data-ttu-id="650af-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="650af-140">Requirements</span></span>



| <span data-ttu-id="650af-141">需求</span><span class="sxs-lookup"><span data-stu-id="650af-141">Requirement</span></span> | <span data-ttu-id="650af-142">值</span><span class="sxs-lookup"><span data-stu-id="650af-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="650af-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="650af-143">Minimum supported client</span></span><br/> | <span data-ttu-id="650af-144">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="650af-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="650af-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="650af-145">Minimum supported server</span></span><br/> | <span data-ttu-id="650af-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="650af-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="650af-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="650af-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="650af-148"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="650af-148"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="650af-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="650af-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650af-150">**ITabletCoNtextP 介面**</span><span class="sxs-lookup"><span data-stu-id="650af-150">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="650af-151">**UseNamedSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="650af-151">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




