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
# <a name="dxgi-15-improvements"></a>DXGI 1.5 改進

Microsoft DirectX Graphic Infrastructure (DXGI) 1.5 中新增了下列功能，以支援更有彈性地指定和複製輸出格式。

## <a name="high-dynamic-range-and-wide-color-gamut"></a>高動態範圍和寬色色域

請參閱 [使用具有高動態範圍的 DirectX 顯示和先進的色彩](../direct3darticles/high-dynamic-range.md)。

## <a name="variable-refresh-rate-displays"></a>變數重新整理率顯示

請參閱 [變數重新整理頻率顯示](variable-refresh-rate-displays.md)。

## <a name="duplicating-output"></a>複製輸出

單一介面 [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5)（具有單一方法 [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1)）已新增至 DXGI 1.5，以提供更具彈性且更高的原始 [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) 方法效能版本。 **DuplicateOutput1** 允許針對可由 [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) 物件傳回的全螢幕表面指定支援的格式清單，並啟用捕獲 HDR 和 WCG 內容。

## <a name="offering-and-reclaiming-resources"></a>提供和回收資源

已將 [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) 和 [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) 的更新方法新增至新的介面 [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4)，以允許除了捨棄資源之外，還可取消認可記憶體。 加入宣告新的 [**DXGI \_ 供應專案 \_ 資源 \_ 旗標 [ \_ 允許 \_ 取消認可**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) ] 旗標表示必須正確處理新的回收結果。

## <a name="related-topics"></a>相關主題

[DXGI 的程式設計指南](dx-graphics-dxgi-overviews.md)
