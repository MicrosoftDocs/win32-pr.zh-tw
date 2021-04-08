---
title: IAgentBalloon GetNumCharsPerLine
description: IAgentBalloon GetNumCharsPerLine
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022034"
---
# <a name="iagentballoongetnumcharsperline"></a>IAgentBalloon::GetNumCharsPerLine

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

抓取文字球中顯示的每一行字元平均字元數的值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*
</dt> <dd>

接收每行字元數的變數位址。

</dd> </dl>

Microsoft 代理程式伺服器會自動將顯示在文字氣球中的語音輸出行滾動。 在 Microsoft Agent 字元編輯器中，會定義字元字提示字元的每一行字元平均字元數。 應用程式無法變更它。

## <a name="see-also"></a>另請參閱

[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md)


 

 




