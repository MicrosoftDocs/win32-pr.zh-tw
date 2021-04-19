---
description: 指定影片捕獲來源是否為硬體裝置或軟體裝置。
ms.assetid: 4a886124-54f1-4cd1-a22b-552e8c8d556f
title: 'MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e816e668267a23e67e7450b81a32cde454315bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971708"
---
# <a name="mf_devsource_attribute_source_type_vidcap_hw_source-attribute"></a><span data-ttu-id="4feda-103">MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ HW \_ 來源屬性</span><span class="sxs-lookup"><span data-stu-id="4feda-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_HW\_SOURCE attribute</span></span>

<span data-ttu-id="4feda-104">指定影片捕獲來源是否為硬體裝置或軟體裝置。</span><span class="sxs-lookup"><span data-stu-id="4feda-104">Specifies whether a video capture source is a hardware device or a software device.</span></span>

## <a name="data-type"></a><span data-ttu-id="4feda-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4feda-105">Data type</span></span>

<span data-ttu-id="4feda-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4feda-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="4feda-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="4feda-107">Get/set</span></span>

<span data-ttu-id="4feda-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="4feda-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4feda-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="4feda-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="4feda-110">備註</span><span class="sxs-lookup"><span data-stu-id="4feda-110">Remarks</span></span>

<span data-ttu-id="4feda-111">如果值為 **TRUE**，則表示捕獲來源是硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="4feda-111">If the value is **TRUE**, the capture source is a hardware device.</span></span> <span data-ttu-id="4feda-112">如果值為 **FALSE**，則為軟體裝置。</span><span class="sxs-lookup"><span data-stu-id="4feda-112">If the value is **FALSE**, it is a software device.</span></span> <span data-ttu-id="4feda-113">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="4feda-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="4feda-114">這個屬性是在下列函式所傳回的啟用物件上設定：</span><span class="sxs-lookup"><span data-stu-id="4feda-114">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="4feda-115">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="4feda-115">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="4feda-116">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="4feda-116">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="4feda-117">屬性只適用于影片捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="4feda-117">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="4feda-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="4feda-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4feda-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4feda-119">Requirements</span></span>



| <span data-ttu-id="4feda-120">需求</span><span class="sxs-lookup"><span data-stu-id="4feda-120">Requirement</span></span> | <span data-ttu-id="4feda-121">值</span><span class="sxs-lookup"><span data-stu-id="4feda-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4feda-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4feda-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4feda-123">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4feda-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4feda-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4feda-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4feda-125">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4feda-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4feda-126">標頭</span><span class="sxs-lookup"><span data-stu-id="4feda-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4feda-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4feda-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4feda-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4feda-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4feda-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4feda-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4feda-130">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="4feda-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="4feda-131">捕獲裝置屬性</span><span class="sxs-lookup"><span data-stu-id="4feda-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




