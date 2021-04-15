---
title: IAgentCommandsEx SetFontSize
description: IAgentCommandsEx SetFontSize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463016"
---
# <a name="iagentcommandsexsetfontsize"></a>IAgentCommandsEx::SetFontSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

設定在字元的快顯功能表中所顯示字型的大小。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

字型的大小。

</dd> </dl>

當您的用戶端應用程式為輸入-主動時，這個屬性會決定用來在字元的快顯功能表中顯示文字的字型的點大小。 字型設定的預設值是以字元語言識別項設定的功能表字型設定為基礎，如果未設定則為-使用者預設語言設定。 如果不是輸入-主動，用戶端應用程式的 [**命令**](/windows/desktop/lwef/the-command-object)[**標題**](caption-property.md)文字會出現在針對輸入-主動用戶端指定的點大小。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx：： GetFontSize**](iagentcommandsex--getfontsize.md)、 [**IAgentCommandsEx：： GetFontName**](iagentcommandsex--getfontname.md)、 [**IAgentCommandsEx：： SetFontName**](iagentcommandsex--setfontname.md)


 

 