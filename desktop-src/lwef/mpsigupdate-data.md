---
title: 'MPSIGUPDATE_DATA 結構 (MpClient .h) '
description: 傳遞至簽章更新回呼函數的通知資料。
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA 結構舊版 Windows 環境功能
- PMPSIGUPDATE_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104538"
---
# <a name="mpsigupdate_data-structure"></a><span data-ttu-id="4c991-105">MPSIGUPDATE \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="4c991-105">MPSIGUPDATE\_DATA structure</span></span>

<span data-ttu-id="4c991-106">傳遞至簽章更新回呼函數的通知資料。</span><span class="sxs-lookup"><span data-stu-id="4c991-106">Notification data passed to the signature update callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c991-107">語法</span><span class="sxs-lookup"><span data-stu-id="4c991-107">Syntax</span></span>


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a><span data-ttu-id="4c991-108">成員</span><span class="sxs-lookup"><span data-stu-id="4c991-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4c991-109">**dwPercentComplete**</span><span class="sxs-lookup"><span data-stu-id="4c991-109">**dwPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="4c991-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4c991-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="4c991-111">在所有已下載及/或已安裝的更新中，估計百分比。</span><span class="sxs-lookup"><span data-stu-id="4c991-111">An estimate of the percentage across all the updates that have been downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="4c991-112">**dwTotalUpdates**</span><span class="sxs-lookup"><span data-stu-id="4c991-112">**dwTotalUpdates**</span></span>
</dt> <dd>

<span data-ttu-id="4c991-113">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4c991-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="4c991-114">要下載及/或安裝的更新總數。</span><span class="sxs-lookup"><span data-stu-id="4c991-114">Total number of updates to download and/or install.</span></span>

</dd> <dt>

<span data-ttu-id="4c991-115">**dwCurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="4c991-115">**dwCurrentUpdateIndex**</span></span>
</dt> <dd>

<span data-ttu-id="4c991-116">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4c991-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="4c991-117">以零為基底的索引值，指定目前正在下載及/或安裝所需的更新。</span><span class="sxs-lookup"><span data-stu-id="4c991-117">Zero-based index value that specifies which update among those required is currently being downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="4c991-118">**eType**</span><span class="sxs-lookup"><span data-stu-id="4c991-118">**eType**</span></span>
</dt> <dd>

<span data-ttu-id="4c991-119">類型： **MPSIGUPDATE \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="4c991-119">Type: **MPSIGUPDATE\_TYPE**</span></span>

</dd> <dd>

<span data-ttu-id="4c991-120">更新類型。</span><span class="sxs-lookup"><span data-stu-id="4c991-120">Update type.</span></span> <span data-ttu-id="4c991-121">下列其中一個可能值：</span><span class="sxs-lookup"><span data-stu-id="4c991-121">One of the following possible values:</span></span>



| <span data-ttu-id="4c991-122">值</span><span class="sxs-lookup"><span data-stu-id="4c991-122">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="4c991-123">意義</span><span class="sxs-lookup"><span data-stu-id="4c991-123">Meaning</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <span data-ttu-id="4c991-124"><dt>**MPSIGUPDATE \_ 類型 \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-124"><dt>**MPSIGUPDATE\_TYPE\_NONE**</dt></span></span> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <span data-ttu-id="4c991-125"><dt>**MPSIGUPDATE \_ 類型 \_ 受控**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-125"><dt>**MPSIGUPDATE\_TYPE\_MANAGED**</dt></span></span> </dl>                                   | <span data-ttu-id="4c991-126">WSUS 更新。</span><span class="sxs-lookup"><span data-stu-id="4c991-126">WSUS update.</span></span> <span data-ttu-id="4c991-127">Cancel 需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="4c991-127">Cancel requires administrator rights.</span></span><br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <span data-ttu-id="4c991-128"><dt>**MPSIGUPDATE \_ 類型 \_ HTTP**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-128"><dt>**MPSIGUPDATE\_TYPE\_HTTP**</dt></span></span> </dl>                                            | <span data-ttu-id="4c991-129">HTTP 更新。</span><span class="sxs-lookup"><span data-stu-id="4c991-129">HTTP update.</span></span> <span data-ttu-id="4c991-130">不需要取消的系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="4c991-130">Administrator rights not needed to cancel.</span></span><br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <span data-ttu-id="4c991-131"><dt>**MPSIGUPDATE \_ 類型 \_ HTTP \_ SRV**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-131"><dt>**MPSIGUPDATE\_TYPE\_HTTP\_SRV**</dt></span></span> </dl>                               | <span data-ttu-id="4c991-132">來自服務的 HTTP。</span><span class="sxs-lookup"><span data-stu-id="4c991-132">HTTP from service.</span></span> <span data-ttu-id="4c991-133">Cancel 需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="4c991-133">Cancel requires administrator rights.</span></span><br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <span data-ttu-id="4c991-134"><dt>**MPSIGUPDATE \_ 類型 \_ UNC**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-134"><dt>**MPSIGUPDATE\_TYPE\_UNC**</dt></span></span> </dl>                                               | <span data-ttu-id="4c991-135">UNC 共用。</span><span class="sxs-lookup"><span data-stu-id="4c991-135">UNC share.</span></span> <span data-ttu-id="4c991-136">不需要取消的系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="4c991-136">Administrator rights not needed to cancel.</span></span><br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <span data-ttu-id="4c991-137"><dt>**MPSIGUPDATE \_ 類型 \_ 非受控**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-137"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED**</dt></span></span> </dl>                             | <span data-ttu-id="4c991-138">MU/WU 更新。</span><span class="sxs-lookup"><span data-stu-id="4c991-138">MU/WU update.</span></span> <span data-ttu-id="4c991-139">Cancel 需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="4c991-139">Cancel requires administrator rights.</span></span><br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <span data-ttu-id="4c991-140"><dt>**MPSIGUPDATE \_ 類型 \_ 受控 \_ 平臺**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-140"><dt>**MPSIGUPDATE\_TYPE\_MANAGED\_PLATFORM**</dt></span></span> </dl>       | <span data-ttu-id="4c991-141">適用于平臺的 WSUS 更新。</span><span class="sxs-lookup"><span data-stu-id="4c991-141">WSUS update for PLATFORM.</span></span> <span data-ttu-id="4c991-142">Cancel 需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="4c991-142">Cancel requires administrator rights.</span></span><br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <span data-ttu-id="4c991-143"><dt>**MPSIGUPDATE \_ 型別 \_ 非受控 \_ 平臺**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-143"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED\_PLATFORM**</dt></span></span> </dl> | <span data-ttu-id="4c991-144">適用于平臺的 MU/WU 更新。</span><span class="sxs-lookup"><span data-stu-id="4c991-144">MU/WU update for PLATFORM.</span></span> <span data-ttu-id="4c991-145">Cancel 需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="4c991-145">Cancel requires administrator rights.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4c991-146">**階段**</span><span class="sxs-lookup"><span data-stu-id="4c991-146">**Stage**</span></span>
</dt> <dd>

