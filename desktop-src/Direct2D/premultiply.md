---
title: Premultiply 效果
description: 使用此效果將影像從 unpremultiplied Alpha 轉換成預乘 Alpha。
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- premultiply 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01a8a9ba005ed688a96254856897b3514f05fd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934692"
---
# <a name="premultiply-effect"></a><span data-ttu-id="6d0e9-104">Premultiply 效果</span><span class="sxs-lookup"><span data-stu-id="6d0e9-104">Premultiply effect</span></span>

<span data-ttu-id="6d0e9-105">使用此效果將影像從 unpremultiplied Alpha 轉換成預乘 Alpha。</span><span class="sxs-lookup"><span data-stu-id="6d0e9-105">Use this effect to convert an image from unpremultiplied alpha to premultiplied alpha.</span></span> <span data-ttu-id="6d0e9-106">效果會將輸出中的每個輸入圖元取代 `P = {R, G, B, A}` 為 `P' = {R*A, G*A, B*A, A}` 。</span><span class="sxs-lookup"><span data-stu-id="6d0e9-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R*A, G*A, B*A, A}` in the output.</span></span>

<span data-ttu-id="6d0e9-107">此效果沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="6d0e9-107">This effect has no properties.</span></span>

<span data-ttu-id="6d0e9-108">這項效果的 CLSID 是 CLSID \_ D2D1Premultiply。</span><span class="sxs-lookup"><span data-stu-id="6d0e9-108">The CLSID for this effect is CLSID\_D2D1Premultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="6d0e9-109">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="6d0e9-109">Output bitmap</span></span>

<span data-ttu-id="6d0e9-110">輸出點陣圖大小與輸入點陣圖大小相同。</span><span class="sxs-lookup"><span data-stu-id="6d0e9-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d0e9-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d0e9-111">Requirements</span></span>



| <span data-ttu-id="6d0e9-112">需求</span><span class="sxs-lookup"><span data-stu-id="6d0e9-112">Requirement</span></span> | <span data-ttu-id="6d0e9-113">值</span><span class="sxs-lookup"><span data-stu-id="6d0e9-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d0e9-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d0e9-114">Minimum supported client</span></span> | <span data-ttu-id="6d0e9-115">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d0e9-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6d0e9-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d0e9-116">Minimum supported server</span></span> | <span data-ttu-id="6d0e9-117">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d0e9-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6d0e9-118">標頭</span><span class="sxs-lookup"><span data-stu-id="6d0e9-118">Header</span></span>                   | <span data-ttu-id="6d0e9-119">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="6d0e9-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="6d0e9-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="6d0e9-120">Library</span></span>                  | <span data-ttu-id="6d0e9-121">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="6d0e9-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="6d0e9-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d0e9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d0e9-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="6d0e9-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
