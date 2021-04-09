---
title: 思考方法
description: 思考方法
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842199"
---
# <a name="think-method"></a>思考方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

在「想像」的文字提示字元中，顯示指定字元的指定文字。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "*** CharacterID * * *" 的字元 ) 。考慮* *  \[ *文字*\]



| 部分   | 描述                                                       |
|--------|-------------------------------------------------------------------|
| *Text* | 選擇性。 字串，指定字元的考慮輸出。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

就像「 [**說話**](speak-method.md) 」方法一樣，「 **思考** 」方法是佇列要求，它會在文字氣球中顯示文字，但 **覺得** 單字球形球的外觀不同。 此外，氣球只支援書簽語音控制項標記 (**\\ Mrk**) 並忽略其他任何語音控制項標記。 和 **說話** 不同的是， **思考** 方法不會變更字元的動畫狀態。

[**球形球**](/windows/desktop/lwef/the-balloon-object)物件的屬性會影響 [**說**](speak-method.md)和 **思考** 方法的輸出。 例如， **氣球** 物件的 [**Enabled**](enabled-property.md) 屬性必須為 **True** ，才會顯示文字。

如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 此外，如果檔案尚未載入，伺服器會將 **要求** 物件的 [ [**狀態**](status-property.md) ] 屬性設定為 [失敗]，並提供適當的錯誤碼編號。

代理程式自動斷詞字提示字元會中斷使用空白字元的單字 (例如，空格鍵或 Tab) 。 但是，如果無法使用，它可能會中斷文字以符合氣球。 在日文、中文和泰文之類的語言中，不會使用空格來分隔單字，)  (在字元之間插入 Unicode 零寬度空白字元，以定義邏輯字組分隔。

> [!Note]  
> 使用「 [**朗讀**](speak-method.md) 」方法之前，請先設定字元的語言識別項，以確保在文字批註內顯示適當的文字。

 

 

 