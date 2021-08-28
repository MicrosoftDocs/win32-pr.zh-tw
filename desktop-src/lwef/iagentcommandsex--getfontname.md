---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 757b2d7554f1efcee27a519b9df61b4601a237b557c3aa26b6575864144a2850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105234"
---
# <a name="iagentcommandsexgetfontname"></a>IAgentCommandsEx::GetFontName

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

抓取字元快顯功能表中所顯示字型的值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

接收字元快顯功能表中所顯示字型名稱的 BSTR 位址。

</dd> </dl>

當您的用戶端應用程式為輸入-主動時，所傳回的字型名稱會對應至在字元的快顯功能表中用來顯示文字的字型。 字型設定的預設值是根據字元語言識別項設定的功能表字型設定，如果未設定，則是使用者預設語言識別項設定。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx：： SetFontName**](iagentcommandsex--setfontname.md)、 [ **IAgentCommandsEx：： SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




