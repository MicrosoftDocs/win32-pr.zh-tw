---
description: 增強影片轉譯器 (EVR) 媒體接收器的自訂影片呈現者 CLSID。
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: 'MF_ACTI加值稅E_CUSTOM_VIDEO_PRESENTER_CLSID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0eb913a56671d5d2ac8d27c785e1cc1fbfc51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981431"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a><span data-ttu-id="178b3-103">MF \_ 啟用 \_ 自訂 \_ 影片展示 \_ 者 \_ CLSID 屬性</span><span class="sxs-lookup"><span data-stu-id="178b3-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID attribute</span></span>

<span data-ttu-id="178b3-104">增強影片轉譯器 (EVR) 媒體接收器的自訂影片呈現者 CLSID。</span><span class="sxs-lookup"><span data-stu-id="178b3-104">CLSID of a custom video presenter for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="178b3-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="178b3-105">Data type</span></span>

<span data-ttu-id="178b3-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="178b3-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="178b3-107">備註</span><span class="sxs-lookup"><span data-stu-id="178b3-107">Remarks</span></span>

<span data-ttu-id="178b3-108">如果您是透過啟用物件建立 EVR，您可以使用這個屬性，在 EVR 上設定自訂的影片展示者。</span><span class="sxs-lookup"><span data-stu-id="178b3-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video presenter on the EVR.</span></span> <span data-ttu-id="178b3-109">使用此屬性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="178b3-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="178b3-110">呼叫 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) 函數，以建立 EVR 的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="178b3-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="178b3-111">函數會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="178b3-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="178b3-112">藉由呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)，在 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="178b3-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="178b3-113">屬性的值是應用程式自訂影片展示者的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="178b3-113">The value of the attribute is the CLSID of the application's custom video presenter.</span></span>

<span data-ttu-id="178b3-114">如果設定此屬性，EVR 就會使用指定的 CLSID 來呼叫 **CoCreateInstance** ，以建立自訂的影片展示者。</span><span class="sxs-lookup"><span data-stu-id="178b3-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video presenter.</span></span> <span data-ttu-id="178b3-115">影片展示者必須公開 [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) 介面。</span><span class="sxs-lookup"><span data-stu-id="178b3-115">The video presenter must expose the [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface.</span></span> <span data-ttu-id="178b3-116">系統會將簡報者建立為同進程 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="178b3-116">The presenter is created as an in-process COM server.</span></span>

<span data-ttu-id="178b3-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="178b3-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="178b3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="178b3-118">Requirements</span></span>



| <span data-ttu-id="178b3-119">需求</span><span class="sxs-lookup"><span data-stu-id="178b3-119">Requirement</span></span> | <span data-ttu-id="178b3-120">值</span><span class="sxs-lookup"><span data-stu-id="178b3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="178b3-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="178b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="178b3-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="178b3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="178b3-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="178b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="178b3-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="178b3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="178b3-125">標頭</span><span class="sxs-lookup"><span data-stu-id="178b3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="178b3-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="178b3-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="178b3-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="178b3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="178b3-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="178b3-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="178b3-129">增強的影片轉譯器屬性</span><span class="sxs-lookup"><span data-stu-id="178b3-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="178b3-130">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="178b3-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="178b3-131">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="178b3-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="178b3-132">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="178b3-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="178b3-133">啟用物件</span><span class="sxs-lookup"><span data-stu-id="178b3-133">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="178b3-134">如何撰寫 EVR 展示者</span><span class="sxs-lookup"><span data-stu-id="178b3-134">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




