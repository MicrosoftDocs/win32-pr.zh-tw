---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec8a396c174fd251b1cc7ac8d7e9696c9b9f2d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672119"
---
# <a name="iagentcharacterexsetlanguageid"></a>IAgentCharacterEx::SetLanguageID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

設定為字元設定的語言識別項。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

字元的語言識別項設定。

</dd> </dl>

指定字元語言識別項的長整數。 字元的語言識別項 (LANGID) 是由 Windows 定義的16位值，其中包含主要語言識別項和次要語言識別項。 您可以針對指定的語言使用下列值。 如需詳細資訊，請參閱 Platform SDK 檔。



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| 阿拉伯文 (沙烏地阿拉伯)         | 0x0401 | 義大利文               | 0x0410 |
| 巴斯克文                | 0x042d | 日文              | 0x0411 |
| 簡體中文  | 0x0804 | 韓文                | 0x0412 |
| 繁體中文 | 0x0404 | 挪威文             | 0x0414 |
| 克羅埃西亞文              | 0x041A | 波蘭文                | 0x0415 |
| 捷克文                 | 0x0405 | 葡萄牙文 (葡萄牙) | 0x0816 |
| 丹麥文                | 0x0406 | 葡萄牙文 (巴西)   | 0x0416 |
| 荷蘭文                 | 0x0413 | 羅馬尼亞文              | 0x0418 |
| 英文 (英國)     | 0x0809 | 俄文               | 0x0419 |
| 英文 (美國)          | 0x0409 | 斯洛伐克文             | 0x041B |
| 芬蘭文               | 0x040B | 斯洛維尼亞文             | 0x0424 |
| 法文                | 0x040C | 西班牙文               | 0x0C0A |
| 德文                | 0x0407 | 瑞典文               | 0x041D |
| 希臘文                 | 0x0408 | 泰文                  | 0x041E |
| Hebrew                | 0x040D | 土耳其文               | 0x041F |
| 匈牙利文             | 0x040E |                       |        |



 

如果您未設定字元的語言識別項，則如果已安裝對應的代理程式語言 DLL，則其語言識別項會是目前的系統語言識別項;否則，字元的語言將會是英文 (US) 。

這個屬性也會決定文字註解文字的語言、字元快顯功能表中的命令，以及語音辨識引擎。 它也會決定 TTS 輸出的預設語言。 若要判斷是否有相容的語音引擎可用於該字元的語言，請使用 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md) 或 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)。

如果您嘗試設定字元和代理程式語言資源的語言識別項、字碼頁或語言識別項的顯示字型無法使用，則代理程式會傳回錯誤，而字元的語言識別項仍會維持在其最後一個設定。 如果語言沒有相符的語音引擎，則設定這個屬性不會傳回錯誤。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

> [!Note]  
> 如果您將字元的語言識別項設定為支援雙向文字 (例如阿拉伯文或希伯來文) ，但執行您的應用程式的系統沒有安裝雙向支援，則文字會以邏輯方式出現在文字提示字元中，而不是顯示順序。

 

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx： GetLanguageID**](iagentcharacterex--getlanguageid.md)、 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md)、 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




