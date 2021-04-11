---
title: 控制項的環境屬性
description: 控制項的環境屬性
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372311"
---
# <a name="ambient-properties-for-controls"></a>控制項的環境屬性

如果控制項完全支援任何環境屬性，則必須至少遵循下表所述的下列環境屬性（使用標準 dispid）的值。



| 環境屬性            | Dispid          | 使用的批註/條件                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocaleID<br/>         | -705<br/> | 如果對控制項的地區設定很重要，例如文字輸出<br/>                                                                                                                                                                                                                  |
| UserMode <br/>        | -709<br/> | 如果控制項在使用者 (設計) 模式和執行模式中的行為不同<br/>                                                                                                                                                                                                          |
| UIDead<br/>           | -710<br/> | 如果控制項回應 UI 事件，則應接受此環境屬性<br/>                                                                                                                                                                                                 |
| ShowGrabHandles<br/>  | -711<br/> | 如果控制項支援就地調整本身的大小<br/>                                                                                                                                                                                                                             |
| ShowHatching<br/>     | -712<br/> | 如果控制項支援就地啟用和 UI 啟用<br/>                                                                                                                                                                                                                   |
| DisplayAsDefault<br/> | -713<br/> | 只有在控制項標示為 OLEMISC \_ ACTSLIKEBUTTON (這表示已提供支援鍵盤助憶鍵，因此 [**IOleControl：： GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) 和 [**IOleControl：： OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) 必須) 執行。<br/> |



 

如先前所述，使用 ambients 需要 [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)的 [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (做為最小) ，以及 [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite)和 [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)) 的 [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (。

\_容器不一定會支援 OLEMISC SETCLIENTSITEFIRST 位。 在這些情況下，控制項必須使用其所需之環境屬性的預設值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項](controls.md)
</dt> </dl>

 

 





