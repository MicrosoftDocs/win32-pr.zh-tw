---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098a89500606482914bfb31303a2cd79cac88f6d96d17abec58c75759f7abedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976458"
---
# <a name="iagentballoonexsetnumcharsperline"></a>IAgentBalloonEx::SetNumCharsPerLine

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

設定可在字元的文字氣球中顯示的每行字元數。

-   傳回 \_ [確定] 表示作業成功。
-   \_如果參數小於8，則傳回 E INVALIDARG。

<dl> <dt>

<span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*
</dt> <dd>

要在文字提示中顯示的行數。

</dd> </dl>

最小設定為8，最大值為255。 如果 [**說話**](speak-method.md) 或 [**考慮**](think-method.md) 方法中指定的文字超過目前的球標大小，則代理程式會自動滾動氣球中的文字。

當使用 Microsoft 代理程式字元編輯器來編譯字元時，預設設定會以設定為基礎。

## <a name="see-also"></a>另請參閱

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




