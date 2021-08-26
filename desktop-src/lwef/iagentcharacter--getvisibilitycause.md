---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdae2465ccc9e7153a0e9cc8202027137e2a7c0f07fdfb5da2a83a7c0d1ed1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962238"
---
# <a name="iagentcharactergetvisibilitycause"></a>IAgentCharacter::GetVisibilityCause

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

捕獲字元可見狀態的原因。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

接收字元上一次可見度狀態變更之原因的變數位址，將會是下列其中一項：



| 值                                                                   | 描述                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **const 不帶正負號短** **NeverShown = 0;**<br/>                 | 未顯示字元。                                                               |
| **const 不帶正負號短** **UserHid = 1;**<br/>                    | 使用者以字元的工作列圖示快顯功能表或使用語音輸入來隱藏字元。 |
| **const 不帶正負號短** **UserShowed = 2;**<br/>                 | 使用者顯示字元。                                                                  |
| **const 不帶正負號短** **ProgramHid = 3;**<br/>                 | 您的應用程式會隱藏該字元。                                                         |
| **const 不帶正負號短** **ProgramShowed = 4;**<br/>              | 您的應用程式會顯示該字元。                                                      |
| **const 不帶正負號短** **OtherProgramHid = 5;**<br/>            | 另一個應用程式會將字元隱藏。                                                      |
| **const 不帶正負號短** **OtherProgramShowed = 6;**<br/>         | 另一個應用程式會顯示該字元。                                                   |
| **const 不帶正負號短** **UserHidViaCharacterMenu = 7**<br/>     | 使用者會在字元的快顯功能表中隱藏該字元。                                    |
| **const 不帶正負號的短** **UserHidViaTaskbarIcon = UserHid**<br/> | 使用者以字元的工作列圖示快顯功能表或使用語音輸入來隱藏字元。 |



 

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentNotifySink::VisibleState**](iagentnotifysink--visiblestate.md)


 

 





