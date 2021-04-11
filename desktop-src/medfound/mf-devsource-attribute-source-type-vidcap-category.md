---
description: 指定影片捕獲裝置的裝置類別。
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: 'MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc65af267df38486f6ad7859d16aff4de5973a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113669"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a><span data-ttu-id="fd594-103">MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 類別目錄屬性</span><span class="sxs-lookup"><span data-stu-id="fd594-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_CATEGORY attribute</span></span>

<span data-ttu-id="fd594-104">指定影片捕獲裝置的裝置類別。</span><span class="sxs-lookup"><span data-stu-id="fd594-104">Specifies the device category for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd594-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="fd594-105">Data type</span></span>

<span data-ttu-id="fd594-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="fd594-106">**GUID**</span></span>

<span data-ttu-id="fd594-107">已定義下列值。</span><span class="sxs-lookup"><span data-stu-id="fd594-107">The following value is defined.</span></span>



| <span data-ttu-id="fd594-108">值</span><span class="sxs-lookup"><span data-stu-id="fd594-108">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="fd594-109">意義</span><span class="sxs-lookup"><span data-stu-id="fd594-109">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <span data-ttu-id="fd594-110"><dt>**CLSID \_ VideoInputDeviceCategory**</dt></span><span class="sxs-lookup"><span data-stu-id="fd594-110"><dt>**CLSID\_VideoInputDeviceCategory**</dt></span></span> </dl> | <span data-ttu-id="fd594-111">影片捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="fd594-111">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="fd594-112">取得/設定</span><span class="sxs-lookup"><span data-stu-id="fd594-112">Get/set</span></span>

<span data-ttu-id="fd594-113">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)。</span><span class="sxs-lookup"><span data-stu-id="fd594-113">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="fd594-114">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)。</span><span class="sxs-lookup"><span data-stu-id="fd594-114">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd594-115">備註</span><span class="sxs-lookup"><span data-stu-id="fd594-115">Remarks</span></span>

<span data-ttu-id="fd594-116">列舉影片捕獲裝置時，請使用這個屬性做為 [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) 函數的輸入。</span><span class="sxs-lookup"><span data-stu-id="fd594-116">Use this attribute as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function when enumerating video capture devices.</span></span>

<span data-ttu-id="fd594-117">此外，此屬性是在下列函式所傳回的啟用物件上設定：</span><span class="sxs-lookup"><span data-stu-id="fd594-117">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="fd594-118">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="fd594-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="fd594-119">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="fd594-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="fd594-120">屬性只適用于影片捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="fd594-120">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="fd594-121">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="fd594-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd594-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd594-122">Requirements</span></span>



| <span data-ttu-id="fd594-123">需求</span><span class="sxs-lookup"><span data-stu-id="fd594-123">Requirement</span></span> | <span data-ttu-id="fd594-124">值</span><span class="sxs-lookup"><span data-stu-id="fd594-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd594-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd594-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fd594-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd594-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fd594-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd594-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fd594-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd594-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="fd594-129">標頭</span><span class="sxs-lookup"><span data-stu-id="fd594-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd594-130"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd594-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd594-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd594-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd594-132">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="fd594-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd594-133">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="fd594-133">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="fd594-134">捕獲裝置屬性</span><span class="sxs-lookup"><span data-stu-id="fd594-134">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




