---
description: Put \_ description 方法會設定會話描述。
ms.assetid: 535957e7-effe-4b1b-8cba-38a7a3fe9a9a
title: 'ITSdp：:p ut_Description 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea8799ce9b2b8f3f44147b8ca60a92d2c37d5e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983209"
---
# <a name="itsdpput_description-method"></a><span data-ttu-id="37823-103">ITSdp：:p 的 ui \_ 描述方法</span><span class="sxs-lookup"><span data-stu-id="37823-103">ITSdp::put\_Description method</span></span>

<span data-ttu-id="37823-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="37823-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="37823-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="37823-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="37823-106">**Put \_ description** 方法會設定會話描述。</span><span class="sxs-lookup"><span data-stu-id="37823-106">The **put\_Description** method sets the session description.</span></span>

## <a name="syntax"></a><span data-ttu-id="37823-107">語法</span><span class="sxs-lookup"><span data-stu-id="37823-107">Syntax</span></span>


```C++
HRESULT put_Description(
  [in] BSTR pDescription
);
```



## <a name="parameters"></a><span data-ttu-id="37823-108">參數</span><span class="sxs-lookup"><span data-stu-id="37823-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37823-109">*pDescription* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37823-109">*pDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37823-110">包含會話描述之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="37823-110">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37823-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="37823-111">Return value</span></span>

<span data-ttu-id="37823-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="37823-112">This method can return one of these values.</span></span>



| <span data-ttu-id="37823-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="37823-113">Return code</span></span>                                                                                   | <span data-ttu-id="37823-114">Description</span><span class="sxs-lookup"><span data-stu-id="37823-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="37823-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="37823-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="37823-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="37823-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="37823-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="37823-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="37823-118">*PDescription* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="37823-118">The *pDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="37823-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="37823-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="37823-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="37823-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="37823-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="37823-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="37823-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="37823-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="37823-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="37823-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="37823-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="37823-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="37823-125">備註</span><span class="sxs-lookup"><span data-stu-id="37823-125">Remarks</span></span>

<span data-ttu-id="37823-126">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pDescription* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="37823-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pDescription* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="37823-127">此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="37823-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="37823-128">使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="37823-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="37823-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="37823-129">Requirements</span></span>



| <span data-ttu-id="37823-130">需求</span><span class="sxs-lookup"><span data-stu-id="37823-130">Requirement</span></span> | <span data-ttu-id="37823-131">值</span><span class="sxs-lookup"><span data-stu-id="37823-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37823-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="37823-132">TAPI version</span></span><br/> | <span data-ttu-id="37823-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="37823-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="37823-134">標頭</span><span class="sxs-lookup"><span data-stu-id="37823-134">Header</span></span><br/>       | <dl> <span data-ttu-id="37823-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="37823-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="37823-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="37823-136">Library</span></span><br/>      | <dl> <span data-ttu-id="37823-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="37823-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="37823-138">DLL</span><span class="sxs-lookup"><span data-stu-id="37823-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="37823-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37823-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37823-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37823-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37823-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="37823-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="37823-142">**ITSdp：： get \_ Description**</span><span class="sxs-lookup"><span data-stu-id="37823-142">**ITSdp::get\_Description**</span></span>](itsdp-get-description.md)
</dt> </dl>

 

