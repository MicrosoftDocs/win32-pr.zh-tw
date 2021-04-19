---
description: Get \_ TransportProtocol 方法會取得傳輸通訊協定。
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: 'ITMedia：： get_TransportProtocol 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf2bc66a98e181674bbf6f7956579bbaa0b5a72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977602"
---
# <a name="itmediaget_transportprotocol-method"></a><span data-ttu-id="d0825-103">ITMedia：： get \_ TransportProtocol 方法</span><span class="sxs-lookup"><span data-stu-id="d0825-103">ITMedia::get\_TransportProtocol method</span></span>

<span data-ttu-id="d0825-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="d0825-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d0825-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d0825-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d0825-106">**Get \_ TransportProtocol** 方法會取得傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d0825-106">The **get\_TransportProtocol** method gets the transport protocol.</span></span> <span data-ttu-id="d0825-107">除了媒體格式之外，還會指定相同的標準媒體格式，即使網路通訊協定相同（例如，使用 Vat PCM 音訊和 RTP PCM 音訊），相同的標準媒體格式也可能會透過不同的傳輸通訊協定來執行。</span><span class="sxs-lookup"><span data-stu-id="d0825-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0825-108">語法</span><span class="sxs-lookup"><span data-stu-id="d0825-108">Syntax</span></span>


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="d0825-109">參數</span><span class="sxs-lookup"><span data-stu-id="d0825-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0825-110">*ppProtocol* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d0825-110">*ppProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0825-111">傳輸通訊協定之 **BSTR** 表示的指標。</span><span class="sxs-lookup"><span data-stu-id="d0825-111">Pointer to the **BSTR** representation of the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0825-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0825-112">Return value</span></span>

<span data-ttu-id="d0825-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d0825-113">This method can return one of these values.</span></span>



| <span data-ttu-id="d0825-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d0825-114">Return code</span></span>                                                                                   | <span data-ttu-id="d0825-115">Description</span><span class="sxs-lookup"><span data-stu-id="d0825-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d0825-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d0825-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d0825-117">方法成功。</span><span class="sxs-lookup"><span data-stu-id="d0825-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d0825-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d0825-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d0825-119">*PpProtocol* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="d0825-119">The *ppProtocol* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="d0825-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d0825-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d0825-121">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="d0825-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d0825-122"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="d0825-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d0825-123">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0825-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d0825-124"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d0825-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d0825-125">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="d0825-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="d0825-126">備註</span><span class="sxs-lookup"><span data-stu-id="d0825-126">Remarks</span></span>

<span data-ttu-id="d0825-127">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppProtocol* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d0825-127">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppProtocol* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0825-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0825-128">Requirements</span></span>



| <span data-ttu-id="d0825-129">需求</span><span class="sxs-lookup"><span data-stu-id="d0825-129">Requirement</span></span> | <span data-ttu-id="d0825-130">值</span><span class="sxs-lookup"><span data-stu-id="d0825-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0825-131">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="d0825-131">TAPI version</span></span><br/> | <span data-ttu-id="d0825-132">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d0825-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d0825-133">標頭</span><span class="sxs-lookup"><span data-stu-id="d0825-133">Header</span></span><br/>       | <dl> <span data-ttu-id="d0825-134"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0825-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0825-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="d0825-135">Library</span></span><br/>      | <dl> <span data-ttu-id="d0825-136"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="d0825-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d0825-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d0825-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="d0825-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0825-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0825-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0825-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0825-140">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="d0825-140">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="d0825-141">**ITMedia：:p 的 \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="d0825-141">**ITMedia::put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md)
</dt> </dl>

 

