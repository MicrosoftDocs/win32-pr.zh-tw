---
title: IAgentCharacterEx 考慮
description: IAgentCharacterEx 考慮
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023380"
---
# <a name="iagentcharacterexthink"></a>IAgentCharacterEx：：試想

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

以指定的文字顯示字元的考慮字組氣球。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

要在字元的考慮氣球中顯示的文字。

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

接收 **考慮** 要求識別碼之變數的位址。

</dd> </dl>

如同 [**IAgentCharacter：：說話**](iagentcharacter--speak.md) 方法， **考慮** 方法是佇列的要求，它會在文字氣球中顯示文字，但想法會顯示在特殊的思考球中。 想像的氣球只支援書簽語音控制項標記 (**\\ Mrk**) 並忽略其他任何語音控制項標記。 不同于 **IAgentCharacter：：說話**， **考慮** 方法不會變更字元的動畫狀態。

[**IAgentBalloon**](/windows/desktop/lwef/iagentballoon)設定也適用于考慮氣球的外觀樣式。 例如，氣球的 [**Enabled**](enabled-property.md) 屬性也必須為 **True** ，才能顯示要顯示的文字。

Microsoft Agent 自動斷詞字組會使用空白字元來中斷文字 (例如，空格鍵和 tab) 。 不過，它也可能會中斷文字以容納球。 在日文、中文和泰文之類的語言中，不會使用空格來分隔單字，)  (在字元之間插入 Unicode 零寬度空白字元，以定義邏輯字組分隔。

> [!Note]  
> 使用 [**IAgentCharacterEx：： SetLanguageID**](iagentcharacterex--setlanguageid.md) ，將字元的語言識別項設定為 (，然後再使用 [**IAgentCharacter：：**](iagentcharacter--speak.md) using 方法，以確保文字氣球內適當的文字顯示。

 

## <a name="see-also"></a>另請參閱

[**IAgentBalloon：： GetEnabled**](iagentballoon--getenabled.md)、 [**IAgentBalloonEx：： >setstyle**](iagentballoonex--setstyle.md)、 [**IAgentCharacter：：說話**](iagentcharacter--speak.md)


 

 