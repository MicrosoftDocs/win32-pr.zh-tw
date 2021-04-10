---
description: 指定如何建立增強型影片轉譯器 (EVR) 的自訂展示者。
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: 'MF_ACTI加值稅E_CUSTOM_VIDEO_PRESENTER_FLAGS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3681edaed39b63b0f7c13313039f1c6e72311a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027067"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a><span data-ttu-id="3bc05-103">MF \_ 啟用 \_ 自訂 \_ 影片展示 \_ 者 \_ 旗標屬性</span><span class="sxs-lookup"><span data-stu-id="3bc05-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_FLAGS attribute</span></span>

<span data-ttu-id="3bc05-104">指定如何建立增強型影片轉譯器 (EVR) 的自訂展示者。</span><span class="sxs-lookup"><span data-stu-id="3bc05-104">Specifies how to create a custom presenter for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="3bc05-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3bc05-105">Data type</span></span>

<span data-ttu-id="3bc05-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3bc05-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3bc05-107">備註</span><span class="sxs-lookup"><span data-stu-id="3bc05-107">Remarks</span></span>

<span data-ttu-id="3bc05-108">您可以在從 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate)函數取得的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="3bc05-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="3bc05-109">這個屬性的值是下列值的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="3bc05-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="3bc05-110">值</span><span class="sxs-lookup"><span data-stu-id="3bc05-110">Value</span></span>                                          | <span data-ttu-id="3bc05-111">描述</span><span class="sxs-lookup"><span data-stu-id="3bc05-111">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc05-112">**MF \_ 啟用 \_ 自訂展示 \_ 者 \_ ALLOWFAIL**</span><span class="sxs-lookup"><span data-stu-id="3bc05-112">**MF\_ACTIVATE\_CUSTOM\_PRESENTER\_ALLOWFAIL**</span></span> | <span data-ttu-id="3bc05-113">如果 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 方法無法建立應用程式的自訂展示者，則會改為使用預設的 EVR 展示者。</span><span class="sxs-lookup"><span data-stu-id="3bc05-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom presenter, it uses the default EVR presenter instead.</span></span> <span data-ttu-id="3bc05-114">根據預設，如果 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 物件嘗試建立自訂的簡報者時失敗， **ActivateObject** 方法就會失敗。</span><span class="sxs-lookup"><span data-stu-id="3bc05-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom presenter, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="3bc05-115">應用程式可以使用 [ [**MF \_ 啟用 \_ 自訂 \_ 影片展示 \_ 者 \_ CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md) ] 屬性來指定 EVR 的自訂展示者。</span><span class="sxs-lookup"><span data-stu-id="3bc05-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md) attribute to specify a custom presenter for the EVR.</span></span>

<span data-ttu-id="3bc05-116">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="3bc05-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc05-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bc05-117">Requirements</span></span>



| <span data-ttu-id="3bc05-118">需求</span><span class="sxs-lookup"><span data-stu-id="3bc05-118">Requirement</span></span> | <span data-ttu-id="3bc05-119">值</span><span class="sxs-lookup"><span data-stu-id="3bc05-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc05-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bc05-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3bc05-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bc05-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3bc05-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bc05-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3bc05-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bc05-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3bc05-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3bc05-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bc05-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3bc05-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bc05-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bc05-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc05-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3bc05-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3bc05-128">增強的影片轉譯器屬性</span><span class="sxs-lookup"><span data-stu-id="3bc05-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="3bc05-129">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3bc05-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3bc05-130">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3bc05-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3bc05-131">啟用物件</span><span class="sxs-lookup"><span data-stu-id="3bc05-131">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="3bc05-132">如何撰寫 EVR 展示者</span><span class="sxs-lookup"><span data-stu-id="3bc05-132">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




