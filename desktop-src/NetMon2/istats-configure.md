---
description: Configure 方法會提交 capture 設定資訊。
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: 'IStats：： Configure 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9f2dddea3132ce81a57f16737c0f90c6277d4efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194543"
---
# <a name="istatsconfigure-method"></a><span data-ttu-id="b3f32-103">IStats：： Configure 方法</span><span class="sxs-lookup"><span data-stu-id="b3f32-103">IStats::Configure method</span></span>

<span data-ttu-id="b3f32-104">**Configure** 方法會提交 capture 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="b3f32-104">The **Configure** method submits capture configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3f32-105">語法</span><span class="sxs-lookup"><span data-stu-id="b3f32-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="b3f32-106">參數</span><span class="sxs-lookup"><span data-stu-id="b3f32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3f32-107">*hConfigurationBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3f32-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3f32-108">呼叫端所設定之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b3f32-108">Handle to the BLOB that the caller configures.</span></span>

</dd> <dt>

<span data-ttu-id="b3f32-109">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b3f32-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3f32-110">錯誤 BLOB 的控制碼，其中包含其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="b3f32-110">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3f32-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3f32-111">Return value</span></span>

<span data-ttu-id="b3f32-112">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="b3f32-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b3f32-113">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="b3f32-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="b3f32-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b3f32-114">Return code</span></span>                                                                                                         | <span data-ttu-id="b3f32-115">Description</span><span class="sxs-lookup"><span data-stu-id="b3f32-115">Description</span></span>                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3f32-116"><dt>**NMERR \_ BLOB \_ 字串 \_ 無效**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-116"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="b3f32-117">字串不是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="b3f32-117">The string is not null-terminated.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="b3f32-118"><dt>**NMERR \_ BLOB \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-118"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="b3f32-119">尚未呼叫 **CreateBlob** 方法。</span><span class="sxs-lookup"><span data-stu-id="b3f32-119">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="b3f32-120"><dt>**NMERR \_ 不正確 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-120"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="b3f32-121">指向的物件不是 BLOB。</span><span class="sxs-lookup"><span data-stu-id="b3f32-121">The object that is pointed to is not a BLOB.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="b3f32-122"><dt>**NMERR \_ 上層 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-122"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="b3f32-123">BLOB 版本號碼不正確。</span><span class="sxs-lookup"><span data-stu-id="b3f32-123">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="b3f32-124"><dt>**NMERR \_ BLOB \_ 專案 \_ 已 \_ 存在**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-124"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="b3f32-125">BLOB 專案已經存在。</span><span class="sxs-lookup"><span data-stu-id="b3f32-125">A BLOB entry already exists.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="b3f32-126"><dt>**NMERR \_ BLOB \_ 專案 \_ 不 \_ \_ 存在**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-126"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="b3f32-127">*HConfigurationBlob* 參數所指定的設定 BLOB 缺少執行這項作業所需的專案。</span><span class="sxs-lookup"><span data-stu-id="b3f32-127">The configuration BLOB specified by the *hConfigurationBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="b3f32-128">查看 *hErrorBlob* 參數所傳回的錯誤 BLOB，以判斷找不到哪個專案。</span><span class="sxs-lookup"><span data-stu-id="b3f32-128">Look at the error BLOB returned by the *hErrorBlob* parameter to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="b3f32-129"><dt>**NMERR 不 \_ 明確的 \_ 規範**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-129"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="b3f32-130">BLOB 缺少擁有者或類別資訊。</span><span class="sxs-lookup"><span data-stu-id="b3f32-130">The BLOB lacks owner or category information.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="b3f32-131"><dt>**\_ \_ \_ \_ 找不到 NMERR BLOB 擁有者**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-131"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="b3f32-132">找不到 BLOB 的擁有者區段。</span><span class="sxs-lookup"><span data-stu-id="b3f32-132">The Owner section of the BLOB was not found.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="b3f32-133"><dt>**\_ \_ \_ \_ 找不到 NMERR BLOB 類別**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-133"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="b3f32-134">找不到 BLOB 的 Category 區段。</span><span class="sxs-lookup"><span data-stu-id="b3f32-134">The Category section of the BLOB was not found.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="b3f32-135"><dt>**NMERR \_ 未知 \_ 類別**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-135"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="b3f32-136">找到類別資訊，但無法理解。</span><span class="sxs-lookup"><span data-stu-id="b3f32-136">Category information was found but not understood.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="b3f32-137"><dt>**NMERR \_ 未知 \_ 標記**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-137"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="b3f32-138">找到標記資訊，但無法理解。</span><span class="sxs-lookup"><span data-stu-id="b3f32-138">Tag information was found but not understood.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="b3f32-139"><dt>**NMERR \_ BLOB \_ 轉換 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-139"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="b3f32-140">BLOB 已損毀。</span><span class="sxs-lookup"><span data-stu-id="b3f32-140">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="b3f32-141"><dt>**NMERR 不 \_ 合法的 \_ 觸發程式**</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-141"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="b3f32-142">BLOB 的觸發程式部分已損毀。</span><span class="sxs-lookup"><span data-stu-id="b3f32-142">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="b3f32-143">備註</span><span class="sxs-lookup"><span data-stu-id="b3f32-143">Remarks</span></span>

<span data-ttu-id="b3f32-144">您必須套用此方法來重新開機已啟動、已停止但未中斷連線的 NPP。</span><span class="sxs-lookup"><span data-stu-id="b3f32-144">You must apply this method to restart an NPP that has been started, stopped but not disconnected.</span></span>

<span data-ttu-id="b3f32-145">*HErrorBlob* 所傳回的錯誤 BLOB 包含網路監視器在 *hConfigurationBlob* 參數中指定的設定 BLOB 中無法瞭解或尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="b3f32-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in the *hConfigurationBlob* parameter.</span></span> <span data-ttu-id="b3f32-146">傳回的錯誤 BLOB 包含應用程式可用於進行疑難排解的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="b3f32-146">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="b3f32-147">例如，如果傳回 NMERR \_ BLOB \_ 專案不存在，則會在 \_ \_ \_ 傳回的錯誤 BLOB 中包含網路監視器找不到的專案。</span><span class="sxs-lookup"><span data-stu-id="b3f32-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3f32-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3f32-148">Requirements</span></span>



| <span data-ttu-id="b3f32-149">需求</span><span class="sxs-lookup"><span data-stu-id="b3f32-149">Requirement</span></span> | <span data-ttu-id="b3f32-150">值</span><span class="sxs-lookup"><span data-stu-id="b3f32-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f32-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3f32-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b3f32-152">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3f32-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b3f32-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3f32-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b3f32-154">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3f32-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b3f32-155">標頭</span><span class="sxs-lookup"><span data-stu-id="b3f32-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3f32-156"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b3f32-157">DLL</span><span class="sxs-lookup"><span data-stu-id="b3f32-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3f32-158"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3f32-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3f32-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3f32-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3f32-160">IStats</span><span class="sxs-lookup"><span data-stu-id="b3f32-160">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="b3f32-161">ISTATS：： Connect</span><span class="sxs-lookup"><span data-stu-id="b3f32-161">ISTATS::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="b3f32-162">網路監視器 BLOB</span><span class="sxs-lookup"><span data-stu-id="b3f32-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




