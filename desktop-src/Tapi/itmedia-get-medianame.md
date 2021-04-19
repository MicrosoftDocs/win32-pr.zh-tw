---
description: Get \_ MediaName 方法會取得媒體名稱。 定義的媒體包括音訊、影片、白板、文字和資料。
ms.assetid: 4afb24f9-582e-420d-8bda-772a3dc4d96c
title: 'ITMedia：： get_MediaName 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9152994eac98d5e846ac147072a51a3334930da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000957"
---
# <a name="itmediaget_medianame-method"></a><span data-ttu-id="ff024-104">ITMedia：： get \_ MediaName 方法</span><span class="sxs-lookup"><span data-stu-id="ff024-104">ITMedia::get\_MediaName method</span></span>

<span data-ttu-id="ff024-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="ff024-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ff024-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ff024-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ff024-107">**Get \_ MediaName** 方法會取得媒體名稱。</span><span class="sxs-lookup"><span data-stu-id="ff024-107">The **get\_MediaName** method gets the media name.</span></span> <span data-ttu-id="ff024-108">定義的媒體包括音訊、影片、白板、文字和資料。</span><span class="sxs-lookup"><span data-stu-id="ff024-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff024-109">語法</span><span class="sxs-lookup"><span data-stu-id="ff024-109">Syntax</span></span>


```C++
HRESULT get_MediaName(
  [out] BSTR *ppMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="ff024-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff024-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff024-111">*ppMediaName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ff024-111">*ppMediaName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff024-112">包含媒體名稱之 **BSTR** 的指標，例如音訊。</span><span class="sxs-lookup"><span data-stu-id="ff024-112">Pointer to a **BSTR** containing the name of the media, such as audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff024-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff024-113">Return value</span></span>

<span data-ttu-id="ff024-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ff024-114">This method can return one of these values.</span></span>



| <span data-ttu-id="ff024-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ff024-115">Return code</span></span>                                                                                   | <span data-ttu-id="ff024-116">Description</span><span class="sxs-lookup"><span data-stu-id="ff024-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ff024-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ff024-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ff024-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="ff024-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ff024-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="ff024-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ff024-120">*PpMediaName* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="ff024-120">The *ppMediaName* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="ff024-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ff024-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ff024-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="ff024-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ff024-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="ff024-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ff024-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ff024-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ff024-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="ff024-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ff024-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="ff024-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="ff024-127">備註</span><span class="sxs-lookup"><span data-stu-id="ff024-127">Remarks</span></span>

<span data-ttu-id="ff024-128">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppMediaName* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ff024-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMediaName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff024-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff024-129">Requirements</span></span>



| <span data-ttu-id="ff024-130">需求</span><span class="sxs-lookup"><span data-stu-id="ff024-130">Requirement</span></span> | <span data-ttu-id="ff024-131">值</span><span class="sxs-lookup"><span data-stu-id="ff024-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff024-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ff024-132">TAPI version</span></span><br/> | <span data-ttu-id="ff024-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ff024-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ff024-134">標頭</span><span class="sxs-lookup"><span data-stu-id="ff024-134">Header</span></span><br/>       | <dl> <span data-ttu-id="ff024-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff024-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff024-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="ff024-136">Library</span></span><br/>      | <dl> <span data-ttu-id="ff024-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="ff024-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ff024-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ff024-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="ff024-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff024-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff024-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff024-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff024-141">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="ff024-141">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="ff024-142">**ITMedia：:p 的 \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="ff024-142">**ITMedia::put\_MediaName**</span></span>](itmedia-put-medianame.md)
</dt> </dl>

 

