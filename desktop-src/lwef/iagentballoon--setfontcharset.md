---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178e2f6e2e086962456b6717dcb6866db9d607dd16136f839a127857d85cd58e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751050"
---
# <a name="iagentballoonsetfontcharset"></a>IAgentBalloon::SetFontCharSet

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

設定文字氣球中所顯示字型的字元集。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*
</dt> <dd>

字型的字元集。 以下是一些常見的值設定：



| 值    | 字元集                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| 0   | 標準 Windows 字元 (ANSI) 。                                                    |
| 1   | 預設字元集。                                                                 |
| 2   | 符號字元集。                                                              |
| 128 | Windows 的日文版 (DBCS) 獨特的雙位元組字元集。            |
| 129 | 雙位元組字集 (DBCS) Windows 的韓文版本是唯一的。              |
| 134 | 雙位元組字集 (DBCS) Windows 的簡體中文版本中是唯一的。  |
| 136 | 雙位元組字集 (DBCS) 繁體中文 Windows 的獨特版本。 |
| 255 | MS-DOS 應用程式通常會顯示的擴充字元。                          |



 

</dd> </dl>

如需其他字元集值，請參閱 Platform SDK 檔集。

字元字提示字元中使用的預設字元集是在 Microsoft Agent 字元編輯器中定義。 您可以使用 [**IAgentBalloon：： SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**)來變更它。 不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字元集設定。 這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentBalloon::GetFontCharSet**](iagentballoon--getfontcharset.md)


 

 




