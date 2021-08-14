---
title: IAgentBalloonEx >setstyle
description: IAgentBalloonEx >setstyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3961bf5f32aad10c662d9dc2943f32b60fad485621b5adce32e2036e6d2d4275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478538"
---
# <a name="iagentballoonexsetstyle"></a>IAgentBalloonEx：： >setstyle

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

抓取字元的文字球標樣式設定。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*
</dt> <dd>

文字氣球的樣式設定，可以是下列任何值的組合：



| 值                                                                            | 描述                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| **const 不帶正負號的簡短****氣球 \_ 樣式 \_ BALLOONON = 0x00000001;**<br/>  | 提示支援輸出。                        |
| **const 不帶正負號的簡短****氣球 \_ 樣式 \_ SIZETOTEXT = 0x0000002;**<br/> | 氣球的高度會調整大小以容納文字輸出。 |
| **const 不帶正負號的簡短****氣球 \_ 樣式自動 \_ 隱藏 = 0x00000004;**<br/>  | 提示會自動隱藏。                        |
| **const 不帶正負號的簡短****氣球 \_ 樣式 \_ AUTOPACE = 0x00000008;**<br/>  | 文字輸出的進度是根據輸出速率。          |



 

</dd> </dl>

當設定 **BalloonOn** 樣式位時，除非使用者覆寫 Microsoft Agent 屬性工作表中的顯示，否則會在使用「 [**說話**](speak-method.md) 」或「 [**想法**](think-method.md) 」方法時出現文字提示。 未設定時，不會出現任何氣球。

當設定 **SizeToText** 樣式位時，文字批註會自動將球的高度調整為 [**說**](speak-method.md) 出或 [**考慮**](think-method.md) 方法中所指定文字的目前大小。 若未設定，則氣球的高度會以球的 [行數] 屬性設定為基礎。 此樣式位設定為1，而且嘗試使用 [**IAgentBalloonEx：： SetNumLines**](iagentballoonex--setnumlines.md) 將會產生錯誤。

設定自動 **隱藏** 樣式位時，會在短時間之後自動隱藏文字提示。 若未設定，則會顯示氣球，直到新的 [**說話**](speak-method.md) 或 [**思考**](think-method.md) 通話、隱藏字元或使用者按一下或拖曳字元為止。

當設定 **AutoPace** 樣式位時，文字氣球會根據目前的輸出速率來步調輸出，例如一次一個單字。 當輸出超過球的大小時，就會自動滾動先前的文字。 若未設定，則會同時顯示 [**說**](speak-method.md) 出或 [**考慮**](think-method.md) 語句中包含的所有文字。

您可以設定球標的樣式屬性，即使使用者已使用 Microsoft Agent 屬性工作表來停用氣球的顯示。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

當使用 Microsoft Agent 字元編輯器來編譯字元時，這些樣式位的預設值會以其設定為基礎。

## <a name="see-also"></a>另請參閱

[**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md)


 

 





