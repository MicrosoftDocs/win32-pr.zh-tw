---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3951cd4a8593d5e043e1571cdf24e14fdd9d93aef690c057860c2889022aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848718"
---
# <a name="iagentballoonexsetnumlines"></a>IAgentBalloonEx::SetNumLines

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

設定可在字元的文字氣球中顯示的文字輸出行數。

-   傳回 \_ [確定] 表示作業成功。
-   \_如果參數為零，則傳回 E INVALIDARG。

<dl> <dt>

<span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*
</dt> <dd>

要在文字提示中顯示的行數。

</dd> </dl>

最小設定為1，最大值為128。 如果 [**說話**](speak-method.md) 或 [**考慮**](think-method.md) 方法中指定的文字超過目前的球標大小，則代理程式會自動滾動氣球中的文字。

如果設定了 **SizeToText** 氣球樣式位，這個方法將會失敗。

當使用 Microsoft 代理程式字元編輯器來編譯字元時，預設設定會以設定為基礎。

## <a name="see-also"></a>另請參閱

[**IAgentBalloon：： GetNumLines**](iagentballoon--getnumlines.md)、 [**IAgentBalloonEx：： GetStyle**](iagentballoonex--getstyle.md)、 [**IAgentBalloonEx：： >setstyle**](iagentballoonex--setstyle.md)


 

 




