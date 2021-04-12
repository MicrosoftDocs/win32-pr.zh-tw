---
description: 設定在來源解析期間建立 PMP 媒體會話的回呼。
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: 'MFPKEY_PMP_Creation_Callback 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192246"
---
# <a name="mfpkey_pmp_creation_callback-property"></a><span data-ttu-id="66e9d-103">MFPKEY \_ PMP \_ 建立 \_ 回呼屬性</span><span class="sxs-lookup"><span data-stu-id="66e9d-103">MFPKEY\_PMP\_Creation\_Callback property</span></span>

<span data-ttu-id="66e9d-104">設定在來源解析期間建立 [PMP 媒體會話](pmp-media-session.md) 的回呼。</span><span class="sxs-lookup"><span data-stu-id="66e9d-104">Sets a callback that creates the [PMP Media Session](pmp-media-session.md) during source resolution.</span></span>



<span data-ttu-id="66e9d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="66e9d-105">Data type</span></span>

<span data-ttu-id="66e9d-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="66e9d-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="66e9d-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="66e9d-107">PROPVARIANT member</span></span>

<span data-ttu-id="66e9d-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="66e9d-108">\**IUnknown\** _</span></span>

<span data-ttu-id="66e9d-109">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="66e9d-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="66e9d-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="66e9d-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="66e9d-111">備註</span><span class="sxs-lookup"><span data-stu-id="66e9d-111">Remarks</span></span>

<span data-ttu-id="66e9d-112">某些受保護的內容可能需要使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="66e9d-112">Some protected content might require the use of this property.</span></span> <span data-ttu-id="66e9d-113">如果是，來源解析程式會失敗，並出現錯誤碼 **MF \_ E \_ 解析度 \_ 需要 \_ PMP \_ 建立 \_ 回呼**。</span><span class="sxs-lookup"><span data-stu-id="66e9d-113">If so, the source resolution process fails with the error code **MF\_E\_RESOLUTION\_REQUIRES\_PMP\_CREATION\_CALLBACK**.</span></span>

<span data-ttu-id="66e9d-114">若要使用這個屬性，請執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="66e9d-114">To use this property, do the following.</span></span>

1.  <span data-ttu-id="66e9d-115">呼叫 [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) 以建立屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="66e9d-115">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a property store.</span></span>
2.  <span data-ttu-id="66e9d-116">執行 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 回呼介面。</span><span class="sxs-lookup"><span data-stu-id="66e9d-116">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback interface.</span></span>
3.  <span data-ttu-id="66e9d-117">在 \_ \_ \_ 屬性存放區上設定 MFPKEY PMP 建立回呼屬性。</span><span class="sxs-lookup"><span data-stu-id="66e9d-117">Set the MFPKEY\_PMP\_Creation\_Callback property on the property store.</span></span> <span data-ttu-id="66e9d-118">值是 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 執行的指標。</span><span class="sxs-lookup"><span data-stu-id="66e9d-118">The value is a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) implementation.</span></span>
4.  <span data-ttu-id="66e9d-119">呼叫 [**IMFSourceResolver：： BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)。</span><span class="sxs-lookup"><span data-stu-id="66e9d-119">Call [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span> <span data-ttu-id="66e9d-120">將指標傳入 *pProps* 參數中的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="66e9d-120">Pass in a pointer to the property store in the *pProps* parameter.</span></span>

<span data-ttu-id="66e9d-121">在回呼介面的 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法中，執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="66e9d-121">In the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of your callback interface, do the following.</span></span>

1.  <span data-ttu-id="66e9d-122">呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) 來建立 [PMP 媒體會話](pmp-media-session.md)。</span><span class="sxs-lookup"><span data-stu-id="66e9d-122">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the [PMP Media Session](pmp-media-session.md).</span></span>
2.  <span data-ttu-id="66e9d-123">將 PMP 媒體會話上的 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 呼叫至 [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="66e9d-123">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the PMP Media Session to a pointer to the [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) interface.</span></span>
3.  <span data-ttu-id="66e9d-124">針對在 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)的 *pAsyncResult* 參數中傳遞的結果物件，呼叫 [**IMFAsyncResult：： >getstate**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) 。</span><span class="sxs-lookup"><span data-stu-id="66e9d-124">Call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) on the result object that is passed in the *pAsyncResult* parameter of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="66e9d-125">查詢傳回的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標以取得 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="66e9d-125">Query the returned [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer for the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
4.  <span data-ttu-id="66e9d-126">使用下列參數呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) ：</span><span class="sxs-lookup"><span data-stu-id="66e9d-126">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) with the following parameters:</span></span>
    -   <span data-ttu-id="66e9d-127">*dwQueue*： **MFASYNC \_ 回呼 \_ 佇列 \_ 標準**</span><span class="sxs-lookup"><span data-stu-id="66e9d-127">*dwQueue*: **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**</span></span>
    -   <span data-ttu-id="66e9d-128">*pCallback*：在步驟3中取得的 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 指標。</span><span class="sxs-lookup"><span data-stu-id="66e9d-128">*pCallback*: The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) pointer obtained in step 3.</span></span>
    -   <span data-ttu-id="66e9d-129">*pState*：在步驟2中取得的 [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) 指標。</span><span class="sxs-lookup"><span data-stu-id="66e9d-129">*pState*: The [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) pointer obtained in step 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e9d-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="66e9d-130">Requirements</span></span>



| <span data-ttu-id="66e9d-131">需求</span><span class="sxs-lookup"><span data-stu-id="66e9d-131">Requirement</span></span> | <span data-ttu-id="66e9d-132">值</span><span class="sxs-lookup"><span data-stu-id="66e9d-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66e9d-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66e9d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="66e9d-134">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66e9d-134">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="66e9d-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66e9d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="66e9d-136">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66e9d-136">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="66e9d-137">標頭</span><span class="sxs-lookup"><span data-stu-id="66e9d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="66e9d-138"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="66e9d-138"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e9d-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66e9d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e9d-140">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="66e9d-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="66e9d-141">PMP 媒體會話</span><span class="sxs-lookup"><span data-stu-id="66e9d-141">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="66e9d-142">受保護的媒體路徑</span><span class="sxs-lookup"><span data-stu-id="66e9d-142">Protected Media Path</span></span>](protected-media-path.md)
</dt> <dt>

[<span data-ttu-id="66e9d-143">來源解析程式</span><span class="sxs-lookup"><span data-stu-id="66e9d-143">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
