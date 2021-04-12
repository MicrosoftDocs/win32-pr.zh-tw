---
title: Style 屬性
description: Style 屬性
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300915"
---
# <a name="style-property"></a>Style 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定字元的文字球標輸出樣式。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式。***字元 (*** 」CharacterID * * * ) 。球形* 樣式 *  \[  =  *樣式*\]



| 部分    | 描述                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Style* | 表示球的輸出樣式的整數。 樣式設定是位在的位位，其中的位會對應至：球形 (位 0) 、大小為文字 (位 1) 、自動隱藏 (位 2) 、自動步調 (位 3) 、每行字元數 (位 16-23) ，以及 (位 24-31) 的行數。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

當氣球 on 樣式位設定為1時，除非使用者在 Microsoft Agent 屬性工作表中覆寫此設定，否則會在使用 [**說話**](https://www.bing.com/search?q=**Speak**) 或 [**考慮**](think-method.md) 方法時出現文字批註。 當設定為0時，不會出現球形。

當 [大小到文字] 樣式位設定為1時，[文字] 氣球會自動將球的高度大小調整為 [ [**朗讀**](https://www.bing.com/search?q=**Speak**) ] 或 [ [**想像**](think-method.md) ] 語句的文字目前大小。 當設定為0時，氣球的高度會以 [**NumberOfLines**](numberoflines-property.md) 屬性設定為基礎。 如果此樣式位設定為1，而您嘗試設定 **NumberOfLines** 屬性，則代理程式會引發錯誤。

當自動隱藏樣式位設定為1時，當語音輸出完成時，會自動隱藏文字球。 當設定為0時，氣球會保持顯示，直到下一個 [**說話**](https://www.bing.com/search?q=**Speak**) 或 [**思考**](think-method.md) 呼叫、隱藏字元或使用者按一下或拖曳字元為止。

當自動步調樣式位設定為1時，文字氣球會根據目前的輸出速率步調輸出，例如一次一個單字。 當輸出超過球的大小時，就會自動滾動先前的文字。 當設定為0時，會一次顯示 [**說**](https://www.bing.com/search?q=**Speak**) 出或 [**考慮**](think-method.md) 語句中包含的所有文字。

表示只抓取底部四個位的值，**以及****樣式** 與255所傳回的值。 設定位值， **或** 以您要設定之位的值傳回的值。 若要關閉一點， **以及** 以一補數的值傳回的值：


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



**Style** 屬性也會傳回上方單字的下個位元組中的字元數，以及上方單字之高位位元組中的行數。 雖然使用 [**CharsPerLine**](charsperline-property.md) 和 [**NumberOfLines**](numberoflines-property.md)屬性可以更輕鬆地閱讀，但是 **Style** 屬性也可讓您設定這些值。

例如，若要變更行數，請在將新值設定為新值時間 2 ^ 24 的乘積之前，先清除位24到 31 **，然後再** 將新值設定為新值 **（property）的現有** 值。


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



若要設定每行的字元數，請在將新值設定為新值時間 2 ^ 16 的產品，然後將新值新增至 Style 屬性的現有值之前，先清除位16到23（具有邏輯 **AND** 運算）。


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



即使使用者已使用 Microsoft Agent 屬性工作表停用氣球顯示，也可以設定 **樣式** 屬性。 不過，行數的值必須介於1到128之間，且每行的數位字元必須介於8到255之間。 如果您為 **Style** 屬性提供不正確值，Agent 將會引發錯誤。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

當使用 Microsoft Agent 字元編輯器來編譯字元時，這些樣式位的預設值會以其設定為基礎。

 

 




