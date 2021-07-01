---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d847bf392709b2433b045a357a703173e2de454
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120644"
---
# <a name="iagentcharacterexgetlanguageid"></a>IAgentCharacterEx::GetLanguageID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

抓取為字元設定的語言識別項。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*
</dt> <dd>

接收字元語言識別項設定之變數的位址。

</dd> </dl>

指定字元語言識別項的長整數。 字元的語言識別項 (LANGID) 是由 Windows 定義的16位值，其中包含主要語言識別項和次要語言識別項。 下列範例是某些語言的值。 若要判斷其他語言的值，請參閱 Platform SDK 檔。



| 語言              | 識別碼     | 語言              | 識別碼     |
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
| 匈牙利文             | 0x040E |                       |        |



 

如果您未設定此字元的語言識別項，則字元的語言識別項將會是目前的系統語言識別項。

這項設定也會決定 TTS 輸出的語言、文字氣球文字、字元的快顯功能表中的命令，以及語音辨識引擎。 若要判斷是否有相容的語音辨識引擎可用於該字元的語言，請使用 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md) 或 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

> [!Note]  
> 如果語言識別項設定為支援雙向文字 (例如阿拉伯文或希伯來文) 的語言，但執行您應用程式的系統沒有安裝雙向支援，則文字會以邏輯方式出現在文字提示字元中，而不是顯示順序。

 

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx： SetLanguageID**](iagentcharacterex--setlanguageid.md)、 [**IAgentCharacterEx：： GetSRModeID**](iagentcharacterex--getsrmodeid.md)、 [**IAgentCharacterEx：： GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




