---
title: PlayerApplication 物件
description: PlayerApplication 物件提供一種方式，可協調遠端 Windows Media Player 控制項與 Windows Media Player 的完整模式之間的切換。
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- PlayerApplication 物件 Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313244"
---
# <a name="playerapplication-object"></a>PlayerApplication 物件

**PlayerApplication** 物件提供一種方式，可協調遠端 Windows Media Player 控制項與 Windows Media Player 的完整模式之間的切換。 此物件僅適用于執行 **IWMPRemoteMediaServices** 介面的 c + + 程式，並在遠端模式中內嵌播放機控制項。 用來作為遠端 Windows Media Player 控制項自訂介面的面板檔案會透過 **playerApplication** 全域屬性，在腳本中存取這個物件。

**PlayerApplication** 物件支援下列屬性。



| 屬性                                           | 描述                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [hasDisplay](playerapplication-hasdisplay.md)     | 抓取值，指出影片是否可以透過遠端 Windows Media Player 控制項顯示。 |
| [playerDocked](playerapplication-playerdocked.md) | 抓取值，指出 Windows Media Player 是否處於停駐狀態。                          |



 

**PlayerApplication** 物件支援下列方法。



| 方法                                                                       | 描述                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [switchToControl](playerapplication-switchtocontrol.md)                     | 將遠端 Windows Media Player 控制項切換至停駐的狀態。            |
| [switchToPlayerApplication](playerapplication-switchtoplayerapplication.md) | 將遠端 Windows Media Player 控制項切換至播放程式的完整模式。 |



 

**PlayerApplication** 物件是透過下列屬性來存取。



| Object                      | 屬性                                          |
|-----------------------------|---------------------------------------------------|
| [球員](player-object.md) | [playerApplication](player-playerapplication.md) |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> <dt>

[**遠端處理 Windows Media Player 控制項**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




