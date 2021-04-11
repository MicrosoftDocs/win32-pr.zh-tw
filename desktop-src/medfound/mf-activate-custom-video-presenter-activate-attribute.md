---
description: 指定啟用物件，此物件會為增強的影片轉譯器 (EVR) 媒體接收器，建立自訂的影片呈現者。
ms.assetid: 65d88832-0969-4d85-bee2-fd0aa68e9f3b
title: 'MF_ACTI加值稅E_CUSTOM_VIDEO_PRESENTER_ACTI加值稅E 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75855c18faba8568547f9efcfb19e04574c4885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318819"
---
# <a name="mf_activate_custom_video_presenter_activate-attribute"></a><span data-ttu-id="ddd92-103">MF \_ 啟用 \_ 自訂 \_ 影片展示 \_ 者 \_ 啟用屬性</span><span class="sxs-lookup"><span data-stu-id="ddd92-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_ACTIVATE attribute</span></span>

<span data-ttu-id="ddd92-104">指定啟用物件，此物件會為增強的影片轉譯器 (EVR) 媒體接收器，建立自訂的影片呈現者。</span><span class="sxs-lookup"><span data-stu-id="ddd92-104">Specifies an activation object that creates a custom video presenter for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="ddd92-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ddd92-105">Data type</span></span>

<span data-ttu-id="ddd92-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="ddd92-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="ddd92-107">備註</span><span class="sxs-lookup"><span data-stu-id="ddd92-107">Remarks</span></span>

<span data-ttu-id="ddd92-108">如果您是透過啟用物件建立 EVR，您可以使用這個屬性，在 EVR 上設定自訂的影片展示者。</span><span class="sxs-lookup"><span data-stu-id="ddd92-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video presenter on the EVR.</span></span> <span data-ttu-id="ddd92-109">使用此屬性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ddd92-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="ddd92-110">呼叫 [_ *MFCreateVideoRendererActivate* \*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate)函式來建立 EVR 的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="ddd92-110">Call the [_ *MFCreateVideoRendererActivate*\*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="ddd92-111">函數會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ddd92-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="ddd92-112">藉由呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)，在 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="ddd92-112">Set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span> <span data-ttu-id="ddd92-113">屬性（attribute）的值（attribute）是呼叫端所執行之啟用物件的指標。</span><span class="sxs-lookup"><span data-stu-id="ddd92-113">The value of the attribute is a pointer to an activation object implemented by the caller.</span></span> <span data-ttu-id="ddd92-114">呼叫端的啟用物件必須公開 **IMFActivate** 介面。</span><span class="sxs-lookup"><span data-stu-id="ddd92-114">The caller's activation object must expose the **IMFActivate** interface.</span></span>

<span data-ttu-id="ddd92-115">如果設定此屬性，EVR 會呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 來建立自訂的影片展示者。</span><span class="sxs-lookup"><span data-stu-id="ddd92-115">If you set this attribute, the EVR calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the custom video presenter.</span></span> <span data-ttu-id="ddd92-116">影片展示者必須公開 [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) 介面。</span><span class="sxs-lookup"><span data-stu-id="ddd92-116">The video presenter must expose the [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface.</span></span>

<span data-ttu-id="ddd92-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="ddd92-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddd92-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ddd92-118">Requirements</span></span>



| <span data-ttu-id="ddd92-119">需求</span><span class="sxs-lookup"><span data-stu-id="ddd92-119">Requirement</span></span> | <span data-ttu-id="ddd92-120">值</span><span class="sxs-lookup"><span data-stu-id="ddd92-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd92-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ddd92-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd92-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ddd92-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ddd92-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ddd92-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd92-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ddd92-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ddd92-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ddd92-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddd92-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ddd92-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddd92-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ddd92-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddd92-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ddd92-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ddd92-129">增強的影片轉譯器屬性</span><span class="sxs-lookup"><span data-stu-id="ddd92-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ddd92-130">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="ddd92-130">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="ddd92-131">**IMFAttributes：： SetUnknown**</span><span class="sxs-lookup"><span data-stu-id="ddd92-131">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="ddd92-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="ddd92-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="ddd92-133">啟用物件</span><span class="sxs-lookup"><span data-stu-id="ddd92-133">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="ddd92-134">如何撰寫 EVR 展示者</span><span class="sxs-lookup"><span data-stu-id="ddd92-134">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




