---
description: 允許增強型影片轉譯器 (EVR) 對 Microsoft Direct3D IDirect3DDevice9：:P 重發方法進行批次呼叫。
ms.assetid: 6dbb2839-97ea-4881-8f22-0f8e943a3071
title: 'EVRConfig_AllowBatching 屬性 (Uuid. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191c3c0f0ea4ad18e7bb711ae6d37c21f75cd478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510793"
---
# <a name="evrconfig_allowbatching-attribute"></a><span data-ttu-id="f279e-103">EVRConfig \_ AllowBatching 屬性</span><span class="sxs-lookup"><span data-stu-id="f279e-103">EVRConfig\_AllowBatching attribute</span></span>

<span data-ttu-id="f279e-104">允許增強型影片轉譯器 (EVR) 對 Microsoft Direct3D **IDirect3DDevice9：:P 重發** 方法進行批次呼叫。</span><span class="sxs-lookup"><span data-stu-id="f279e-104">Allows the Enhanced Video Renderer (EVR) to batch calls to the Microsoft Direct3D **IDirect3DDevice9::Present** method.</span></span>

## <a name="data-type"></a><span data-ttu-id="f279e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f279e-105">Data type</span></span>

<span data-ttu-id="f279e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f279e-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f279e-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="f279e-107">Get/set</span></span>

<span data-ttu-id="f279e-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="f279e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f279e-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="f279e-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f279e-110">備註</span><span class="sxs-lookup"><span data-stu-id="f279e-110">Remarks</span></span>

<span data-ttu-id="f279e-111">您可以在 EVR 媒體接收上設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f279e-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="f279e-112">若要設定屬性，請使用 **QueryInterface** 來查詢 [**IMFATTRIBUTES**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的 EVR 媒體接收。</span><span class="sxs-lookup"><span data-stu-id="f279e-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="f279e-113">設定這個屬性的效果與在 EVR 上設定 **MFVideoRenderPrefs \_ AllowBatching** 旗標相同。</span><span class="sxs-lookup"><span data-stu-id="f279e-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_AllowBatching** flag on the EVR.</span></span> <span data-ttu-id="f279e-114">如需此旗標的說明，請參閱 [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) 。</span><span class="sxs-lookup"><span data-stu-id="f279e-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="f279e-115">這個屬性的 GUID 常數是從 strmiids 匯出。</span><span class="sxs-lookup"><span data-stu-id="f279e-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f279e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f279e-116">Requirements</span></span>



| <span data-ttu-id="f279e-117">需求</span><span class="sxs-lookup"><span data-stu-id="f279e-117">Requirement</span></span> | <span data-ttu-id="f279e-118">值</span><span class="sxs-lookup"><span data-stu-id="f279e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f279e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f279e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f279e-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f279e-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f279e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f279e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f279e-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f279e-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f279e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f279e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f279e-124"><dt>Uuid。h</dt></span><span class="sxs-lookup"><span data-stu-id="f279e-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f279e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f279e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f279e-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f279e-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f279e-127">EVR 屬性</span><span class="sxs-lookup"><span data-stu-id="f279e-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="f279e-128">影片品質管制</span><span class="sxs-lookup"><span data-stu-id="f279e-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




