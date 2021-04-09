---
title: Microsoft 代理程式語音輸出標記
description: Microsoft 代理程式語音輸出標記
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365d4837df3e3a5afb57c355e229f21ade0b5a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840096"
---
# <a name="microsoft-agent-speech-output-tags"></a>Microsoft 代理程式語音輸出標記

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

Microsoft 代理程式服務支援透過在語音文字字串中插入的特殊標記來修改語音輸出。 這些標記可協助您變更字元輸出運算式的特性。

語音輸出標記會使用下列語法規則：

-   所有標記的開頭和結尾都是反斜線字元 (\) 。
-   標記中未啟用單一反斜線字元。 若要在標記的文字參數中包含反斜線字元，請使用雙反斜線 (\\ \) 。
-   標記不區分大小寫。 例如， \\ pit 與 \\ \\ pit 相同 \\ 。
-   標記與空白字元相依。 例如， \\ rst 與 \\ \\ rst 不同 \\ 。

除非另一個標記另有指定或修改，否則語音輸出會將標記所設定的特性保留在單一 [**說話**](speak-method.md) 方法中指定的文字內。 語音輸出會在 **說話** 方法完成之後，透過使用者定義的參數自動重設。

某些標記包含加上引號的字串。 針對某些程式設計語言（例如 Visual Basic Scripting Edition (VBScript) 和 Visual Basic），這表示您可能必須使用兩個引號來指定標記的參數，或串連雙引號字元作為字串的一部分。 後者會顯示在此 Visual Basic 範例中：


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



若為 C、c + + 和 JAVA™程式設計，請在反斜線和雙引號前面加上反斜線。 例如：


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



針對支援雙位元組字元集 (DBCS) 字元的外部語言，您可以使用雙位元組字元來指定字串參數。 但是，針對用來定義標記的所有其他參數和字元（包括標記本身），請使用單一位元組字元。

支援的標記如下：

-   [**Chr**](chr-tag.md)
-   [**環 磷 醯 胺**](ctx-tag.md)
-   [**Emp**](emp-tag.md)
-   [**Lst**](lst-tag.md)
-   [**對應**](map-tag.md)
-   [**Mrk**](mrk-tag.md)
-   [**保羅**](pau-tag.md)
-   [**坑**](pit-tag.md)
-   [**Rst**](rst-tag.md)
-   [**Spd**](spd-tag.md)
-   [**卷**](vol-tag.md)

這些標記主要是設計來調整文字轉換語音 (TTS) 產生的輸出。 只有 [**Mrk**](mrk-tag.md) 和 [**Map**](map-tag.md) 標記可以與以檔案為基礎的聲音輸出搭配使用。

> [!Note]  
> Microsoft 代理程式不支援 Microsoft 語音 SDK 中記載的所有標記。 參數也會根據選取的 TTS 引擎而有所不同。 您可以使用 [**TTSModeID**](ttsmodeid-property.md)來設定特定的 TTS 引擎。

 

 

 




