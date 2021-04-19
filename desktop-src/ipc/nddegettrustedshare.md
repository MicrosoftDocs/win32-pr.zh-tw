---
description: 抓取受信任共用的伺服器使用者清單中，與 DDE 共用相關聯的選項。
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: 'NDdeGetTrustedShare 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 1f8d7e79c48e0409d8040f6d44159c473dd58ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973001"
---
# <a name="nddegettrustedshare-function"></a><span data-ttu-id="d0dd9-103">NDdeGetTrustedShare 函式</span><span class="sxs-lookup"><span data-stu-id="d0dd9-103">NDdeGetTrustedShare function</span></span>

<span data-ttu-id="d0dd9-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="d0dd9-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="d0dd9-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="d0dd9-106">抓取與在伺服器使用者的受信任共用清單中之 DDE 共用相關聯的選項。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-106">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0dd9-107">語法</span><span class="sxs-lookup"><span data-stu-id="d0dd9-107">Syntax</span></span>


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a><span data-ttu-id="d0dd9-108">參數</span><span class="sxs-lookup"><span data-stu-id="d0dd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0dd9-109">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d0dd9-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0dd9-110">DSDM 所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="d0dd9-111">*lpszShareName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d0dd9-111">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0dd9-112">要查詢其信任狀態的共用名稱。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-112">The share name whose trusted status is being queried.</span></span> <span data-ttu-id="d0dd9-113">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d0dd9-114">*lpdwTrustOptions* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d0dd9-114">*lpdwTrustOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0dd9-115">接收信任選項之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-115">A pointer to a variable that receives the trust options.</span></span> <span data-ttu-id="d0dd9-116">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-116">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="d0dd9-117">有下列信任選項可供使用。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-117">The following trust options are available.</span></span>



| <span data-ttu-id="d0dd9-118">值</span><span class="sxs-lookup"><span data-stu-id="d0dd9-118">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="d0dd9-119">意義</span><span class="sxs-lookup"><span data-stu-id="d0dd9-119">Meaning</span></span>                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <span data-ttu-id="d0dd9-120"><dt>**NDDE \_CMD \_ 顯示 \_ 遮罩**</dt> <dt>0x0000FFFFL</dt></span><span class="sxs-lookup"><span data-stu-id="d0dd9-120"><dt>**NDDE\_CMD\_SHOW\_MASK**</dt> <dt>0x0000FFFFL</dt></span></span> </dl>             | <span data-ttu-id="d0dd9-121">如果 \_ \_ 已設定 NDDE TRUST CMD show，則用來取得用來覆寫「DDE 共用顯示」狀態之值的遮罩 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-121">Mask used to obtain the value used to override the DDE share show state, if NDDE\_TRUST\_CMD\_SHOW is set.</span></span><br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <span data-ttu-id="d0dd9-122"><dt>**NDDE \_信任 \_ CMD \_ 顯示**</dt> <dt>0x10000000L</dt></span><span class="sxs-lookup"><span data-stu-id="d0dd9-122"><dt>**NDDE\_TRUST\_CMD\_SHOW**</dt> <dt>0x10000000L</dt></span></span> </dl>          | <span data-ttu-id="d0dd9-123">覆寫 [DDE 共用 DSDM] 中指定的顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-123">Override the show state specified in the DDE share DSDM.</span></span><br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <span data-ttu-id="d0dd9-124"><dt>**NDDE \_信任 \_ 共用 \_ DEL**</dt> <dt>0x20000000L</dt></span><span class="sxs-lookup"><span data-stu-id="d0dd9-124"><dt>**NDDE\_TRUST\_SHARE\_DEL**</dt> <dt>0x20000000L</dt></span></span> </dl>       | <span data-ttu-id="d0dd9-125">移除共用的受信任狀態。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-125">Remove the share's trusted status.</span></span><br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <span data-ttu-id="d0dd9-126"><dt>**NDDE \_信任 \_ 共用 \_ INIT**</dt> <dt>0x40000000L</dt></span><span class="sxs-lookup"><span data-stu-id="d0dd9-126"><dt>**NDDE\_TRUST\_SHARE\_INIT**</dt> <dt>0x40000000L</dt></span></span> </dl>    | <span data-ttu-id="d0dd9-127">如果應用程式已在使用者的內容中執行，則允許用戶端起始該應用程式。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-127">Allow a client to initiate to the application if it is already running in the user's context.</span></span><br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <span data-ttu-id="d0dd9-128"><dt>**NDDE \_信任 \_ 共用 \_ 開始**</dt> <dt>0x80000000L</dt></span><span class="sxs-lookup"><span data-stu-id="d0dd9-128"><dt>**NDDE\_TRUST\_SHARE\_START**</dt> <dt>0x80000000L</dt></span></span> </dl> | <span data-ttu-id="d0dd9-129">允許在使用者的內容中啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-129">Allow the application to be started in the user's context.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="d0dd9-130">*lpdwShareModId0* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d0dd9-130">*lpdwShareModId0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0dd9-131">變數的指標，此變數會接收受信任共用修改識別碼的第一個部分。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-131">A pointer to a variable that receives the first part of the trusted share modify identifier.</span></span> <span data-ttu-id="d0dd9-132">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-132">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d0dd9-133">*lpdwShareModId1* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d0dd9-133">*lpdwShareModId1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0dd9-134">變數的指標，此變數會接收受信任共用修改識別碼的第二個部分。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-134">A pointer to a variable that receives the second part of the trusted share modify identifier.</span></span> <span data-ttu-id="d0dd9-135">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-135">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0dd9-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0dd9-136">Return value</span></span>

