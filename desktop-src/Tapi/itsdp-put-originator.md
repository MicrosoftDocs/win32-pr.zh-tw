---
description: Put \_ 建立者方法會設定會議製作者。
ms.assetid: b70fc584-3536-4296-bc38-e20ff6630abc
title: 'ITSdp：:p ut_Originator 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506554668e697e9281dc5dc15784fa36f7429d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986561"
---
# <a name="itsdpput_originator-method"></a><span data-ttu-id="f0115-103">ITSdp：:p 的內容建立者 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="f0115-103">ITSdp::put\_Originator method</span></span>

<span data-ttu-id="f0115-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="f0115-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f0115-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f0115-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f0115-106">**Put 建立 \_** 者方法會設定會議製作者。</span><span class="sxs-lookup"><span data-stu-id="f0115-106">The **put\_Originator** method sets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0115-107">語法</span><span class="sxs-lookup"><span data-stu-id="f0115-107">Syntax</span></span>


```C++
HRESULT put_Originator(
  [in] BSTR pOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="f0115-108">參數</span><span class="sxs-lookup"><span data-stu-id="f0115-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0115-109">*pOriginator* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0115-109">*pOriginator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0115-110">會議建立者之 **BSTR** 表示的指標。</span><span class="sxs-lookup"><span data-stu-id="f0115-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0115-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0115-111">Return value</span></span>

<span data-ttu-id="f0115-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f0115-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f0115-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f0115-113">Return code</span></span>                                                                                   | <span data-ttu-id="f0115-114">Description</span><span class="sxs-lookup"><span data-stu-id="f0115-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f0115-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f0115-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f0115-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="f0115-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f0115-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f0115-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f0115-118">*POriginator* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="f0115-118">The *pOriginator* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="f0115-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f0115-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f0115-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="f0115-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f0115-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="f0115-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f0115-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f0115-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f0115-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f0115-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f0115-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="f0115-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="f0115-125">備註</span><span class="sxs-lookup"><span data-stu-id="f0115-125">Remarks</span></span>

<span data-ttu-id="f0115-126">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pOriginator* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="f0115-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pOriginator* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="f0115-127">此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="f0115-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="f0115-128">使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="f0115-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0115-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0115-129">Requirements</span></span>



| <span data-ttu-id="f0115-130">需求</span><span class="sxs-lookup"><span data-stu-id="f0115-130">Requirement</span></span> | <span data-ttu-id="f0115-131">值</span><span class="sxs-lookup"><span data-stu-id="f0115-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0115-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f0115-132">TAPI version</span></span><br/> | <span data-ttu-id="f0115-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f0115-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f0115-134">標頭</span><span class="sxs-lookup"><span data-stu-id="f0115-134">Header</span></span><br/>       | <dl> <span data-ttu-id="f0115-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0115-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0115-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="f0115-136">Library</span></span><br/>      | <dl> <span data-ttu-id="f0115-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="f0115-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f0115-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f0115-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="f0115-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0115-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0115-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0115-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0115-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="f0115-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="f0115-142">**ITSdp： \_ ：取得建立者**</span><span class="sxs-lookup"><span data-stu-id="f0115-142">**ITSdp::get\_Originator**</span></span>](itsdp-get-originator.md)
</dt> </dl>

 

