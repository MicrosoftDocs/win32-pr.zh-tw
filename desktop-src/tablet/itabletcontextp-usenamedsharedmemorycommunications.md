---
description: 設定平板電腦內容的共用記憶體通訊。
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: ITabletCoNtextP：： UseNamedSharedMemoryCommunications 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 81e8c653dd12600ae02fe7e6038de6e6a38786e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985462"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a><span data-ttu-id="98e7e-103">ITabletCoNtextP：： UseNamedSharedMemoryCommunications 方法</span><span class="sxs-lookup"><span data-stu-id="98e7e-103">ITabletContextP::UseNamedSharedMemoryCommunications method</span></span>

<span data-ttu-id="98e7e-104">設定平板電腦內容的共用記憶體通訊。</span><span class="sxs-lookup"><span data-stu-id="98e7e-104">Sets up shared memory communication for the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e7e-105">語法</span><span class="sxs-lookup"><span data-stu-id="98e7e-105">Syntax</span></span>


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a><span data-ttu-id="98e7e-106">參數</span><span class="sxs-lookup"><span data-stu-id="98e7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e7e-107">*pid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98e7e-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98e7e-108">存取共用記憶體之用戶端的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="98e7e-108">The process ID of the client that accesses shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="98e7e-109">*pszCallerSid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98e7e-109">*pszCallerSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98e7e-110">函數呼叫端的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="98e7e-110">The security identifier of the function caller.</span></span>

</dd> <dt>

<span data-ttu-id="98e7e-111">*pszCallerIntegritySid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98e7e-111">*pszCallerIntegritySid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98e7e-112">可以驗證呼叫函數完整性的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="98e7e-112">The security identifier that can verify the integrity of the calling function.</span></span>

</dd> <dt>

<span data-ttu-id="98e7e-113">*pdwEventMoreDataId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="98e7e-113">*pdwEventMoreDataId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98e7e-114">用來建立事件名稱的整數。</span><span class="sxs-lookup"><span data-stu-id="98e7e-114">An integer used to construct the name of an event.</span></span> <span data-ttu-id="98e7e-115">此事件表示是否有更多資料。</span><span class="sxs-lookup"><span data-stu-id="98e7e-115">The event indicates whether there is more data.</span></span>

</dd> <dt>

<span data-ttu-id="98e7e-116">*pdwEventClientReadyId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="98e7e-116">*pdwEventClientReadyId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98e7e-117">用來建立事件名稱的整數。</span><span class="sxs-lookup"><span data-stu-id="98e7e-117">An integer used to construct the name of an event.</span></span> <span data-ttu-id="98e7e-118">此事件表示用戶端已準備好接收資料。</span><span class="sxs-lookup"><span data-stu-id="98e7e-118">The event signals that the client is ready to receive data.</span></span> <span data-ttu-id="98e7e-119">此事件會在處理新資料之後收到信號。</span><span class="sxs-lookup"><span data-stu-id="98e7e-119">The event is signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="98e7e-120">*pdwMutexAccessId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="98e7e-120">*pdwMutexAccessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98e7e-121">共用記憶體的存取識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="98e7e-121">A pointer to the access identifier of the shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="98e7e-122">*pdwFileMappingId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="98e7e-122">*pdwFileMappingId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98e7e-123">識別共用記憶體的整數。</span><span class="sxs-lookup"><span data-stu-id="98e7e-123">An integer that identifies the shared memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e7e-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="98e7e-124">Return value</span></span>

<span data-ttu-id="98e7e-125">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="98e7e-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="98e7e-126">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="98e7e-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e7e-127">備註</span><span class="sxs-lookup"><span data-stu-id="98e7e-127">Remarks</span></span>

<span data-ttu-id="98e7e-128">**UseNamedSharedMemoryCommunications** 方法是 Tablet PC 共用記憶體通訊協定的一部分。</span><span class="sxs-lookup"><span data-stu-id="98e7e-128">The **UseNamedSharedMemoryCommunications** method is part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="98e7e-129">沒有較高許可權的用戶端會在安全識別碼中傳遞 (SID) 和完整性層級安全識別碼 (IL SID) ，讓平板電腦服務可以使用 (ACL) 的存取控制清單來存取共用記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="98e7e-129">A client without elevated privileges passes in a security identifier (SID) and an integrity level security identifier (IL-SID) so that the Tablet service can use access control lists (ACL) to access the shared memory objects.</span></span> <span data-ttu-id="98e7e-130">如果用戶端有更高的許可權，則應該使用 UseSharedMemoryCommunications，也就是當服務已經有更高的許可權時，所呼叫的 API。</span><span class="sxs-lookup"><span data-stu-id="98e7e-130">If the client has elevated privileges, it should use UseSharedMemoryCommunications, which is the API that is called if the service already has an elevated privilege.</span></span>

<span data-ttu-id="98e7e-131">[**SHAREDMEMORY \_ 標頭**](sharedmemory-header.md)結構會儲存共用記憶體標頭。</span><span class="sxs-lookup"><span data-stu-id="98e7e-131">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure stores the shared memory header.</span></span>

