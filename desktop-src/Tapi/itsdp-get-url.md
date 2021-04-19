---
description: Get \_ url 方法會取得 url。
ms.assetid: 9ea2ddf6-b8c7-4bfa-aab3-ff2d2056837f
title: 'ITSdp：： get_Url 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a207c158d405ac0931e42aa19995d1d4b3078fd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991053"
---
# <a name="itsdpget_url-method"></a><span data-ttu-id="cad75-103">ITSdp：： get \_ Url 方法</span><span class="sxs-lookup"><span data-stu-id="cad75-103">ITSdp::get\_Url method</span></span>

<span data-ttu-id="cad75-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="cad75-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cad75-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="cad75-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cad75-106">**Get \_ url** 方法會取得 url。</span><span class="sxs-lookup"><span data-stu-id="cad75-106">The **get\_Url** method gets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad75-107">語法</span><span class="sxs-lookup"><span data-stu-id="cad75-107">Syntax</span></span>


```C++
HRESULT get_Url(
  [out] BSTR *ppUrl
);
```



## <a name="parameters"></a><span data-ttu-id="cad75-108">參數</span><span class="sxs-lookup"><span data-stu-id="cad75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cad75-109">*ppUrl* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cad75-109">*ppUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cad75-110">URL 之 **BSTR** 表示的指標。</span><span class="sxs-lookup"><span data-stu-id="cad75-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cad75-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cad75-111">Return value</span></span>

<span data-ttu-id="cad75-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cad75-112">This method can return one of these values.</span></span>



| <span data-ttu-id="cad75-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cad75-113">Return code</span></span>                                                                                   | <span data-ttu-id="cad75-114">Description</span><span class="sxs-lookup"><span data-stu-id="cad75-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cad75-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cad75-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cad75-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="cad75-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cad75-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="cad75-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cad75-118">*PpUrl* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="cad75-118">The *ppUrl* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="cad75-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cad75-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cad75-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="cad75-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="cad75-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="cad75-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cad75-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cad75-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="cad75-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="cad75-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="cad75-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="cad75-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="cad75-125">備註</span><span class="sxs-lookup"><span data-stu-id="cad75-125">Remarks</span></span>

<span data-ttu-id="cad75-126">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppUrl* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="cad75-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppUrl* parameter.</span></span>

<span data-ttu-id="cad75-127">URL 通常用來參考包含其他資源的網頁或有關會議的背景資訊。</span><span class="sxs-lookup"><span data-stu-id="cad75-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

## <a name="requirements"></a><span data-ttu-id="cad75-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="cad75-128">Requirements</span></span>



| <span data-ttu-id="cad75-129">需求</span><span class="sxs-lookup"><span data-stu-id="cad75-129">Requirement</span></span> | <span data-ttu-id="cad75-130">值</span><span class="sxs-lookup"><span data-stu-id="cad75-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cad75-131">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="cad75-131">TAPI version</span></span><br/> | <span data-ttu-id="cad75-132">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="cad75-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cad75-133">標頭</span><span class="sxs-lookup"><span data-stu-id="cad75-133">Header</span></span><br/>       | <dl> <span data-ttu-id="cad75-134"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="cad75-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cad75-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="cad75-135">Library</span></span><br/>      | <dl> <span data-ttu-id="cad75-136"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="cad75-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cad75-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cad75-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="cad75-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cad75-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cad75-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cad75-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad75-140">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="cad75-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="cad75-141">**ITSdp：:p 的內容 \_ Url**</span><span class="sxs-lookup"><span data-stu-id="cad75-141">**ITSdp::put\_Url**</span></span>](itsdp-put-url.md)
</dt> </dl>

 

