---
title: TLSKeyPackEnumNext 函式
description: 繼續進行先前的 TLSKeyPackEnumBegin 函式呼叫，並傳回與搜尋條件相符的遠端桌面授權伺服器上所安裝的下一個金鑰套件。
ms.assetid: 2614eb7a-df57-42a6-ad34-0a3211a6b8c3
ms.tgt_platform: multiple
keywords:
- TLSKeyPackEnumNext 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSKeyPackEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897874f333ed7933ea1616f7f5ba5f1686736d0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024690"
---
# <a name="tlskeypackenumnext-function"></a><span data-ttu-id="8b2f0-104">TLSKeyPackEnumNext 函式</span><span class="sxs-lookup"><span data-stu-id="8b2f0-104">TLSKeyPackEnumNext function</span></span>

<span data-ttu-id="8b2f0-105">繼續進行先前的 [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) 函式呼叫，並傳回與搜尋條件相符的遠端桌面授權伺服器上所安裝的下一個金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-105">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="8b2f0-106">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="8b2f0-107">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8b2f0-108">語法</span><span class="sxs-lookup"><span data-stu-id="8b2f0-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LsKeyPack  *lpKeyPack,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="8b2f0-109">參數</span><span class="sxs-lookup"><span data-stu-id="8b2f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b2f0-110">*hHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b2f0-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b2f0-111">遠端桌面授權伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="8b2f0-112">指定 [**TLSConnectToLsServer**](tlsconnecttolsserver.md) 函式所開啟的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8b2f0-113">*lpKeyPack* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b2f0-113">*lpKeyPack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b2f0-114">[**LSKeyPack**](lskeypack.md)結構的指標，此結構會接收符合搜尋準則的下一個金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-114">Pointer to a [**LSKeyPack**](lskeypack.md) structure that receives the next key pack that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="8b2f0-115">*pdwErrCode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8b2f0-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b2f0-116">變數的指標，此變數會在傳回時接收下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="8b2f0-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_S \_ 成功** (0) </span><span class="sxs-lookup"><span data-stu-id="8b2f0-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8b2f0-118">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="8b2f0-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_我 \_ 沒有 \_ 其他 \_ 資料** (4001) </span><span class="sxs-lookup"><span data-stu-id="8b2f0-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="8b2f0-120">沒有其他金鑰套件符合搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-120">No more key packs match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="8b2f0-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_E \_ 內部 \_ 錯誤** (5001) </span><span class="sxs-lookup"><span data-stu-id="8b2f0-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="8b2f0-122">授權伺服器發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="8b2f0-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_E \_ 不正確 \_ 序列** (5006) </span><span class="sxs-lookup"><span data-stu-id="8b2f0-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="8b2f0-124">呼叫順序無效。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-124">The calling sequence was not valid.</span></span> <span data-ttu-id="8b2f0-125">必須先呼叫 [**TLSKeyPackEnumBegin ()**](tlskeypackenumbegin.md) 函式，才能進行此工作。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-125">Must call the [**TLSKeyPackEnumBegin()**](tlskeypackenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="8b2f0-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_E \_ SERVER \_ 忙碌** (5007) </span><span class="sxs-lookup"><span data-stu-id="8b2f0-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="8b2f0-127">授權伺服器太忙碌，無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="8b2f0-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_E \_ OUTOFMEMORY** (5008) </span><span class="sxs-lookup"><span data-stu-id="8b2f0-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="8b2f0-129">因為記憶體不足，所以無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b2f0-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b2f0-130">Return value</span></span>

<span data-ttu-id="8b2f0-131">此函數會傳回下列可能的傳回值。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="8b2f0-132">**RPC \_ S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="8b2f0-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="8b2f0-133">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-133">The call succeeded.</span></span> <span data-ttu-id="8b2f0-134">檢查 *pdwErrCode* 參數的值，以取得呼叫的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="8b2f0-135">**RPC \_ S \_ 不正確 \_ ARG**</span><span class="sxs-lookup"><span data-stu-id="8b2f0-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="8b2f0-136">引數無效。</span><span class="sxs-lookup"><span data-stu-id="8b2f0-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b2f0-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b2f0-137">Requirements</span></span>



| <span data-ttu-id="8b2f0-138">需求</span><span class="sxs-lookup"><span data-stu-id="8b2f0-138">Requirement</span></span> | <span data-ttu-id="8b2f0-139">值</span><span class="sxs-lookup"><span data-stu-id="8b2f0-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b2f0-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b2f0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8b2f0-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b2f0-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b2f0-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b2f0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8b2f0-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b2f0-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b2f0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8b2f0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b2f0-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b2f0-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b2f0-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b2f0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b2f0-147">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="8b2f0-147">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="8b2f0-148">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="8b2f0-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="8b2f0-149">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="8b2f0-149">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="8b2f0-150">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="8b2f0-150">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