<span data-ttu-id="98e7e-132">[**SHAREDMEMORY \_ 標頭**](sharedmemory-header.md)結構是從檔案對應所參考的資料進行轉換。</span><span class="sxs-lookup"><span data-stu-id="98e7e-132">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping.</span></span> <span data-ttu-id="98e7e-133">原始的封包資料會遵循 **SHAREDMEMORY \_ 標頭**。</span><span class="sxs-lookup"><span data-stu-id="98e7e-133">The raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="98e7e-134">當引發 *pdwEventClientReadyId* 所參考的事件時，可以從共用記憶體讀取原始的封包資料。</span><span class="sxs-lookup"><span data-stu-id="98e7e-134">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReadyId* is raised.</span></span>

<span data-ttu-id="98e7e-135">下列清單描述用來存取和使用共用記憶體的事件順序。</span><span class="sxs-lookup"><span data-stu-id="98e7e-135">The following list describes the sequence of events for accessing and using shared memory.</span></span>

1.  <span data-ttu-id="98e7e-136">用戶端會引發 clientReady 事件。</span><span class="sxs-lookup"><span data-stu-id="98e7e-136">The client raises the clientReady event.</span></span>
2.  <span data-ttu-id="98e7e-137">用戶端會等候 moreData 事件。</span><span class="sxs-lookup"><span data-stu-id="98e7e-137">The client waits for the moreData event.</span></span>
3.  <span data-ttu-id="98e7e-138">用戶端會取得 mutex。</span><span class="sxs-lookup"><span data-stu-id="98e7e-138">The client acquires the mutex.</span></span>
4.  <span data-ttu-id="98e7e-139">用戶端會從標頭後面的共用記憶體區段讀取封包資料。</span><span class="sxs-lookup"><span data-stu-id="98e7e-139">The client reads packet data from the section of shared memory that follows the header.</span></span> <span data-ttu-id="98e7e-140">序號會顯示在封包資料之後的共用記憶體中。</span><span class="sxs-lookup"><span data-stu-id="98e7e-140">Serial numbers appear in the shared memory after the packet data.</span></span>
5.  <span data-ttu-id="98e7e-141">用戶端會根據 **dwEvent** 的值來處理資料。</span><span class="sxs-lookup"><span data-stu-id="98e7e-141">The client handles data depending on the value of **dwEvent**.</span></span>
6.  <span data-ttu-id="98e7e-142">用戶端寫入-1 (0xFFFFFFFF) **dwEvent**。</span><span class="sxs-lookup"><span data-stu-id="98e7e-142">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
7.  <span data-ttu-id="98e7e-143">用戶端釋放 mutex。</span><span class="sxs-lookup"><span data-stu-id="98e7e-143">The client releases the mutex.</span></span>
8.  <span data-ttu-id="98e7e-144">用戶端會引發 clientReady 事件。</span><span class="sxs-lookup"><span data-stu-id="98e7e-144">The client raises the clientReady event.</span></span>

<span data-ttu-id="98e7e-145">事件名稱的建立方式是將此方法的輸出格式化。</span><span class="sxs-lookup"><span data-stu-id="98e7e-145">The event names are created by formatting the output of this method.</span></span> <span data-ttu-id="98e7e-146">下列定義可以搭配 sprintf 使用，或其對等專案來建立事件名稱。</span><span class="sxs-lookup"><span data-stu-id="98e7e-146">The following definitions can be used in conjunction with sprintf or its equivalent to create the event names.</span></span>


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



<span data-ttu-id="98e7e-147">在每個定義中，% d 區段會取代為處理序識別碼，而% u 區段會取代為 *pdwEventMoreDataId* 或 *pdwEventClientReadyId* 中傳回的整數。</span><span class="sxs-lookup"><span data-stu-id="98e7e-147">In each definition, the %d section is replaced with the process ID, and the %u section is replaced with the integer returned in *pdwEventMoreDataId* or *pdwEventClientReadyId*.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e7e-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="98e7e-148">Requirements</span></span>



| <span data-ttu-id="98e7e-149">需求</span><span class="sxs-lookup"><span data-stu-id="98e7e-149">Requirement</span></span> | <span data-ttu-id="98e7e-150">值</span><span class="sxs-lookup"><span data-stu-id="98e7e-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98e7e-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98e7e-151">Minimum supported client</span></span><br/> | <span data-ttu-id="98e7e-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98e7e-152">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="98e7e-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98e7e-153">Minimum supported server</span></span><br/> | <span data-ttu-id="98e7e-154">都不支援</span><span class="sxs-lookup"><span data-stu-id="98e7e-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="98e7e-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="98e7e-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="98e7e-156"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="98e7e-156"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e7e-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98e7e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e7e-158">**UseSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="98e7e-158">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[<span data-ttu-id="98e7e-159">**ITabletCoNtextP**</span><span class="sxs-lookup"><span data-stu-id="98e7e-159">**ITabletContextP**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




