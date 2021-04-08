---
title: IAgentCommandsEx SetFontName
description: IAgentCommandsEx SetFontName
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9a4b76a58fc3651c02bedc43f8d372f607c2df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671639"
---
# <a name="iagentcommandsexsetfontname"></a>IAgentCommandsEx::SetFontName

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

設定在字元的快顯功能表中顯示的字型。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*
</dt> <dd>

設定字元快顯功能表中所顯示字型的 BSTR。

</dd> </dl>

這個屬性會決定在字元的快顯功能表中用來顯示文字的字型。 字型設定的預設值是以字元語言識別項設定的功能表字型設定為基礎，如果未設定則為-使用者預設語言識別項設定。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx：： GetFontName**](iagentcommandsex--getfontname.md)、 [**IAgentCommandsEx：： GetFontSize**](iagentcommandsex--getfontsize.md)、 [**IAgentCommandsEx：： SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




