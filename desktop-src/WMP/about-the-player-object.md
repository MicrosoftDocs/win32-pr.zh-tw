---
title: 關於 Player 物件
description: 關於 Player 物件
ms.assetid: db995e75-d4e3-4f50-a34a-cc1b2f2c5db5
keywords:
- Windows Media Player，Player 物件
- Windows Media Player 物件模型、Player 物件
- 物件模型、Player 物件
- Windows Media Player ActiveX control、Player 物件
- ActiveX control、Player 物件
- Windows Media PlayerMobile ActiveX control、Player 物件
- Windows Media PlayerMobile、Player 物件
- Player 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a6d32fe08bca480d907d0b97588cdc9477441951f619a0fab4fcbcb2933c48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903108"
---
# <a name="about-the-player-object"></a>關於 Player 物件

**Player** 物件是 Windows Media Player 控制項的核心物件。 所有其他相關物件都會透過傳回物件的特定屬性連接到這個物件。 例如，**設定** 物件是透過 **Settings** 屬性來存取。 **Player** 物件提供與 Windows Media Player 核心功能相關的方法、屬性和事件。

因為此參考也可用於外觀程式設計，所以 **播放** 程式物件的識別碼將會是 "player"，以取得語法範例。

使用面板定義檔內的 **media player** 全域屬性，可讓您存取 **player** 物件以在腳本中使用。 透過 **Player** 物件，Windows Media Player 控制項中的其他所有物件也都可供腳本使用。 **Player** 物件和 **URL** 屬性的事件也可以在設計階段使用 [播放](player-element.md)程式面板元素來指定。 如需詳細資訊，請參閱[Windows Media Player 的外觀](windows-media-player-skins.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**指令碼語言的播放程式物件模型**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




