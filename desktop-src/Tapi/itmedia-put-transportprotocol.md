---
description: Put \_ TransportProtocol 方法會設定傳輸通訊協定。
ms.assetid: d2f74d4a-a65d-4829-ad17-7548ef06cfeb
title: 'ITMedia：:p ut_TransportProtocol 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6b4228a5d2a6ea49ae3f87b9306ea80e94fc36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990060"
---
# <a name="itmediaput_transportprotocol-method"></a><span data-ttu-id="66c34-103">ITMedia：:p 的 \_ TransportProtocol 方法</span><span class="sxs-lookup"><span data-stu-id="66c34-103">ITMedia::put\_TransportProtocol method</span></span>

<span data-ttu-id="66c34-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="66c34-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="66c34-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="66c34-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="66c34-106">**Put \_ TransportProtocol** 方法會設定傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="66c34-106">The **put\_TransportProtocol** method sets the transport protocol.</span></span> <span data-ttu-id="66c34-107">除了媒體格式之外，還會指定相同的標準媒體格式，即使網路通訊協定相同（例如，使用 Vat PCM 音訊和 RTP PCM 音訊），相同的標準媒體格式也可能會透過不同的傳輸通訊協定來執行。</span><span class="sxs-lookup"><span data-stu-id="66c34-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="66c34-108">語法</span><span class="sxs-lookup"><span data-stu-id="66c34-108">Syntax</span></span>


```C++
HRESULT put_TransportProtocol(
  [in] BSTR pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="66c34-109">參數</span><span class="sxs-lookup"><span data-stu-id="66c34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66c34-110">*pProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66c34-110">*pProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c34-111">包含傳輸通訊協定之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="66c34-111">Pointer to a **BSTR** containing the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66c34-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="66c34-112">Return value</span></span>

<span data-ttu-id="66c34-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="66c34-113">This method can return one of these values.</span></span>



| <span data-ttu-id="66c34-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="66c34-114">Return code</span></span>                                                                                   | <span data-ttu-id="66c34-115">Description</span><span class="sxs-lookup"><span data-stu-id="66c34-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="66c34-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="66c34-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="66c34-117">方法成功。</span><span class="sxs-lookup"><span data-stu-id="66c34-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="66c34-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="66c34-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="66c34-119">*PProtocol* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="66c34-119">The *pProtocol* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="66c34-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="66c34-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="66c34-121">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="66c34-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="66c34-122"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="66c34-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="66c34-123">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="66c34-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="66c34-124"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="66c34-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="66c34-125">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="66c34-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="66c34-126">備註</span><span class="sxs-lookup"><span data-stu-id="66c34-126">Remarks</span></span>

<span data-ttu-id="66c34-127">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pProtocol* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="66c34-127">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pProtocol* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="66c34-128">此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="66c34-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="66c34-129">使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="66c34-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="66c34-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="66c34-130">Requirements</span></span>



| <span data-ttu-id="66c34-131">需求</span><span class="sxs-lookup"><span data-stu-id="66c34-131">Requirement</span></span> | <span data-ttu-id="66c34-132">值</span><span class="sxs-lookup"><span data-stu-id="66c34-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66c34-133">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="66c34-133">TAPI version</span></span><br/> | <span data-ttu-id="66c34-134">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="66c34-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="66c34-135">標頭</span><span class="sxs-lookup"><span data-stu-id="66c34-135">Header</span></span><br/>       | <dl> <span data-ttu-id="66c34-136"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="66c34-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="66c34-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="66c34-137">Library</span></span><br/>      | <dl> <span data-ttu-id="66c34-138"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="66c34-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="66c34-139">DLL</span><span class="sxs-lookup"><span data-stu-id="66c34-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="66c34-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66c34-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66c34-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66c34-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c34-142">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="66c34-142">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="66c34-143">**ITMedia：： get \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="66c34-143">**ITMedia::get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md)
</dt> </dl>

 

