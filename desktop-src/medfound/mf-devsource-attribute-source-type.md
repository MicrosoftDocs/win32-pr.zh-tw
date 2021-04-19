---
description: 指定裝置類型，例如音訊捕獲或影片捕獲。
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: 'MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977021"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a><span data-ttu-id="fe5ed-103">MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型屬性</span><span class="sxs-lookup"><span data-stu-id="fe5ed-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE attribute</span></span>

<span data-ttu-id="fe5ed-104">指定裝置的類型，例如音訊捕獲或影片捕獲。</span><span class="sxs-lookup"><span data-stu-id="fe5ed-104">Specifies a device's type, such as audio capture or video capture.</span></span>

## <a name="data-type"></a><span data-ttu-id="fe5ed-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="fe5ed-105">Data type</span></span>

<span data-ttu-id="fe5ed-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="fe5ed-106">**GUID**</span></span>

<span data-ttu-id="fe5ed-107">這個屬性會定義下列值：</span><span class="sxs-lookup"><span data-stu-id="fe5ed-107">The following values are defined for this attribute:</span></span>



| <span data-ttu-id="fe5ed-108">值</span><span class="sxs-lookup"><span data-stu-id="fe5ed-108">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="fe5ed-109">意義</span><span class="sxs-lookup"><span data-stu-id="fe5ed-109">Meaning</span></span>                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <span data-ttu-id="fe5ed-110"><dt>**MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5ed-110"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="fe5ed-111">音訊捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="fe5ed-111">Audio capture device.</span></span><br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <span data-ttu-id="fe5ed-112"><dt>**MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5ed-112"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="fe5ed-113">影片捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="fe5ed-113">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="fe5ed-114">取得/設定</span><span class="sxs-lookup"><span data-stu-id="fe5ed-114">Get/set</span></span>

<span data-ttu-id="fe5ed-115">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)。</span><span class="sxs-lookup"><span data-stu-id="fe5ed-115">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="fe5ed-116">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)。</span><span class="sxs-lookup"><span data-stu-id="fe5ed-116">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe5ed-117">備註</span><span class="sxs-lookup"><span data-stu-id="fe5ed-117">Remarks</span></span>

<span data-ttu-id="fe5ed-118">使用此屬性作為下列函式的輸入：</span><span class="sxs-lookup"><span data-stu-id="fe5ed-118">Use this attribute as input to the following functions:</span></span>

-   [<span data-ttu-id="fe5ed-119">**MFCreateDeviceSource**</span><span class="sxs-lookup"><span data-stu-id="fe5ed-119">**MFCreateDeviceSource**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [<span data-ttu-id="fe5ed-120">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="fe5ed-120">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="fe5ed-121">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="fe5ed-121">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="fe5ed-122">此外，這個屬性是在 [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) 函式所傳回的啟用物件上設定的。</span><span class="sxs-lookup"><span data-stu-id="fe5ed-122">In addition, this attribute is set on the activation objects returned by the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span>

<span data-ttu-id="fe5ed-123">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="fe5ed-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe5ed-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe5ed-124">Requirements</span></span>



| <span data-ttu-id="fe5ed-125">需求</span><span class="sxs-lookup"><span data-stu-id="fe5ed-125">Requirement</span></span> | <span data-ttu-id="fe5ed-126">值</span><span class="sxs-lookup"><span data-stu-id="fe5ed-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe5ed-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe5ed-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fe5ed-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe5ed-128">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fe5ed-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe5ed-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fe5ed-130">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe5ed-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="fe5ed-131">標頭</span><span class="sxs-lookup"><span data-stu-id="fe5ed-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe5ed-132"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe5ed-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe5ed-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe5ed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe5ed-134">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="fe5ed-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe5ed-135">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="fe5ed-135">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="fe5ed-136">捕獲裝置屬性</span><span class="sxs-lookup"><span data-stu-id="fe5ed-136">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