<span data-ttu-id="4c991-147">類型： **MP \_ 更新 \_ 階段**</span><span class="sxs-lookup"><span data-stu-id="4c991-147">Type: **MP\_UPDATE\_STAGE**</span></span>

</dd> <dd>

<span data-ttu-id="4c991-148">更新階段。</span><span class="sxs-lookup"><span data-stu-id="4c991-148">Update stage.</span></span> <span data-ttu-id="4c991-149">下列其中一個可能值：</span><span class="sxs-lookup"><span data-stu-id="4c991-149">One of the following possible values:</span></span>



| <span data-ttu-id="4c991-150">值</span><span class="sxs-lookup"><span data-stu-id="4c991-150">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="4c991-151">意義</span><span class="sxs-lookup"><span data-stu-id="4c991-151">Meaning</span></span>                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <span data-ttu-id="4c991-152"><dt>**MP \_ 階段 \_ 不明**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-152"><dt>**MP\_STAGE\_UNKNOWN**</dt></span></span> </dl>       | <span data-ttu-id="4c991-153">更新階段未知。</span><span class="sxs-lookup"><span data-stu-id="4c991-153">Update stage unknown.</span></span><br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <span data-ttu-id="4c991-154"><dt>**MP \_ 搜尋 \_ 更新**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-154"><dt>**MP\_SEARCH\_UPDATE**</dt></span></span> </dl>       | <span data-ttu-id="4c991-155">更新搜尋階段。</span><span class="sxs-lookup"><span data-stu-id="4c991-155">Update search stage.</span></span><br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <span data-ttu-id="4c991-156"><dt>**MP \_ 下載 \_ 更新**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-156"><dt>**MP\_DOWNLOAD\_UPDATE**</dt></span></span> </dl> | <span data-ttu-id="4c991-157">更新下載階段。</span><span class="sxs-lookup"><span data-stu-id="4c991-157">Update download stage.</span></span><br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <span data-ttu-id="4c991-158"><dt>**MP \_ 安裝 \_ 更新**</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-158"><dt>**MP\_INSTALL\_UPDATE**</dt></span></span> </dl>    | <span data-ttu-id="4c991-159">更新安裝階段。</span><span class="sxs-lookup"><span data-stu-id="4c991-159">Update install stage.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="4c991-160">**路徑**</span><span class="sxs-lookup"><span data-stu-id="4c991-160">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="4c991-161">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="4c991-161">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="4c991-162">更新路徑。</span><span class="sxs-lookup"><span data-stu-id="4c991-162">Update path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c991-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c991-163">Requirements</span></span>



| <span data-ttu-id="4c991-164">需求</span><span class="sxs-lookup"><span data-stu-id="4c991-164">Requirement</span></span> | <span data-ttu-id="4c991-165">值</span><span class="sxs-lookup"><span data-stu-id="4c991-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c991-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c991-166">Minimum supported client</span></span><br/> | <span data-ttu-id="4c991-167">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c991-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4c991-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c991-168">Minimum supported server</span></span><br/> | <span data-ttu-id="4c991-169">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c991-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c991-170">標頭</span><span class="sxs-lookup"><span data-stu-id="4c991-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c991-171"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c991-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





