---
title: 'IMAGELISTDRAWFLAGS (Commctrl) '
description: 傳遞給 IMAGELISTDRAWPARAMS 之 fStyle 成員中的 IImageList Draw 方法。
ms.assetid: 99fd2cb2-0cb0-40c2-b184-b6d8e54397b4
topic_type:
- apiref
api_name:
- ILD_NORMAL
- ILD_TRANSPARENT
- ILD_BLEND25
- ILD_FOCUS
- ILD_BLEND50
- ILD_SELECTED
- ILD_BLEND
- ILD_MASK
- ILD_IMAGE
- ILD_ROP
- ILD_OVERLAYMASK
- ILD_PRESERVEALPHA
- ILD_SCALE
- ILD_DPISCALE
- ILD_ASYNC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0743fc2778b3ef693646327fe8206ebedcb89e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934201"
---
# <a name="imagelistdrawflags"></a>IMAGELISTDRAWFLAGS

傳遞至 [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)的 **fStyle** 成員中的 [**IImageList：:D 原始**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw)方法。



| 常數/值                                                                                                                                                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILD_NORMAL"></span><span id="ild_normal"></span><dl> <dt>**I ... \_正常**</dt> <dt>0x00000000</dt> </dl>                      | 使用影像清單的背景色彩繪製影像。 如果背景色彩是 CLR \_ 無值，則會使用遮罩以透明的方式繪製影像。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_TRANSPARENT"></span><span id="ild_transparent"></span><dl> <dt>**I ... \_透明**</dt> <dt>0x00000001</dt> </dl>       | 使用遮罩以透明的方式繪製影像，不論背景色彩為何。 如果影像清單不包含遮罩，則此值沒有任何作用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_BLEND25"></span><span id="ild_blend25"></span><dl> <dt>**I ... \_BLEND25**</dt> <dt>0x00000002</dt> </dl>                   | 繪製影像，並使用 **rgbFg** 所指定的 blend 色彩來混合25%。 如果影像清單不包含遮罩，則此值沒有任何作用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_FOCUS"></span><span id="ild_focus"></span><dl> <dt>**I ... \_專注于**</dt> <dt>0x00000002</dt> </dl>                         | 與 **I ... \_ BLEND25** 相同。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND50"></span><span id="ild_blend50"></span><dl> <dt>**I ... \_BLEND50**</dt> <dt>0x00000004</dt> </dl>                   | 繪製影像，並使用 **rgbFg** 所指定的 blend 色彩來混合50%。 如果影像清單不包含遮罩，則此值沒有任何作用。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_SELECTED"></span><span id="ild_selected"></span><dl> <dt>**I ... \_選取**</dt>的 <dt>0x00000004</dt> </dl>                | 與 **I ... \_ BLEND50** 相同。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND"></span><span id="ild_blend"></span><dl> <dt>**I ... \_BLEND**</dt> <dt>0x00000004</dt> </dl>                         | 與 **I ... \_ BLEND50** 相同。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_MASK"></span><span id="ild_mask"></span><dl> <dt>**I ... \_遮罩**</dt> <dt>0x00000010</dt> </dl>                            | 繪製遮罩。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_IMAGE"></span><span id="ild_image"></span><dl> <dt>**I ... \_映射**</dt> <dt>0x00000020</dt> </dl>                         | 如果覆迭不需要繪製遮罩，請設定此旗標。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_ROP"></span><span id="ild_rop"></span><dl> <dt>**I ... \_ROP**</dt> <dt>0x00000040</dt> </dl>                               | 使用 **dwRop** 成員所指定的點陣作業程式碼繪製影像。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_OVERLAYMASK"></span><span id="ild_overlaymask"></span><dl> <dt>**I ... \_OVERLAYMASK**</dt> <dt>0x00000F00</dt> </dl>       | 若要從 **fStyle** 成員解壓縮覆迭影像，請使用邏輯 AND 來結合 **fStyle** 與 **i ... \_ OVERLAYMASK** 值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ILD_PRESERVEALPHA"></span><span id="ild_preservealpha"></span><dl> <dt>**I ... \_PRESERVEALPHA**</dt> <dt>0x00001000</dt> </dl> | 保留目的地中的 Alpha 通道。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_SCALE"></span><span id="ild_scale"></span><dl> <dt>**I ... \_調整**</dt> <dt>0x00002000</dt> </dl>                         | 使影像縮放至 cx、cy 而不是裁剪。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ILD_DPISCALE"></span><span id="ild_dpiscale"></span><dl> <dt>**I ... \_DPISCALE**</dt> <dt>0x00004000</dt> </dl>                | 將影像縮放至顯示器的目前 DPI。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ILD_ASYNC"></span><span id="ild_async"></span><dl> <dt>**I ... \_非同步**</dt> <dt>0x00008000</dt> </dl>                         | **Windows Vista （含）以後版本。** 如果映射可在快取中使用，請繪製影像。 請勿自動將其解壓縮。 呼叫的繪圖方法會將 E 暫止傳回 \_ 給呼叫的元件，然後再採取替代動作，例如，提供另一個影像並將背景工作排入佇列，以強制透過 [**FORCEIMAGEPRESENT**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-forceimagepresent) 使用 ILFIP ALWAYS 旗標來載入映射 \_ 。 I ... \_ ASYNC 旗標接著會防止解壓縮作業封鎖目前的執行緒，而且如果從使用者介面呼叫 draw 方法 (UI) 執行緒，就特別重要。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

