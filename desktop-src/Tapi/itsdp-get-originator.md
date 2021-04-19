---
description: 取得建立者方法會取得會議製作者 \_ 。
ms.assetid: a324098d-ae22-42e9-901e-b277433af199
title: 'ITSdp：： get_Originator 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f751dd5a9dffe2d3bbc7883b8a0f8f18f8e6381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999169"
---
# <a name="itsdpget_originator-method"></a><span data-ttu-id="a073b-103">ITSdp：：取得建立者 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="a073b-103">ITSdp::get\_Originator method</span></span>

<span data-ttu-id="a073b-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="a073b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a073b-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="a073b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a073b-106">取得建立者方法會取得會議製作者。 **\_**</span><span class="sxs-lookup"><span data-stu-id="a073b-106">The **get\_Originator** method gets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="a073b-107">語法</span><span class="sxs-lookup"><span data-stu-id="a073b-107">Syntax</span></span>


```C++
HRESULT get_Originator(
  [out] BSTR *ppOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="a073b-108">參數</span><span class="sxs-lookup"><span data-stu-id="a073b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a073b-109">*ppOriginator* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a073b-109">*ppOriginator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a073b-110">會議建立者之 **BSTR** 表示的指標。</span><span class="sxs-lookup"><span data-stu-id="a073b-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a073b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a073b-111">Return value</span></span>

<span data-ttu-id="a073b-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a073b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a073b-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a073b-113">Return code</span></span>                                                                                   | <span data-ttu-id="a073b-114">Description</span><span class="sxs-lookup"><span data-stu-id="a073b-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a073b-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a073b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a073b-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="a073b-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a073b-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="a073b-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a073b-118">*PpOriginator* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="a073b-118">The *ppOriginator* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="a073b-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a073b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a073b-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="a073b-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a073b-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="a073b-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a073b-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a073b-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a073b-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a073b-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a073b-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="a073b-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a073b-125">備註</span><span class="sxs-lookup"><span data-stu-id="a073b-125">Remarks</span></span>

<span data-ttu-id="a073b-126">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppOriginator* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a073b-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppOriginator* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a073b-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a073b-127">Requirements</span></span>



| <span data-ttu-id="a073b-128">需求</span><span class="sxs-lookup"><span data-stu-id="a073b-128">Requirement</span></span> | <span data-ttu-id="a073b-129">值</span><span class="sxs-lookup"><span data-stu-id="a073b-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a073b-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="a073b-130">TAPI version</span></span><br/> | <span data-ttu-id="a073b-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a073b-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a073b-132">標頭</span><span class="sxs-lookup"><span data-stu-id="a073b-132">Header</span></span><br/>       | <dl> <span data-ttu-id="a073b-133"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="a073b-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a073b-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="a073b-134">Library</span></span><br/>      | <dl> <span data-ttu-id="a073b-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="a073b-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a073b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a073b-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="a073b-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a073b-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a073b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a073b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a073b-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="a073b-139">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="a073b-140">**ITSdp：:p 的等 \_ 人**</span><span class="sxs-lookup"><span data-stu-id="a073b-140">**ITSdp::put\_Originator**</span></span>](itsdp-put-originator.md)
</dt> </dl>

 

