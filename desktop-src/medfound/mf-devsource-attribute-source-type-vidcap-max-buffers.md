---
description: 指定影片捕獲來源將緩衝的最大框架數目。
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: 'MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972667"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a><span data-ttu-id="b00b4-103">MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ MAX \_ 緩衝區屬性</span><span class="sxs-lookup"><span data-stu-id="b00b4-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_MAX\_BUFFERS attribute</span></span>

<span data-ttu-id="b00b4-104">指定影片捕獲來源將緩衝的最大框架數目。</span><span class="sxs-lookup"><span data-stu-id="b00b4-104">Specifies the maximum number of frames that the video capture source will buffer.</span></span>

## <a name="data-type"></a><span data-ttu-id="b00b4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b00b4-105">Data type</span></span>

<span data-ttu-id="b00b4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b00b4-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b00b4-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="b00b4-107">Get/set</span></span>

<span data-ttu-id="b00b4-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="b00b4-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b00b4-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="b00b4-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b00b4-110">備註</span><span class="sxs-lookup"><span data-stu-id="b00b4-110">Remarks</span></span>

<span data-ttu-id="b00b4-111">影片捕獲來源預設會一次緩衝最多一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="b00b4-111">By default, the video capture source buffers a maximum of one frame at a time.</span></span> <span data-ttu-id="b00b4-112">您可以藉由設定此屬性來增加緩衝區限制。</span><span class="sxs-lookup"><span data-stu-id="b00b4-112">You can increase the buffer limit by setting this attribute.</span></span>

<span data-ttu-id="b00b4-113">設定這個屬性的正確方式，取決於用來建立媒體來源的函式：</span><span class="sxs-lookup"><span data-stu-id="b00b4-113">The correct way to set this attribute depends on the function used to create the media source:</span></span>

-   <span data-ttu-id="b00b4-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)：透過函數的 *pAttributes* 參數來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="b00b4-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="b00b4-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)：透過函數的 *pAttributes* 參數來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="b00b4-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="b00b4-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)：在函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="b00b4-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): Set the attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned by the function.</span></span> <span data-ttu-id="b00b4-117">呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)之前，請先設定屬性。</span><span class="sxs-lookup"><span data-stu-id="b00b4-117">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="b00b4-118">屬性只適用于影片捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="b00b4-118">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="b00b4-119">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="b00b4-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b00b4-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b00b4-120">Requirements</span></span>



| <span data-ttu-id="b00b4-121">需求</span><span class="sxs-lookup"><span data-stu-id="b00b4-121">Requirement</span></span> | <span data-ttu-id="b00b4-122">值</span><span class="sxs-lookup"><span data-stu-id="b00b4-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b00b4-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b00b4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b00b4-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b00b4-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b00b4-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b00b4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b00b4-126">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b00b4-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b00b4-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b00b4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b00b4-128"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b00b4-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b00b4-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b00b4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b00b4-130">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b00b4-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b00b4-131">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="b00b4-131">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="b00b4-132">捕獲裝置屬性</span><span class="sxs-lookup"><span data-stu-id="b00b4-132">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




