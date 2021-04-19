---
description: Configure 方法會提交 capture 的設定資訊。
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'IESP：： Configure 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 53efbe7eb2887165dacc4cb904822de953b84017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999847"
---
# <a name="iespconfigure-method"></a><span data-ttu-id="6316b-103">IESP：： Configure 方法</span><span class="sxs-lookup"><span data-stu-id="6316b-103">IESP::Configure method</span></span>

<span data-ttu-id="6316b-104">Configure 方法會提交 capture 的 **設定** 資訊。</span><span class="sxs-lookup"><span data-stu-id="6316b-104">The **Configure** method submits configuration information for a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6316b-105">語法</span><span class="sxs-lookup"><span data-stu-id="6316b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="6316b-106">參數</span><span class="sxs-lookup"><span data-stu-id="6316b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6316b-107">*hConfigurationBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6316b-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6316b-108">呼叫端所設定之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6316b-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="6316b-109">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6316b-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6316b-110">錯誤 BLOB 的控制碼，其中包含其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="6316b-110">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="6316b-111">如需錯誤 BLOB 內容的相關資訊，請參閱本主題中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="6316b-111">For information about the contents of an error BLOB, see the Remarks section in this topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6316b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6316b-112">Return value</span></span>

<span data-ttu-id="6316b-113">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="6316b-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6316b-114">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="6316b-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="6316b-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6316b-115">Return code</span></span>                                                                                                         | <span data-ttu-id="6316b-116">Description</span><span class="sxs-lookup"><span data-stu-id="6316b-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6316b-117"><dt>**NMERR \_ 未 \_ 連接**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-117"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>                | <span data-ttu-id="6316b-118">NPP 未連接到網路。</span><span class="sxs-lookup"><span data-stu-id="6316b-118">The NPP is not connected to the network.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="6316b-119"><dt>**NMERR \_ 非 \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>                      | <span data-ttu-id="6316b-120">NPP 已連接到網路，但不是使用 [IESP：： Connect](iesp-connect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6316b-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="6316b-121"><dt>**NMERR \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-121"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>                     | <span data-ttu-id="6316b-122">NPP 會報告 capture 會話已啟動。</span><span class="sxs-lookup"><span data-stu-id="6316b-122">The NPP reports that the capture session has started.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="6316b-123"><dt>**NMERR 不 \_ 合法的 \_ 觸發程式**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-123"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="6316b-124">設定 BLOB 的觸發程式部分已損毀。</span><span class="sxs-lookup"><span data-stu-id="6316b-124">The trigger portion of the configuration BLOB is corrupt.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="6316b-125"><dt>**NMERR \_ BLOB \_ 專案 \_ 不 \_ \_ 存在**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-125"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="6316b-126">*HConfigurationBlob* 所指定的設定 BLOB 缺少執行這項作業所需的專案。</span><span class="sxs-lookup"><span data-stu-id="6316b-126">The configuration BLOB specified by *hConfigurationBlob* is missing an entry needed to perform this operation.</span></span> <span data-ttu-id="6316b-127">查看 *hErrorBlob* 傳回的錯誤 BLOB，以判斷找不到哪個專案。</span><span class="sxs-lookup"><span data-stu-id="6316b-127">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="6316b-128"><dt>**NMERR \_ BLOB \_ 轉換 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-128"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="6316b-129">BLOB 已損毀。</span><span class="sxs-lookup"><span data-stu-id="6316b-129">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="6316b-130"><dt>**NMERR \_ BLOB \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-130"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="6316b-131">尚未呼叫 **CreateBlob** 方法。</span><span class="sxs-lookup"><span data-stu-id="6316b-131">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="6316b-132"><dt>**NMERR \_ 不正確 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-132"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="6316b-133">指向的物件不是 BLOB。</span><span class="sxs-lookup"><span data-stu-id="6316b-133">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="6316b-134"><dt>**NMERR \_ BLOB \_ 字串 \_ 無效**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-134"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="6316b-135">字串不是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="6316b-135">The string is not null-terminated.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="6316b-136"><dt>**NMERR \_ 上層 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-136"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="6316b-137">BLOB 版本號碼不正確。</span><span class="sxs-lookup"><span data-stu-id="6316b-137">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="6316b-138"><dt>**NMERR \_ \_ 記憶體不足 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-138"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="6316b-139">沒有可用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6316b-139">No memory was available.</span></span> <span data-ttu-id="6316b-140">關閉 windows 以釋出資源。</span><span class="sxs-lookup"><span data-stu-id="6316b-140">Shut down windows to free up resources.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="6316b-141"><dt>**NMERR \_ TIMEOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-141"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="6316b-142">要求已逾時。</span><span class="sxs-lookup"><span data-stu-id="6316b-142">The request has timed out.</span></span><br/>                                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="6316b-143">備註</span><span class="sxs-lookup"><span data-stu-id="6316b-143">Remarks</span></span>

<span data-ttu-id="6316b-144">您必須套用此方法，才能重新開機已啟動且停止但未中斷連線的 NPP。</span><span class="sxs-lookup"><span data-stu-id="6316b-144">You must apply this method to restart an NPP that has been started and stopped, but not disconnected.</span></span>

<span data-ttu-id="6316b-145">*HErrorBlob* 參數所傳回的錯誤 BLOB 包含網路監視器無法在 *hConfigurationBlob* 中指定的設定 BLOB 中瞭解或尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="6316b-145">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="6316b-146">傳回的錯誤 BLOB 包含應用程式可用於進行疑難排解的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="6316b-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="6316b-147">例如，如果傳回 NMERR \_ BLOB \_ 專案不存在，則會在 \_ \_ \_ 傳回的錯誤 BLOB 中包含網路監視器找不到的專案。</span><span class="sxs-lookup"><span data-stu-id="6316b-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="6316b-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="6316b-148">Requirements</span></span>



| <span data-ttu-id="6316b-149">需求</span><span class="sxs-lookup"><span data-stu-id="6316b-149">Requirement</span></span> | <span data-ttu-id="6316b-150">值</span><span class="sxs-lookup"><span data-stu-id="6316b-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6316b-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6316b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="6316b-152">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6316b-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6316b-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6316b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="6316b-154">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6316b-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6316b-155">標頭</span><span class="sxs-lookup"><span data-stu-id="6316b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="6316b-156"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6316b-157">DLL</span><span class="sxs-lookup"><span data-stu-id="6316b-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6316b-158"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6316b-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

 




