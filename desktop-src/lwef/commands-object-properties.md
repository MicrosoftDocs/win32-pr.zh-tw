---
title: 命令物件屬性
description: 命令物件屬性
ms.assetid: 889a56b2-0b6d-4df8-a313-7553371e4413
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b9e8f8e6e7b44697891cd567fce8ca0f5db13a0142936b5cf48bdb52721392
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716538"
---
# <a name="commands-object-properties"></a>命令物件屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

伺服器支援 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合的下列屬性：

-   [**標題**](caption-property-cmds.md)
-   [**計數**](count-property.md)
-   [**DefaultCommand**](defaultcommand-property.md)
-   [**FontName**](fontname-property.md)
-   [**FontSize**](fontsize-property.md)
-   [**GlobalVoiceCommandsEnabled**](globalvoicecommandsenabled-property.md)
-   [**號**](helpcontextid-property.md)
-   [**可見**](visible-property-cso.md)
-   [**語音**](voice-property.md)
-   [**VoiceCaption**](voicecaption-property.md)

[**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的專案可以同時出現在一個字元的快顯功能表和 [語音命令] 視窗中。 若要讓這個專案出現在快顯功能表中，請設定其 [**標題**](caption-property-cmds.md) 屬性。 若要在 [語音命令] 視窗中包含專案，請設定其 [**VoiceCaption**](voicecaption-property.md) 屬性。  (為了回溯相容性，如果沒有 **VoiceCaption**，則會使用 **標題** 設定) 

下表摘要說明 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件的屬性如何影響專案的呈現方式：



| Caption 屬性                                                                                                                                                                                                                                            | Voice-Caption 屬性 | Voice 屬性 | Visible 屬性 | 出現在字元的快顯功能表中 | 出現在 [語音命令] 視窗中 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|----------------|------------------|------------------------------------|----------------------------------|
| 是                                                                                                                                                                                                                                                         | 是                    | 是            | 是             | 是，使用標題                 | 是，使用 VoiceCaption          |
| 是                                                                                                                                                                                                                                                         | 是                    | 否             | 是             | 是，使用標題                 | 否                               |
| 是                                                                                                                                                                                                                                                         | 是                    | 是            | False            | 否                                 | 是，使用 VoiceCaption          |
| 是                                                                                                                                                                                                                                                         | 是                    | 否             | False            | 否                                 | 否                               |
| 否                                                                                                                                                                                                                                                          | 是                    | 是            | True             | 否                                 | 是，使用 VoiceCaption          |
| 否                                                                                                                                                                                                                                                          | 是                    | 是            | False            | 否                                 | 是，使用 VoiceCaption          |
| 否                                                                                                                                                                                                                                                          | 是                    | 否             | True             | 否                                 | 否                               |
| 否                                                                                                                                                                                                                                                          | 是                    | 否             | False            | 否                                 | 否                               |
| 是                                                                                                                                                                                                                                                         | 否                    | Yes            | 是             | 是，使用標題                 | 是，使用標題               |
| 是                                                                                                                                                                                                                                                         | 否                     | 否             | True             | 是                                | 否                               |
| 是                                                                                                                                                                                                                                                         | 否                     | 是            | False            | 否                                 | 是，使用標題               |
| 是                                                                                                                                                                                                                                                         | 否                     | 否             | False            | 否                                 | 否                               |
| 否                                                                                                                                                                                                                                                          | 否                     | 是            | True             | 否                                 | 否                               |
| 否                                                                                                                                                                                                                                                          | 否                     | 是            | False            | 否                                 | 否                               |
| 否                                                                                                                                                                                                                                                          | 否                     | 否             | True             | 否                                 | 否                               |
| 否                                                                                                                                                                                                                                                          | 否                     | 否             | False            | 否                                 | 否                               |
|  如果屬性設定為 null。 在某些程式設計語言中，空字串可能不會解讀為與 null 字串相同的字串。  此命令仍然可以語音存取，並在 [語音命令] 視窗中顯示為「 (命令未定義) 」。<br/> |                        |                |                  |                                    |                                  |



 

 

