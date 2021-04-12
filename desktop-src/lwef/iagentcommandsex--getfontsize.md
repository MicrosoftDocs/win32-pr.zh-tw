---
title: IAgentCommandsEx GetFontSize
description: IAgentCommandsEx GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372295"
---
# <a name="iagentcommandsexgetfontsize"></a>IAgentCommandsEx::GetFontSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

抓取字元的快顯功能表中所顯示字型的大小值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

接收字型大小之值的位址。

</dd> </dl>

當您的用戶端為輸入-主動時，所傳回字型的點大小會對應到在字元的快顯功能表中顯示文字的大小。 字型設定的預設值是根據字元語言識別項設定的功能表字型設定，如果未設定，則是使用者預設語言設定。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx：： SetFontSize**](iagentcommandsex--setfontsize.md)、 [ **IAgentCommandsEx：： SetFontName**](iagentcommandsex--setfontname.md)


 

 




