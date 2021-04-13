---
title: IAgentCharacter SetIdleOn
description: IAgentCharacter SetIdleOn
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372686"
---
# <a name="iagentcharactersetidleon"></a>IAgentCharacter::SetIdleOn

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

為字元設定自動閒置處理。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*邦*
</dt> <dd>

閒置處理旗標。 如果此參數為 **True**，Microsoft 代理程式會自動播放 **閒置** 狀態動畫。

</dd> </dl>

伺服器會自動設定最後一個動畫播放某個字元之後的時間。 當此計時器的間隔完成時，伺服器會開始 **閒置** 狀態的字元，並定期播放其相關聯的 **閒置** 動畫。 如果您想要自行管理 **閒置** 狀態動畫，請將屬性設定為 **False**。 這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md)


 

 




