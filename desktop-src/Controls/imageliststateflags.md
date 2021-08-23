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
ms.openlocfilehash: 3cbb4eef2f744c78e84999e9f07f3ca5a06d5dbf93dbfa26d5c6593d94d4e19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576138"
---
# <a name="imageliststateflags"></a>IMAGELISTSTATEFLAGS

下列旗標會傳遞至 [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)的 **fState** 成員中的 [**IImageList：:D raw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw)方法。



| 常數/值                                                                                                                                                                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <dt>**ILS \_正常**</dt> <dt>0x00000000</dt> </dl>       | 映射狀態不會修改。<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <dt>**ILS \_發光**</dt> <dt>0x00000001</dt> </dl>             | 不支援。 <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <dt>**ILS \_陰影**</dt> <dt>0x00000002</dt> </dl>       | 不支援。 <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <dt>**ILS \_飽和**</dt> <dt>0x00000004</dt> </dl> | 將圖示的色彩飽和度減少為灰階。 這只會影響32bpp 映射。 <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <dt>**ILS \_ALPHA**</dt> <dt>0x00000008</dt> </dl>          | Alpha 會混合圖示。 Alpha 混色會根據其 Alpha 色板的值來控制圖示的透明度層級。 Alpha 色板的值是由 [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)方法中的 **frame** 成員所表示。 Alpha 色板可以是從0到255，其中0是完全透明，而255則完全不透明。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

