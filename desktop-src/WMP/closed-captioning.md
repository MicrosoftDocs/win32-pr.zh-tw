---
title: 隱藏式字幕功能
description: 隱藏式字幕功能
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- 'Windows Media Player，可同步的可存取媒體交換 (薩米文) '
- 'Windows Media Player 物件模型、已同步處理的可存取媒體交換 (薩米文) '
- '物件模型、同步的可存取媒體交換 (薩米) '
- 'Windows Media Player 行動裝置、已同步處理的可存取媒體交換 (薩米文) '
- 'Windows Media Player ActiveX 控制項、同步存取媒體交換 (薩米文) '
- 'Windows Media Player 的行動 ActiveX 控制項、已同步處理的可存取媒體交換 (薩米文) '
- 'ActiveX 控制項、同步的可存取媒體交換 (薩米) '
- Windows Media Player，遷移隱藏式輔助字幕
- Windows Media Player 物件模型、Smigrating 隱藏式輔助字幕
- 物件模型，遷移隱藏式輔助字幕
- Windows Media Player 行動裝置，遷移隱藏式輔助字幕
- Windows Media Player ActiveX 控制項、遷移隱藏式輔助字幕
- Windows Media Player 行動 ActiveX 控制項、遷移隱藏式輔助字幕
- ActiveX 控制項，遷移隱藏式輔助字幕
- 已同步處理的可存取媒體交換 (薩米) ，正在遷移隱藏式輔助字幕
- 薩米文 (同步處理可存取媒體交換) ，遷移隱藏式輔助字幕
- '遷移指南，同步處理的可存取媒體交換 (薩米) '
- 遷移指南，隱藏式輔助字幕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092564"
---
# <a name="closed-captioning"></a>隱藏式字幕功能

Windows Media Player 6.4 ActiveX 控制項包含整合式隱藏式輔助字幕顯示面板，當它顯示時，會啟用同步的可存取媒體交換 (薩米) 隱藏式輔助字幕，並顯示隱藏的標題文字。 Windows Media Player 7 或更新版本的控制項可讓您使用 HTML 元素，啟用以薩米的隱藏式輔助字幕顯示 **<DIV>** 。 例如：


```C++
<DIV  ID = "CCDiv"></DIV>

```



這項技術可提供您完整的彈性，因為您可以設計網頁以自訂的方式顯示隱藏式輔助字幕;隱藏式輔助字幕顯示不再需要位於 Windows Media Player 使用者介面旁的固定位置。

建立區域以顯示隱藏式輔助字幕之後，請使用 *ClosedCaption*。**captioningID** 屬性，指定 Windows Media Player 呈現隱藏式輔助字幕文字的位置。


```C++
Player.closedCaption.captioningID = "CCDiv";

```



Windows Media Player 軟體發展工具組 (SDK) 包含可顯示隱藏式輔助字幕文字之內嵌播放程式的工作範例。 若要取得 SDK 範例，請從 Microsoft 網站下載並安裝完整的 Windows Media Player SDK。 如需隱藏式輔助字幕和薩米文的詳細資訊，請參閱 [Microsoft 協助工具網站](https://www.microsoft.com/enable/)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption 物件**](closedcaption-object.md)
</dt> <dt>

[**物件模型遷移指南**](object-model-migration-guide.md)
</dt> </dl>

 

 




