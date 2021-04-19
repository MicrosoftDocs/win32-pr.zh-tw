---
title: 'Tab 控制項專案狀態 (CommCtrl .h) '
description: 索引標籤控制項現在支援支援 TCM DESELECTALL 訊息的專案狀態 \_ 。 此外，TCITEM 結構支援專案狀態值。
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989572"
---
# <a name="tab-control-item-states"></a>Tab 控制項專案狀態

索引標籤控制項現在支援支援 [**TCM \_ DESELECTALL**](tcm-deselectall.md) 訊息的專案狀態。 此外， [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) 結構支援專案狀態值。



| 常數                                                                                                                                                                     | 描述                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <dt>**TCIS \_ BUTTONPRESSED**</dt> </dl> | [版本 4.70](common-control-versions.md)。 已選取 [索引標籤控制項] 專案。 只有在已設定 [**TCS \_ 按鈕**](tab-control-styles.md) 樣式旗標的情況下，此狀態才有意義。<br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <dt>**TCIS 反 \_ 白顯示**</dt> </dl>       | [版本 4.71](common-control-versions.md)。 索引標籤控制項專案會反白顯示，並使用目前的反白顯示色彩來繪製索引標籤和文字。 使用高色彩時，這會是真正的插補，而非遞色色彩。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





