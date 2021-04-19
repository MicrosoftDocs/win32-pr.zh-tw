---
title: TLSGetServerCertificate 函式
description: 傳回到遠端桌面授權伺服器的憑證。
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- TLSGetServerCertificate 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3144245863ee4a4316bbce8333f03ca3901cb499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996177"
---
# <a name="tlsgetservercertificate-function"></a><span data-ttu-id="3b6ae-104">TLSGetServerCertificate 函式</span><span class="sxs-lookup"><span data-stu-id="3b6ae-104">TLSGetServerCertificate function</span></span>

<span data-ttu-id="3b6ae-105">傳回到遠端桌面授權伺服器的憑證。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-105">Returns the certificate of the Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="3b6ae-106">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="3b6ae-107">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3b6ae-108">語法</span><span class="sxs-lookup"><span data-stu-id="3b6ae-108">Syntax</span></span>


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="3b6ae-109">參數</span><span class="sxs-lookup"><span data-stu-id="3b6ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b6ae-110">*hHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b6ae-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6ae-111">對 [**TLSConnectToLsServer**](tlsconnecttolsserver.md) 函式的呼叫所開啟的遠端桌面授權伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="3b6ae-112">*bSignCert* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b6ae-112">*bSignCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6ae-113">如果簽章憑證 **則為 TRUE** ，如果是 exchange 憑證則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-113">**TRUE** if signature certificate, **FALSE** if exchange certificate.</span></span>

</dd> <dt>

<span data-ttu-id="3b6ae-114">*ppbCertBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3b6ae-114">*ppbCertBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6ae-115">變數的指標，此變數會接收包含憑證之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-115">Pointer to a variable that receives a pointer to a buffer that contains the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="3b6ae-116">*lpdwCertBlobLen* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3b6ae-116">*lpdwCertBlobLen* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6ae-117">變數的指標，此變數會接收所傳回之憑證的大小。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-117">Pointer to a variable that receives the size of the certificate that is returned.</span></span>

</dd> <dt>

<span data-ttu-id="3b6ae-118">*pdwErrCode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3b6ae-118">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6ae-119">接收錯誤碼之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-119">Pointer to a variable that receives the error code.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="3b6ae-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_S \_ 成功** (0) </span><span class="sxs-lookup"><span data-stu-id="3b6ae-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3b6ae-121">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-121">Call is successful.</span></span>

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span data-ttu-id="3b6ae-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS \_W \_ SELFSIGN \_ CERTIFICATE** (4007) </span><span class="sxs-lookup"><span data-stu-id="3b6ae-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS\_W\_SELFSIGN\_CERTIFICATE** (4007)</span></span>


</dt> <dd>

<span data-ttu-id="3b6ae-123">傳回的憑證是自我簽署的憑證。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-123">Certificate returned is a self-signed certificate.</span></span>

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span data-ttu-id="3b6ae-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS \_W \_ TEMP \_ SELFSIGN \_ CERT** (4009) </span><span class="sxs-lookup"><span data-stu-id="3b6ae-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS\_W\_TEMP\_SELFSIGN\_CERT** (4009)</span></span>


</dt> <dd>

<span data-ttu-id="3b6ae-125">傳回的憑證是暫時性的。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-125">Certificate returned is temporary.</span></span>

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span data-ttu-id="3b6ae-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS \_\_ \_ 拒絕存取** (5003) </span><span class="sxs-lookup"><span data-stu-id="3b6ae-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS\_E\_ACCESS\_DENIED** (5003)</span></span>


</dt> <dd>

<span data-ttu-id="3b6ae-127">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-127">Access denied.</span></span>

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span data-ttu-id="3b6ae-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS \_E \_ 配置 \_** (5007) 的控制碼</span><span class="sxs-lookup"><span data-stu-id="3b6ae-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS\_E\_ALLOCATE\_HANDLE** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="3b6ae-129">伺服器太忙碌，無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-129">Server is too busy to process the request.</span></span>

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span data-ttu-id="3b6ae-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS \_E \_ 無 \_ 憑證** (5022) </span><span class="sxs-lookup"><span data-stu-id="3b6ae-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS\_E\_NO\_CERTIFICATE** (5022)</span></span>


</dt> <dd>

<span data-ttu-id="3b6ae-131">無法取得憑證。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-131">Cannot retrieve a certificate.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b6ae-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b6ae-132">Return value</span></span>

<span data-ttu-id="3b6ae-133">此函數會傳回下列可能的傳回值。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-133">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="3b6ae-134">**RPC \_ S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="3b6ae-134">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="3b6ae-135">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-135">The call succeeded.</span></span> <span data-ttu-id="3b6ae-136">檢查 *pdwErrCode* 參數的值，以取得呼叫的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-136">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="3b6ae-137">**RPC \_ S \_ 不正確 \_ ARG**</span><span class="sxs-lookup"><span data-stu-id="3b6ae-137">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="3b6ae-138">此引數無效。</span><span class="sxs-lookup"><span data-stu-id="3b6ae-138">The argument was invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b6ae-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b6ae-139">Requirements</span></span>



| <span data-ttu-id="3b6ae-140">需求</span><span class="sxs-lookup"><span data-stu-id="3b6ae-140">Requirement</span></span> | <span data-ttu-id="3b6ae-141">值</span><span class="sxs-lookup"><span data-stu-id="3b6ae-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b6ae-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b6ae-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3b6ae-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b6ae-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b6ae-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b6ae-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3b6ae-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b6ae-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b6ae-146">DLL</span><span class="sxs-lookup"><span data-stu-id="3b6ae-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b6ae-147"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b6ae-147"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b6ae-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b6ae-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b6ae-149">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="3b6ae-149">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

