---
description: 取得 \_ 名稱方法會取得會話名稱。
ms.assetid: 97b44a01-585b-434c-ad59-51c35e8a1ceb
title: 'ITSdp：： get_Name 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b41d431a76f3d0bb2122847e8ee5c3a4dde3c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993979"
---
# <a name="itsdpget_name-method"></a><span data-ttu-id="79ce0-103">ITSdp：： get \_ Name 方法</span><span class="sxs-lookup"><span data-stu-id="79ce0-103">ITSdp::get\_Name method</span></span>

<span data-ttu-id="79ce0-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="79ce0-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="79ce0-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="79ce0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="79ce0-106">**取得 \_ 名稱** 方法會取得會話名稱。</span><span class="sxs-lookup"><span data-stu-id="79ce0-106">The **get\_Name** method gets the session name.</span></span> <span data-ttu-id="79ce0-107">如果字元集是 ASCII，則必須是 ASCII 可轉換字串。</span><span class="sxs-lookup"><span data-stu-id="79ce0-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="79ce0-108"> (否則，它可以是任何 **BSTR** 字串。 ) </span><span class="sxs-lookup"><span data-stu-id="79ce0-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="79ce0-109">語法</span><span class="sxs-lookup"><span data-stu-id="79ce0-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="79ce0-110">參數</span><span class="sxs-lookup"><span data-stu-id="79ce0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79ce0-111">*ppName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="79ce0-111">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79ce0-112">包含會話名稱之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="79ce0-112">Pointer to a **BSTR** containing the session name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79ce0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="79ce0-113">Return value</span></span>

<span data-ttu-id="79ce0-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="79ce0-114">This method can return one of these values.</span></span>



| <span data-ttu-id="79ce0-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="79ce0-115">Return code</span></span>                                                                                   | <span data-ttu-id="79ce0-116">Description</span><span class="sxs-lookup"><span data-stu-id="79ce0-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="79ce0-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="79ce0-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="79ce0-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="79ce0-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="79ce0-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="79ce0-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="79ce0-120">*PpName* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="79ce0-120">The *ppName* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="79ce0-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="79ce0-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="79ce0-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="79ce0-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="79ce0-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="79ce0-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="79ce0-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="79ce0-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="79ce0-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="79ce0-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="79ce0-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="79ce0-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="79ce0-127">備註</span><span class="sxs-lookup"><span data-stu-id="79ce0-127">Remarks</span></span>

<span data-ttu-id="79ce0-128">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppName* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="79ce0-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="79ce0-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="79ce0-129">Requirements</span></span>



| <span data-ttu-id="79ce0-130">需求</span><span class="sxs-lookup"><span data-stu-id="79ce0-130">Requirement</span></span> | <span data-ttu-id="79ce0-131">值</span><span class="sxs-lookup"><span data-stu-id="79ce0-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79ce0-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="79ce0-132">TAPI version</span></span><br/> | <span data-ttu-id="79ce0-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="79ce0-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="79ce0-134">標頭</span><span class="sxs-lookup"><span data-stu-id="79ce0-134">Header</span></span><br/>       | <dl> <span data-ttu-id="79ce0-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="79ce0-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="79ce0-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="79ce0-136">Library</span></span><br/>      | <dl> <span data-ttu-id="79ce0-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="79ce0-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="79ce0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="79ce0-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="79ce0-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79ce0-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79ce0-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79ce0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79ce0-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="79ce0-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="79ce0-142">**ITSdp：:p 的內容 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="79ce0-142">**ITSdp::put\_Name**</span></span>](itsdp-put-name.md)
</dt> </dl>

 

