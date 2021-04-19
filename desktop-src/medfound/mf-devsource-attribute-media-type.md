---
description: 指定裝置的輸出格式。
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: 'MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05283f33fa3b3bf4b9e339b830c2ae6a948ea82
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "107000348"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a><span data-ttu-id="e74d1-103">MF \_ DEVSOURCE \_ 屬性 \_ 媒體 \_ 類型屬性</span><span class="sxs-lookup"><span data-stu-id="e74d1-103">MF\_DEVSOURCE\_ATTRIBUTE\_MEDIA\_TYPE attribute</span></span>

<span data-ttu-id="e74d1-104">指定裝置的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="e74d1-104">Specifies the output format of a device.</span></span>

## <a name="data-type"></a><span data-ttu-id="e74d1-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e74d1-105">Data type</span></span>

<span data-ttu-id="e74d1-106">**[**MFT \_儲存 \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** 為 **位元組 \[ 的 \]** 註冊類型資訊</span><span class="sxs-lookup"><span data-stu-id="e74d1-106">**[**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="e74d1-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="e74d1-107">Get/set</span></span>

<span data-ttu-id="e74d1-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。</span><span class="sxs-lookup"><span data-stu-id="e74d1-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="e74d1-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。</span><span class="sxs-lookup"><span data-stu-id="e74d1-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="e74d1-110">備註</span><span class="sxs-lookup"><span data-stu-id="e74d1-110">Remarks</span></span>

<span data-ttu-id="e74d1-111">此屬性包含一對 Guid：主要類型和子類型。</span><span class="sxs-lookup"><span data-stu-id="e74d1-111">This attribute contains a pair of GUIDs: a major type and a subtype.</span></span> <span data-ttu-id="e74d1-112">這些 Guid 描述裝置的預設輸出格式。</span><span class="sxs-lookup"><span data-stu-id="e74d1-112">These GUIDs describe the default output format of the device.</span></span> <span data-ttu-id="e74d1-113">裝置可能會支援其他輸出格式。</span><span class="sxs-lookup"><span data-stu-id="e74d1-113">The device might support additional output formats.</span></span>

<span data-ttu-id="e74d1-114">例如，如果影片捕獲裝置輸出 RGB-32 影片，則此屬性的值為 `{ MFMediaType_Video, MFVideoFormat_RGB32 }` 。</span><span class="sxs-lookup"><span data-stu-id="e74d1-114">For example, if a video capture device outputs RGB-32 video, the value of this attribute is `{ MFMediaType_Video, MFVideoFormat_RGB32 }`.</span></span>

<span data-ttu-id="e74d1-115">這個屬性是應用程式的提示。</span><span class="sxs-lookup"><span data-stu-id="e74d1-115">This attribute is a hint to the application.</span></span> <span data-ttu-id="e74d1-116">若要取得確切的輸出格式，請建立裝置的媒體來源，並取得媒體來源的展示描述項。</span><span class="sxs-lookup"><span data-stu-id="e74d1-116">To get the exact output format, create the media source for the device and get the media source's presentation descriptor.</span></span>

<span data-ttu-id="e74d1-117">這個屬性是在下列函式所傳回的啟用物件上設定：</span><span class="sxs-lookup"><span data-stu-id="e74d1-117">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="e74d1-118">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="e74d1-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="e74d1-119">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="e74d1-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="e74d1-120">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e74d1-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e74d1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e74d1-121">Requirements</span></span>



| <span data-ttu-id="e74d1-122">需求</span><span class="sxs-lookup"><span data-stu-id="e74d1-122">Requirement</span></span> | <span data-ttu-id="e74d1-123">值</span><span class="sxs-lookup"><span data-stu-id="e74d1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e74d1-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e74d1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e74d1-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e74d1-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e74d1-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e74d1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e74d1-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e74d1-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e74d1-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e74d1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e74d1-129"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e74d1-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e74d1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e74d1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e74d1-131">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e74d1-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e74d1-132">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="e74d1-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="e74d1-133">捕獲裝置屬性</span><span class="sxs-lookup"><span data-stu-id="e74d1-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




