---
description: Microsoft DirectX Graphic Infrastructure (DXGI) 1.5 中新增了下列功能，以支援更有彈性地指定和複製輸出格式。
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: DXGI 1.5 改進
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 58df3ef78781437ee033530a2ed2179bb9a132d8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104321747"
---
# <a name="dxgi-15-improvements"></a><span data-ttu-id="c2c5f-103">DXGI 1.5 改進</span><span class="sxs-lookup"><span data-stu-id="c2c5f-103">DXGI 1.5 Improvements</span></span>

<span data-ttu-id="c2c5f-104">Microsoft DirectX Graphic Infrastructure (DXGI) 1.5 中新增了下列功能，以支援更有彈性地指定和複製輸出格式。</span><span class="sxs-lookup"><span data-stu-id="c2c5f-104">The following functionality has been added to Microsoft DirectX Graphics Infrastructure (DXGI) 1.5, to support more flexible specifying and duplication of output formats.</span></span>

## <a name="high-dynamic-range-and-wide-color-gamut"></a><span data-ttu-id="c2c5f-105">高動態範圍和寬色色域</span><span class="sxs-lookup"><span data-stu-id="c2c5f-105">High Dynamic Range and Wide Color Gamut</span></span>

<span data-ttu-id="c2c5f-106">請參閱 [使用具有高動態範圍的 DirectX 顯示和先進的色彩](../direct3darticles/high-dynamic-range.md)。</span><span class="sxs-lookup"><span data-stu-id="c2c5f-106">Refer to [Using DirectX with high dynamic range displays and advanced color](../direct3darticles/high-dynamic-range.md).</span></span>

## <a name="variable-refresh-rate-displays"></a><span data-ttu-id="c2c5f-107">變數重新整理率顯示</span><span class="sxs-lookup"><span data-stu-id="c2c5f-107">Variable refresh rate displays</span></span>

<span data-ttu-id="c2c5f-108">請參閱 [變數重新整理頻率顯示](variable-refresh-rate-displays.md)。</span><span class="sxs-lookup"><span data-stu-id="c2c5f-108">Refer to [Variable refresh rate displays](variable-refresh-rate-displays.md).</span></span>

## <a name="duplicating-output"></a><span data-ttu-id="c2c5f-109">複製輸出</span><span class="sxs-lookup"><span data-stu-id="c2c5f-109">Duplicating output</span></span>

<span data-ttu-id="c2c5f-110">單一介面 [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5)（具有單一方法 [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1)）已新增至 DXGI 1.5，以提供更具彈性且更高的原始 [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) 方法效能版本。</span><span class="sxs-lookup"><span data-stu-id="c2c5f-110">A single interface, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), with a single method, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), has been added to DXGI 1.5 to provide a more flexible and higher performance version of the original [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) method.</span></span> <span data-ttu-id="c2c5f-111">**DuplicateOutput1** 允許針對可由 [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) 物件傳回的全螢幕表面指定支援的格式清單，並啟用捕獲 HDR 和 WCG 內容。</span><span class="sxs-lookup"><span data-stu-id="c2c5f-111">**DuplicateOutput1** allows specifying a list of supported formats for fullscreen surfaces that can be returned by the [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) object, and enables capturing HDR and WCG content.</span></span>

## <a name="offering-and-reclaiming-resources"></a><span data-ttu-id="c2c5f-112">提供和回收資源</span><span class="sxs-lookup"><span data-stu-id="c2c5f-112">Offering and Reclaiming Resources</span></span>

<span data-ttu-id="c2c5f-113">已將 [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) 和 [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) 的更新方法新增至新的介面 [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4)，以允許除了捨棄資源之外，還可取消認可記憶體。</span><span class="sxs-lookup"><span data-stu-id="c2c5f-113">Updated methods [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) and [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) have been added to a new interface, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), to allow de-committing of memory in addition to discarding resources.</span></span> <span data-ttu-id="c2c5f-114">加入宣告新的 [**DXGI \_ 供應專案 \_ 資源 \_ 旗標 [ \_ 允許 \_ 取消認可**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) ] 旗標表示必須正確處理新的回收結果。</span><span class="sxs-lookup"><span data-stu-id="c2c5f-114">Opting in to the new [**DXGI\_OFFER\_RESOURCE\_FLAG\_ALLOW\_DECOMMIT**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) flag means the new reclaim results must be properly handled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2c5f-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2c5f-115">Related topics</span></span>

[<span data-ttu-id="c2c5f-116">DXGI 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="c2c5f-116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
