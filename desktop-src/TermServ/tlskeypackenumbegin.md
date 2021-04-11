---
title: TLSKeyPackEnumBegin 函式
description: 根據搜尋準則，在遠端桌面授權伺服器上安裝的所有金鑰套件開始列舉。
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- TLSKeyPackEnumBegin 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSKeyPackEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f61197e3c08f5608be954a9288ea54cad5586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317479"
---
# <a name="tlskeypackenumbegin-function"></a><span data-ttu-id="a820a-104">TLSKeyPackEnumBegin 函式</span><span class="sxs-lookup"><span data-stu-id="a820a-104">TLSKeyPackEnumBegin function</span></span>

<span data-ttu-id="a820a-105">根據搜尋準則，在遠端桌面授權伺服器上安裝的所有金鑰套件開始列舉。</span><span class="sxs-lookup"><span data-stu-id="a820a-105">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="a820a-106">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="a820a-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="a820a-107">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。</span><span class="sxs-lookup"><span data-stu-id="a820a-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a820a-108">語法</span><span class="sxs-lookup"><span data-stu-id="a820a-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="a820a-109">參數</span><span class="sxs-lookup"><span data-stu-id="a820a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a820a-110">*hHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a820a-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a820a-111">遠端桌面授權伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a820a-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="a820a-112">指定 [**TLSConnectToLsServer**](tlsconnecttolsserver.md) 函式所開啟的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a820a-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a820a-113">*dwSearchParm* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a820a-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a820a-114">指定搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="a820a-114">Specifies the search criteria.</span></span> <span data-ttu-id="a820a-115">此參數會保留供日後使用，且必須包含0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="a820a-115">This parameter is reserved for future use and must contain 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="a820a-116">*bMatchAll* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a820a-116">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a820a-117">指定是否要符合所有搜尋值。</span><span class="sxs-lookup"><span data-stu-id="a820a-117">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="a820a-118">*lpSearchParm* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a820a-118">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a820a-119">[**LSKeyPack**](lskeypack.md)結構的指標，指定要尋找的搜尋參數。</span><span class="sxs-lookup"><span data-stu-id="a820a-119">Pointer to a [**LSKeyPack**](lskeypack.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="a820a-120">*pdwErrCode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a820a-120">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a820a-121">變數的指標，此變數會在傳回時接收下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a820a-121">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="a820a-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_S \_ 成功** (0) </span><span class="sxs-lookup"><span data-stu-id="a820a-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a820a-123">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="a820a-123">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="a820a-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_E \_ 內部 \_ 錯誤** (5001) </span><span class="sxs-lookup"><span data-stu-id="a820a-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="a820a-125">授權伺服器發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="a820a-125">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="a820a-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_E \_ 不正確 \_ 序列** (5006) </span><span class="sxs-lookup"><span data-stu-id="a820a-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="a820a-127">呼叫順序無效。</span><span class="sxs-lookup"><span data-stu-id="a820a-127">The calling sequence was not valid.</span></span> <span data-ttu-id="a820a-128">最可能的情況是先前的列舉尚未結束。</span><span class="sxs-lookup"><span data-stu-id="a820a-128">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="a820a-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_E \_ SERVER \_ 忙碌** (5007) </span><span class="sxs-lookup"><span data-stu-id="a820a-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="a820a-130">授權伺服器太忙碌，無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="a820a-130">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="a820a-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_E \_ OUTOFMEMORY** (5008) </span><span class="sxs-lookup"><span data-stu-id="a820a-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="a820a-132">因為記憶體不足，所以無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="a820a-132">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="a820a-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_E \_ 不正確 \_ 資料** (5009) </span><span class="sxs-lookup"><span data-stu-id="a820a-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="a820a-134">搜尋參數中的資料無效。</span><span class="sxs-lookup"><span data-stu-id="a820a-134">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a820a-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="a820a-135">Return value</span></span>

<span data-ttu-id="a820a-136">此函數會傳回下列可能的傳回值。</span><span class="sxs-lookup"><span data-stu-id="a820a-136">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="a820a-137">**RPC \_ S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="a820a-137">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="a820a-138">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="a820a-138">The call succeeded.</span></span> <span data-ttu-id="a820a-139">檢查 *pdwErrCode* 參數的值，以取得呼叫的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="a820a-139">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="a820a-140">**RPC \_ S \_ 不正確 \_ ARG**</span><span class="sxs-lookup"><span data-stu-id="a820a-140">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="a820a-141">引數無效。</span><span class="sxs-lookup"><span data-stu-id="a820a-141">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a820a-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="a820a-142">Requirements</span></span>



| <span data-ttu-id="a820a-143">需求</span><span class="sxs-lookup"><span data-stu-id="a820a-143">Requirement</span></span> | <span data-ttu-id="a820a-144">值</span><span class="sxs-lookup"><span data-stu-id="a820a-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a820a-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a820a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a820a-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a820a-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a820a-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a820a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a820a-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a820a-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a820a-149">DLL</span><span class="sxs-lookup"><span data-stu-id="a820a-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a820a-150"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a820a-150"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a820a-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a820a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a820a-152">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="a820a-152">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="a820a-153">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="a820a-153">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="a820a-154">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="a820a-154">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="a820a-155">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="a820a-155">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

