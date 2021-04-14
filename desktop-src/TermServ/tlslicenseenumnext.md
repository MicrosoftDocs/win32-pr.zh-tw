---
title: TLSLicenseEnumNext 函式
description: 繼續進行先前的 TLSLicenseEnumBegin 函式呼叫，並傳回與搜尋條件相符的遠端桌面授權伺服器上所安裝的下一個授權。
ms.assetid: 6932289b-b59c-493c-8dbc-03c0662e921e
ms.tgt_platform: multiple
keywords:
- TLSLicenseEnumNext 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSLicenseEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c13b0a3137258015fe311c49b2cc9b999e3a13f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385254"
---
# <a name="tlslicenseenumnext-function"></a><span data-ttu-id="c3b41-104">TLSLicenseEnumNext 函式</span><span class="sxs-lookup"><span data-stu-id="c3b41-104">TLSLicenseEnumNext function</span></span>

<span data-ttu-id="c3b41-105">繼續進行先前的 [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) 函式呼叫，並傳回與搜尋條件相符的遠端桌面授權伺服器上所安裝的下一個授權。</span><span class="sxs-lookup"><span data-stu-id="c3b41-105">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="c3b41-106">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="c3b41-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="c3b41-107">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。</span><span class="sxs-lookup"><span data-stu-id="c3b41-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c3b41-108">語法</span><span class="sxs-lookup"><span data-stu-id="c3b41-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LSLicense  *lpLicense,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="c3b41-109">參數</span><span class="sxs-lookup"><span data-stu-id="c3b41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3b41-110">*hHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3b41-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3b41-111">遠端桌面授權伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c3b41-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="c3b41-112">指定 [**TLSConnectToLsServer**](tlsconnecttolsserver.md) 函式所開啟的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c3b41-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c3b41-113">*lpLicense* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3b41-113">*lpLicense* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3b41-114">[**LSLicense**](lslicense.md)結構的指標，此結構會接收符合搜尋準則的下一個授權。</span><span class="sxs-lookup"><span data-stu-id="c3b41-114">Pointer to a [**LSLicense**](lslicense.md) structure that receives the next license that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="c3b41-115">*pdwErrCode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c3b41-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3b41-116">變數的指標，此變數會在傳回時接收下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c3b41-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="c3b41-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_S \_ 成功** (0) </span><span class="sxs-lookup"><span data-stu-id="c3b41-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c3b41-118">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="c3b41-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="c3b41-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_我 \_ 沒有 \_ 其他 \_ 資料** (4001) </span><span class="sxs-lookup"><span data-stu-id="c3b41-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="c3b41-120">沒有其他授權符合搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="c3b41-120">No more licenses match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="c3b41-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_E \_ 內部 \_ 錯誤** (5001) </span><span class="sxs-lookup"><span data-stu-id="c3b41-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="c3b41-122">授權伺服器發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="c3b41-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="c3b41-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_E \_ 不正確 \_ 序列** (5006) </span><span class="sxs-lookup"><span data-stu-id="c3b41-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="c3b41-124">呼叫順序無效。</span><span class="sxs-lookup"><span data-stu-id="c3b41-124">The calling sequence was not valid.</span></span> <span data-ttu-id="c3b41-125">必須先呼叫 [**TLSLicenseEnumBegin ()**](tlslicenseenumbegin.md) 函式，才能進行此工作。</span><span class="sxs-lookup"><span data-stu-id="c3b41-125">Must call the [**TLSLicenseEnumBegin()**](tlslicenseenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="c3b41-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_E \_ SERVER \_ 忙碌** (5007) </span><span class="sxs-lookup"><span data-stu-id="c3b41-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="c3b41-127">授權伺服器太忙碌，無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="c3b41-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="c3b41-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_E \_ OUTOFMEMORY** (5008) </span><span class="sxs-lookup"><span data-stu-id="c3b41-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="c3b41-129">因為記憶體不足，所以無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="c3b41-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3b41-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3b41-130">Return value</span></span>

<span data-ttu-id="c3b41-131">此函數會傳回下列可能的傳回值。</span><span class="sxs-lookup"><span data-stu-id="c3b41-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="c3b41-132">**RPC \_ S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="c3b41-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="c3b41-133">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="c3b41-133">The call succeeded.</span></span> <span data-ttu-id="c3b41-134">檢查 *pdwErrCode* 參數的值，以取得呼叫的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="c3b41-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="c3b41-135">**RPC \_ S \_ 不正確 \_ ARG**</span><span class="sxs-lookup"><span data-stu-id="c3b41-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="c3b41-136">引數無效。</span><span class="sxs-lookup"><span data-stu-id="c3b41-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3b41-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3b41-137">Requirements</span></span>



| <span data-ttu-id="c3b41-138">需求</span><span class="sxs-lookup"><span data-stu-id="c3b41-138">Requirement</span></span> | <span data-ttu-id="c3b41-139">值</span><span class="sxs-lookup"><span data-stu-id="c3b41-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b41-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c3b41-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c3b41-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3b41-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3b41-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c3b41-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c3b41-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3b41-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3b41-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c3b41-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3b41-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3b41-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3b41-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3b41-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3b41-147">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="c3b41-147">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="c3b41-148">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="c3b41-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="c3b41-149">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="c3b41-149">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="c3b41-150">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="c3b41-150">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

