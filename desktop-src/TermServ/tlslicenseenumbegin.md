---
title: TLSLicenseEnumBegin 函式
description: 根據搜尋準則開始列舉遠端桌面授權伺服器所發行的授權。
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- TLSLicenseEnumBegin 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95913337de968d0b30780b5898b7f204d947dd4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686480"
---
# <a name="tlslicenseenumbegin-function"></a><span data-ttu-id="a8d23-104">TLSLicenseEnumBegin 函式</span><span class="sxs-lookup"><span data-stu-id="a8d23-104">TLSLicenseEnumBegin function</span></span>

<span data-ttu-id="a8d23-105">根據搜尋準則開始列舉遠端桌面授權伺服器所發行的授權。</span><span class="sxs-lookup"><span data-stu-id="a8d23-105">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="a8d23-106">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="a8d23-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="a8d23-107">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。</span><span class="sxs-lookup"><span data-stu-id="a8d23-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a8d23-108">語法</span><span class="sxs-lookup"><span data-stu-id="a8d23-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="a8d23-109">參數</span><span class="sxs-lookup"><span data-stu-id="a8d23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8d23-110">*hHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8d23-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d23-111">遠端桌面授權伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8d23-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="a8d23-112">指定 [**TLSConnectToLsServer**](tlsconnecttolsserver.md) 函式所開啟的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8d23-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a8d23-113">*dwSearchParm* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8d23-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d23-114">指定搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="a8d23-114">Specifies the search criteria.</span></span> <span data-ttu-id="a8d23-115">參數可以是下列清單所描述的一或多個值的組合。</span><span class="sxs-lookup"><span data-stu-id="a8d23-115">The parameter can be one or a combination of the values that are described in the following list.</span></span> <span data-ttu-id="a8d23-116">參數指定金鑰套件的類型以及要搜尋的金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="a8d23-116">The parameter specifies the type of key pack and which key pack to search.</span></span>

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span data-ttu-id="a8d23-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_搜尋 \_ LICENSEID** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="a8d23-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE\_SEARCH\_LICENSEID** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-118">依授權識別碼搜尋。</span><span class="sxs-lookup"><span data-stu-id="a8d23-118">Search by license ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span data-ttu-id="a8d23-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_搜尋 \_ KEYPACKID** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="a8d23-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE\_SEARCH\_KEYPACKID** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-120">依金鑰套件識別碼搜尋。</span><span class="sxs-lookup"><span data-stu-id="a8d23-120">Search by key pack ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span data-ttu-id="a8d23-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_搜尋 \_ MACHINENAME** (0x00000008) </span><span class="sxs-lookup"><span data-stu-id="a8d23-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE\_SEARCH\_MACHINENAME** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-122">依電腦名稱稱搜尋。</span><span class="sxs-lookup"><span data-stu-id="a8d23-122">Search by machine name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span data-ttu-id="a8d23-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_搜尋使用者 \_ 名稱** (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="a8d23-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE\_SEARCH\_USERNAME** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-124">依使用者名稱搜尋。</span><span class="sxs-lookup"><span data-stu-id="a8d23-124">Search by user name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span data-ttu-id="a8d23-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_搜尋 \_ ISSUEDATE** (0x00000080) </span><span class="sxs-lookup"><span data-stu-id="a8d23-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE\_SEARCH\_ISSUEDATE** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-126">依發行日期搜尋。</span><span class="sxs-lookup"><span data-stu-id="a8d23-126">Search by issue date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span data-ttu-id="a8d23-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_搜尋 \_ EXPIREDATE** (0x00000100) </span><span class="sxs-lookup"><span data-stu-id="a8d23-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE\_SEARCH\_EXPIREDATE** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-128">依到期日搜尋。</span><span class="sxs-lookup"><span data-stu-id="a8d23-128">Search by expiration date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span data-ttu-id="a8d23-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_搜尋 \_ NUMLICENSES** (0x00000200) </span><span class="sxs-lookup"><span data-stu-id="a8d23-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE\_SEARCH\_ NUMLICENSES** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-130">依授權數目搜尋。</span><span class="sxs-lookup"><span data-stu-id="a8d23-130">Search by number of licenses.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span data-ttu-id="a8d23-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_搜尋 \_ 輸入 \_ 狀態** (0x20000000) </span><span class="sxs-lookup"><span data-stu-id="a8d23-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE\_SEARCH\_ ENTRY\_STATUS** (0x20000000)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-132">依專案狀態搜尋。</span><span class="sxs-lookup"><span data-stu-id="a8d23-132">Search by entry status.</span></span>

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span data-ttu-id="a8d23-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_EXSEARCH \_ LICENSESTATUS** (0x00100000) </span><span class="sxs-lookup"><span data-stu-id="a8d23-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE\_EXSEARCH\_LICENSESTATUS** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-134">依授權狀態搜尋。</span><span class="sxs-lookup"><span data-stu-id="a8d23-134">Search by license status.</span></span>

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span data-ttu-id="a8d23-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_搜尋 \_ 所有** (0xffffffff) </span><span class="sxs-lookup"><span data-stu-id="a8d23-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK\_SEARCH\_ALL** (0xFFFFFFFF)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-136">搜尋所有授權。</span><span class="sxs-lookup"><span data-stu-id="a8d23-136">Search all licenses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a8d23-137">*bMatchAll* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8d23-137">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d23-138">指定是否要符合所有搜尋值。</span><span class="sxs-lookup"><span data-stu-id="a8d23-138">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="a8d23-139">*lpSearchParm* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8d23-139">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d23-140">[**LSLicense**](lslicense.md)結構的指標，指定要尋找的搜尋參數。</span><span class="sxs-lookup"><span data-stu-id="a8d23-140">Pointer to a [**LSLicense**](lslicense.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="a8d23-141">*pdwErrCode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a8d23-141">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d23-142">變數的指標，此變數會在傳回時接收下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a8d23-142">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="a8d23-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_S \_ 成功** (0) </span><span class="sxs-lookup"><span data-stu-id="a8d23-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-144">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="a8d23-144">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="a8d23-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_E \_ 內部 \_ 錯誤** (5001) </span><span class="sxs-lookup"><span data-stu-id="a8d23-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-146">授權伺服器發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="a8d23-146">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="a8d23-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_E \_ 不正確 \_ 序列** (5006) </span><span class="sxs-lookup"><span data-stu-id="a8d23-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-148">呼叫順序無效。</span><span class="sxs-lookup"><span data-stu-id="a8d23-148">The calling sequence was not valid.</span></span> <span data-ttu-id="a8d23-149">最可能的情況是先前的列舉尚未結束。</span><span class="sxs-lookup"><span data-stu-id="a8d23-149">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="a8d23-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_E \_ SERVER \_ 忙碌** (5007) </span><span class="sxs-lookup"><span data-stu-id="a8d23-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-151">授權伺服器太忙碌，無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="a8d23-151">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="a8d23-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_E \_ OUTOFMEMORY** (5008) </span><span class="sxs-lookup"><span data-stu-id="a8d23-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-153">因為記憶體不足，所以無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="a8d23-153">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="a8d23-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_E \_ 不正確 \_ 資料** (5009) </span><span class="sxs-lookup"><span data-stu-id="a8d23-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="a8d23-155">搜尋參數中的資料無效。</span><span class="sxs-lookup"><span data-stu-id="a8d23-155">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8d23-156">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8d23-156">Return value</span></span>

<span data-ttu-id="a8d23-157">此函數會傳回下列可能的傳回值。</span><span class="sxs-lookup"><span data-stu-id="a8d23-157">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="a8d23-158">**RPC \_ S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="a8d23-158">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="a8d23-159">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="a8d23-159">The call succeeded.</span></span> <span data-ttu-id="a8d23-160">檢查 *pdwErrCode* 參數的值，以取得呼叫的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="a8d23-160">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="a8d23-161">**RPC \_ S \_ 不正確 \_ ARG**</span><span class="sxs-lookup"><span data-stu-id="a8d23-161">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="a8d23-162">引數無效。</span><span class="sxs-lookup"><span data-stu-id="a8d23-162">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8d23-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8d23-163">Requirements</span></span>



| <span data-ttu-id="a8d23-164">需求</span><span class="sxs-lookup"><span data-stu-id="a8d23-164">Requirement</span></span> | <span data-ttu-id="a8d23-165">值</span><span class="sxs-lookup"><span data-stu-id="a8d23-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d23-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8d23-166">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d23-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8d23-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8d23-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8d23-168">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d23-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8d23-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8d23-170">DLL</span><span class="sxs-lookup"><span data-stu-id="a8d23-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8d23-171"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8d23-171"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8d23-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8d23-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d23-173">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="a8d23-173">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="a8d23-174">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="a8d23-174">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="a8d23-175">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="a8d23-175">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="a8d23-176">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="a8d23-176">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

