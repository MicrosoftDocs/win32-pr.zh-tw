---
title: IAgentCommandsEx GetFontSize
description: IAgentCommandsEx GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92f2ce1908ea5f37d24fb8a085204917440f61ae30feb1e596639d0240c353d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976268"
---
# <a name="iagentcommandsexgetfontsize"></a>IAgentCommandsEx::GetFontSize

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 




