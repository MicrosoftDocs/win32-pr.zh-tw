---
description: 提交資料捕獲的設定資料。
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'IRTC：： Configure 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 702a3883acdbb7509d79e76d8fcc73af1e167e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972620"
---
# <a name="irtcconfigure-method"></a><span data-ttu-id="4b1ae-103">IRTC：： Configure 方法</span><span class="sxs-lookup"><span data-stu-id="4b1ae-103">IRTC::Configure method</span></span>

<span data-ttu-id="4b1ae-104">Configure 方法會提交資料捕獲的 [**設定**](configure.md) 資料。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-104">The [**Configure**](configure.md) method submits configuration data for a data capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b1ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="4b1ae-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="4b1ae-106">參數</span><span class="sxs-lookup"><span data-stu-id="4b1ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b1ae-107">*hConfigurationBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b1ae-107">*hConfigurationBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b1ae-108">呼叫端所設定之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-108">A handle to the BLOB that is configured by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="4b1ae-109">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4b1ae-109">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b1ae-110">錯誤 BLOB 的控制碼，其中包含其他錯誤資料。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-110">A handle to an error BLOB that contains additional error data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b1ae-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b1ae-111">Return value</span></span>

<span data-ttu-id="4b1ae-112">如果方法成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4b1ae-113">如果此方法不成功，則傳回值是下列其中一個錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="4b1ae-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="4b1ae-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4b1ae-114">Return code</span></span>                                                                                                         | <span data-ttu-id="4b1ae-115">Description</span><span class="sxs-lookup"><span data-stu-id="4b1ae-115">Description</span></span>                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b1ae-116"><dt>**NMERR \_ BLOB \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-116"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="4b1ae-117">尚未呼叫 **CreateBlob** 方法。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-117">The **CreateBlob** method has not been called.</span></span><br/>                                                                                                                                                 |
| <dl> <span data-ttu-id="4b1ae-118"><dt>**NMERR \_ 不正確 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-118"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="4b1ae-119">指向的物件不是 BLOB。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-119">The object pointed to is not a BLOB.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="4b1ae-120"><dt>**NMERR \_ 上層 \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-120"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="4b1ae-121">BLOB 版本號碼不正確。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-121">The BLOB version number is incorrect.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="4b1ae-122"><dt>**NMERR \_ BLOB \_ 專案 \_ 已 \_ 存在**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-122"><dt>**NMERR\_BLOB\_ENTRY\_ALREADY\_EXISTS**</dt></span></span> </dl>  | <span data-ttu-id="4b1ae-123">BLOB 重複。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-123">Duplicate BLOB.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="4b1ae-124"><dt>**NMERR \_ BLOB \_ 專案 \_ 不 \_ \_ 存在**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-124"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="4b1ae-125">*HConfigurationBlob* 所指定的設定 BLOB 缺少執行這項作業所需的專案。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-125">The configuration BLOB specified by *hConfigurationBlob* lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="4b1ae-126">查看 *hErrorBlob* 傳回的錯誤 BLOB，以判斷找不到哪個專案。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-126">View the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="4b1ae-127"><dt>**NMERR 不 \_ 明確的 \_ 規範**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-127"><dt>**NMERR\_AMBIGUOUS\_SPECIFIER**</dt></span></span> </dl>          | <span data-ttu-id="4b1ae-128">遺漏 BLOB 擁有者或類別資料。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-128">The BLOB Owner or Category data is missing.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="4b1ae-129"><dt>**\_ \_ \_ \_ 找不到 NMERR BLOB 擁有者**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-129"><dt>**NMERR\_BLOB\_OWNER\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="4b1ae-130">找不到 BLOB 擁有者區段。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-130">The BLOB Owner section was not found.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="4b1ae-131"><dt>**\_ \_ \_ \_ 找不到 NMERR BLOB 類別**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-131"><dt>**NMERR\_BLOB\_CATEGORY\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="4b1ae-132">找不到 BLOB 類別區段。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-132">The BLOB Category section was not found.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="4b1ae-133"><dt>**NMERR \_ 未知 \_ 類別**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-133"><dt>**NMERR\_UNKNOWN\_CATEGORY**</dt></span></span> </dl>             | <span data-ttu-id="4b1ae-134">找到 BLOB 類別區段，但無法理解。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-134">The BLOB Category section was found, but not understood.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="4b1ae-135"><dt>**NMERR \_ 未知 \_ 標記**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-135"><dt>**NMERR\_UNKNOWN\_TAG**</dt></span></span> </dl>                  | <span data-ttu-id="4b1ae-136">找到 BLOB 標記區段，但無法理解。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-136">The BLOB Tag section was found, but not understood.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="4b1ae-137"><dt>**NMERR \_ BLOB \_ 轉換 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-137"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="4b1ae-138">BLOB 已損毀。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-138">The BLOB is corrupt.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="4b1ae-139"><dt>**NMERR 不 \_ 合法的 \_ 觸發程式**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-139"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="4b1ae-140">BLOB 的觸發程式部分已損毀。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-140">The trigger portion of the BLOB is corrupt.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="4b1ae-141"><dt>**NMERR \_ BLOB \_ 字串 \_ 無效**</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-141"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="4b1ae-142">字串不是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-142">The string is not null-terminated.</span></span><br/>                                                                                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="4b1ae-143">備註</span><span class="sxs-lookup"><span data-stu-id="4b1ae-143">Remarks</span></span>