<span data-ttu-id="d0dd9-137">如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-137">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="d0dd9-138">如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-138">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0dd9-139">備註</span><span class="sxs-lookup"><span data-stu-id="d0dd9-139">Remarks</span></span>

<span data-ttu-id="d0dd9-140">受信任的共用修改識別碼會反映 DSDM 中的 DDE 共用在一開始授與信任狀態時的版本。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-140">The trusted share modify identifier reflects the version of the DDE share in the DSDM at the time the DDE share was initially granted trusted status.</span></span> <span data-ttu-id="d0dd9-141">受信任的共用修改識別碼主要是用來移除淘汰的受信任共用。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-141">The trusted share modify identifier is primarily used to remove obsolete trusted shares.</span></span> <span data-ttu-id="d0dd9-142">不過，使用者不需要移除已淘汰的受信任共用。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-142">However, the user does not need to remove obsolete trusted shares.</span></span> <span data-ttu-id="d0dd9-143">網路 DDE 代理程式代表使用者移除已淘汰的共用。</span><span class="sxs-lookup"><span data-stu-id="d0dd9-143">The network DDE agent removes obsolete shares on the user's behalf.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0dd9-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0dd9-144">Requirements</span></span>



| <span data-ttu-id="d0dd9-145">需求</span><span class="sxs-lookup"><span data-stu-id="d0dd9-145">Requirement</span></span> | <span data-ttu-id="d0dd9-146">值</span><span class="sxs-lookup"><span data-stu-id="d0dd9-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0dd9-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0dd9-147">Minimum supported client</span></span><br/> | <span data-ttu-id="d0dd9-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0dd9-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d0dd9-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0dd9-149">Minimum supported server</span></span><br/> | <span data-ttu-id="d0dd9-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0dd9-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d0dd9-151">標頭</span><span class="sxs-lookup"><span data-stu-id="d0dd9-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0dd9-152"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0dd9-152"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0dd9-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="d0dd9-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0dd9-154"><dt>Nddeapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0dd9-154"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d0dd9-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d0dd9-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0dd9-156"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0dd9-156"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0dd9-157">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d0dd9-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d0dd9-158">**NDdeGetTrustedShareW** (Unicode) 和 **NDdeGetTrustedShareA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d0dd9-158">**NDdeGetTrustedShareW** (Unicode) and **NDdeGetTrustedShareA** (ANSI)</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="d0dd9-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0dd9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0dd9-160">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="d0dd9-160">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="d0dd9-161">網路 DDE 函數</span><span class="sxs-lookup"><span data-stu-id="d0dd9-161">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="d0dd9-162">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="d0dd9-162">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)
</dt> </dl>

 

 




