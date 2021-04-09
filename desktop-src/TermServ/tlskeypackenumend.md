---
title: TLSKeyPackEnumEnd 函式
description: 從先前的 TLSKeyPackEnumBegin 函式呼叫繼續，然後終止列舉。
ms.assetid: 3434e18d-54c9-46ed-b6a5-bc174b63a152
ms.tgt_platform: multiple
keywords:
- TLSKeyPackEnumEnd 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSKeyPackEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04723318b29adff7a647fe2cab39fb0b16f3f5a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685851"
---
# <a name="tlskeypackenumend-function"></a><span data-ttu-id="e318c-104">TLSKeyPackEnumEnd 函式</span><span class="sxs-lookup"><span data-stu-id="e318c-104">TLSKeyPackEnumEnd function</span></span>

<span data-ttu-id="e318c-105">從先前的 [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) 函式呼叫繼續，然後終止列舉。</span><span class="sxs-lookup"><span data-stu-id="e318c-105">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and terminates the enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="e318c-106">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="e318c-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="e318c-107">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。</span><span class="sxs-lookup"><span data-stu-id="e318c-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e318c-108">語法</span><span class="sxs-lookup"><span data-stu-id="e318c-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="e318c-109">參數</span><span class="sxs-lookup"><span data-stu-id="e318c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e318c-110">*hHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e318c-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e318c-111">遠端桌面授權伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e318c-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="e318c-112">指定 [**TLSConnectToLsServer**](tlsconnecttolsserver.md) 函式所開啟的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e318c-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e318c-113">*pdwErrCode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e318c-113">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e318c-114">變數的指標，此變數會在傳回時接收下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e318c-114">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="e318c-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_S \_ 成功** (0) </span><span class="sxs-lookup"><span data-stu-id="e318c-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e318c-116">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="e318c-116">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span data-ttu-id="e318c-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER \_E \_ 不正確 \_ 控制碼** (5005) </span><span class="sxs-lookup"><span data-stu-id="e318c-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER\_E\_INVALID\_HANDLE** (5005)</span></span>


</dt> <dd>

<span data-ttu-id="e318c-118">控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="e318c-118">The handle is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e318c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="e318c-119">Return value</span></span>

<span data-ttu-id="e318c-120">此函數會傳回下列可能的傳回值。</span><span class="sxs-lookup"><span data-stu-id="e318c-120">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="e318c-121">**RPC \_ S \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="e318c-121">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="e318c-122">呼叫成功。</span><span class="sxs-lookup"><span data-stu-id="e318c-122">The call succeeded.</span></span> <span data-ttu-id="e318c-123">檢查 *pdwErrCode* 參數的值，以取得呼叫的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="e318c-123">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="e318c-124">**RPC \_ S \_ 不正確 \_ ARG**</span><span class="sxs-lookup"><span data-stu-id="e318c-124">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="e318c-125">引數無效。</span><span class="sxs-lookup"><span data-stu-id="e318c-125">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e318c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e318c-126">Requirements</span></span>



| <span data-ttu-id="e318c-127">需求</span><span class="sxs-lookup"><span data-stu-id="e318c-127">Requirement</span></span> | <span data-ttu-id="e318c-128">值</span><span class="sxs-lookup"><span data-stu-id="e318c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e318c-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e318c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e318c-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e318c-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e318c-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e318c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e318c-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e318c-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e318c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e318c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e318c-134"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e318c-134"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e318c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e318c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e318c-136">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="e318c-136">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="e318c-137">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="e318c-137">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="e318c-138">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="e318c-138">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="e318c-139">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="e318c-139">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> </dl>

 