<span data-ttu-id="4b1ae-144">您必須套用此方法來重新開機已啟動、已停止但未中斷連線的 NPP。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-144">You must apply this method to restart an NPP that has been started, stopped, but not disconnected.</span></span>

<span data-ttu-id="4b1ae-145">*HErrorBlob* 所傳回的錯誤 BLOB 包含網路監視器在 *hConfigurationBlob* 中指定的設定 BLOB 中無法瞭解或尋找的專案。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-145">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the configuration BLOB specified in *hConfigurationBlob*.</span></span> <span data-ttu-id="4b1ae-146">傳回的錯誤 BLOB 包含應用程式可用於進行疑難排解的錯誤資料。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-146">The returned error BLOB contains error data that the application can use for troubleshooting.</span></span> <span data-ttu-id="4b1ae-147">例如，如果傳回 NMERR \_ BLOB \_ 專案不存在，則會在 \_ \_ \_ 傳回的錯誤 BLOB 中包含網路監視器找不到的專案。</span><span class="sxs-lookup"><span data-stu-id="4b1ae-147">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor cannot find is included in the returned error BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b1ae-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b1ae-148">Requirements</span></span>



| <span data-ttu-id="4b1ae-149">需求</span><span class="sxs-lookup"><span data-stu-id="4b1ae-149">Requirement</span></span> | <span data-ttu-id="4b1ae-150">值</span><span class="sxs-lookup"><span data-stu-id="4b1ae-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b1ae-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b1ae-151">Minimum supported client</span></span><br/> | <span data-ttu-id="4b1ae-152">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b1ae-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="4b1ae-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b1ae-153">Minimum supported server</span></span><br/> | <span data-ttu-id="4b1ae-154">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b1ae-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="4b1ae-155">標頭</span><span class="sxs-lookup"><span data-stu-id="4b1ae-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b1ae-156"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-156"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="4b1ae-157">DLL</span><span class="sxs-lookup"><span data-stu-id="4b1ae-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b1ae-158"><dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b1ae-158"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b1ae-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b1ae-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b1ae-160">IRTC</span><span class="sxs-lookup"><span data-stu-id="4b1ae-160">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="4b1ae-161">IRTC：： Connect</span><span class="sxs-lookup"><span data-stu-id="4b1ae-161">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="4b1ae-162">網路監視器 BLOB</span><span class="sxs-lookup"><span data-stu-id="4b1ae-162">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




