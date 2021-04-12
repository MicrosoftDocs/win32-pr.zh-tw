---
description: 允許增強型影片轉譯器 (EVR) 使用 bob 去交錯來改善效能。
ms.assetid: e145e862-b987-4962-a94b-f8370bbcd5ac
title: 'EVRConfig_AllowDropToBob 屬性 (Uuid. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3940edd0945999f7300060d963806e3572a5d0fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386028"
---
# <a name="evrconfig_allowdroptobob-attribute"></a><span data-ttu-id="1125d-103">EVRConfig \_ AllowDropToBob 屬性</span><span class="sxs-lookup"><span data-stu-id="1125d-103">EVRConfig\_AllowDropToBob attribute</span></span>

<span data-ttu-id="1125d-104">允許增強型影片轉譯器 (EVR) 使用 bob 去交錯來改善效能。</span><span class="sxs-lookup"><span data-stu-id="1125d-104">Allows the Enhanced Video Renderer (EVR) to improve performance by using bob deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="1125d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="1125d-105">Data type</span></span>

<span data-ttu-id="1125d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1125d-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="1125d-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="1125d-107">Get/set</span></span>

<span data-ttu-id="1125d-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="1125d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="1125d-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="1125d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="1125d-110">備註</span><span class="sxs-lookup"><span data-stu-id="1125d-110">Remarks</span></span>

<span data-ttu-id="1125d-111">您可以在 EVRmedia 接收上設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1125d-111">This attribute can be set on the EVRmedia sink.</span></span> <span data-ttu-id="1125d-112">若要設定屬性，請針對 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面查詢 EVR 媒體接收的 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="1125d-112">To set the attribute, **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="1125d-113">設定這個屬性的效果與在 EVR 上設定 **MFVideoMixPrefs \_ AllowDropToBob** 旗標相同。</span><span class="sxs-lookup"><span data-stu-id="1125d-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_AllowDropToBob** flag on the EVR.</span></span> <span data-ttu-id="1125d-114">如需此旗標的說明，請參閱 [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) 。</span><span class="sxs-lookup"><span data-stu-id="1125d-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="1125d-115">這個屬性的 GUID 常數是從 strmiids 匯出。</span><span class="sxs-lookup"><span data-stu-id="1125d-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1125d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1125d-116">Requirements</span></span>



| <span data-ttu-id="1125d-117">需求</span><span class="sxs-lookup"><span data-stu-id="1125d-117">Requirement</span></span> | <span data-ttu-id="1125d-118">值</span><span class="sxs-lookup"><span data-stu-id="1125d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1125d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1125d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1125d-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1125d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1125d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1125d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1125d-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1125d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1125d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1125d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1125d-124"><dt>Uuid。h</dt></span><span class="sxs-lookup"><span data-stu-id="1125d-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1125d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1125d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1125d-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="1125d-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1125d-127">EVR 屬性</span><span class="sxs-lookup"><span data-stu-id="1125d-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="1125d-128">影片品質管制</span><span class="sxs-lookup"><span data-stu-id="1125d-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




