---
title: 'IMAGELISTSTATEFLAGS (Commctrl) '
description: 下列旗標會傳遞至 IMAGELISTDRAWPARAMS 的 fState 成員中的 IImageList Draw 方法。
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024931"
---
# <a name="imageliststateflags"></a><span data-ttu-id="eaf46-103">IMAGELISTSTATEFLAGS</span><span class="sxs-lookup"><span data-stu-id="eaf46-103">IMAGELISTSTATEFLAGS</span></span>

<span data-ttu-id="eaf46-104">下列旗標會傳遞至 [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)的 **fState** 成員中的 [**IImageList：:D raw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw)方法。</span><span class="sxs-lookup"><span data-stu-id="eaf46-104">The following flags are passed to the [**IImageList::Draw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) method in the **fState** member of [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span></span>



| <span data-ttu-id="eaf46-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="eaf46-105">Constant/value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="eaf46-106">Description</span><span class="sxs-lookup"><span data-stu-id="eaf46-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <span data-ttu-id="eaf46-107"><dt>**ILS \_正常**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="eaf46-107"><dt>**ILS\_NORMAL**</dt> <dt>0x00000000</dt></span></span> </dl>       | <span data-ttu-id="eaf46-108">映射狀態不會修改。</span><span class="sxs-lookup"><span data-stu-id="eaf46-108">The image state is not modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <span data-ttu-id="eaf46-109"><dt>**ILS \_發光**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="eaf46-109"><dt>**ILS\_GLOW**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="eaf46-110">不支援。</span><span class="sxs-lookup"><span data-stu-id="eaf46-110">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <span data-ttu-id="eaf46-111"><dt>**ILS \_陰影**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="eaf46-111"><dt>**ILS\_SHADOW**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="eaf46-112">不支援。</span><span class="sxs-lookup"><span data-stu-id="eaf46-112">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <span data-ttu-id="eaf46-113"><dt>**ILS \_飽和**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="eaf46-113"><dt>**ILS\_SATURATE**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="eaf46-114">將圖示的色彩飽和度減少為灰階。</span><span class="sxs-lookup"><span data-stu-id="eaf46-114">Reduces the color saturation of the icon to grayscale.</span></span> <span data-ttu-id="eaf46-115">這只會影響32bpp 映射。</span><span class="sxs-lookup"><span data-stu-id="eaf46-115">This only affects 32bpp images.</span></span> <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <span data-ttu-id="eaf46-116"><dt>**ILS \_ALPHA**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="eaf46-116"><dt>**ILS\_ALPHA**</dt> <dt>0x00000008</dt></span></span> </dl>          | <span data-ttu-id="eaf46-117">Alpha 會混合圖示。</span><span class="sxs-lookup"><span data-stu-id="eaf46-117">Alpha blends the icon.</span></span> <span data-ttu-id="eaf46-118">Alpha 混色會根據其 Alpha 色板的值來控制圖示的透明度層級。</span><span class="sxs-lookup"><span data-stu-id="eaf46-118">Alpha blending controls the transparency level of an icon, according to the value of its alpha channel.</span></span> <span data-ttu-id="eaf46-119">Alpha 色板的值是由 [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)方法中的 **frame** 成員所表示。</span><span class="sxs-lookup"><span data-stu-id="eaf46-119">The value of the alpha channel is indicated by the **frame** member in the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) method.</span></span> <span data-ttu-id="eaf46-120">Alpha 色板可以是從0到255，其中0是完全透明，而255則完全不透明。</span><span class="sxs-lookup"><span data-stu-id="eaf46-120">The alpha channel can be from 0 to 255, with 0 being completely transparent, and 255 being completely opaque.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="eaf46-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="eaf46-121">Requirements</span></span>



| <span data-ttu-id="eaf46-122">需求</span><span class="sxs-lookup"><span data-stu-id="eaf46-122">Requirement</span></span> | <span data-ttu-id="eaf46-123">值</span><span class="sxs-lookup"><span data-stu-id="eaf46-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf46-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eaf46-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf46-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eaf46-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eaf46-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eaf46-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf46-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eaf46-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eaf46-128">標頭</span><span class="sxs-lookup"><span data-stu-id="eaf46-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaf46-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="eaf46-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

