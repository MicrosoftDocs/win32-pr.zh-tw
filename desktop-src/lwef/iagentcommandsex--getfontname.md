---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372296"
---
# <a name="iagentcommandsexgetfontname"></a>IAgentCommandsEx::GetFontName

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

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


 

 




