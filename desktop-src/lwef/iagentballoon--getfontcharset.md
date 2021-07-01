---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120403"
---
# <a name="iagentballoongetfontcharset"></a>IAgentBalloon::GetFontCharSet

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

指出字型文字提示中所顯示字型的字元集。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*
</dt> <dd>

接收字型字元集之值的位址。 以下是一些常見的值設定：



| 值    | 字元集                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| 0   | 標準 Windows 字元 (ANSI) 。                                                    |
| 1   | 預設字元集。                                                                 |
| 2   | 符號字元集。                                                              |
| 128 | 在日文版的 Windows 中，雙位元組字元集 (DBCS) 是唯一的。            |
| 129 | 雙位元組字集 (DBCS) Windows 的韓文版本是唯一的。              |
| 134 | 雙位元組字集 (DBCS) Windows 的簡體中文版本獨有。  |
| 136 | 雙位元組字集 (DBCS) Windows 的唯一版本。 |
| 255 | MS-DOS 應用程式通常會顯示的擴充字元。                          |



 

</dd> </dl>

如需其他字元集值，請參閱 Platform SDK 檔集。

字元字提示字元中使用的預設字元集是在 Microsoft Agent 字元編輯器中定義。 您可以使用 [**IAgentBalloon：： SetFontCharSet**](iagentballoon--setfontcharset.md)來變更它。 不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字元集設定。

## <a name="see-also"></a>另請參閱

[**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md)


 

 




