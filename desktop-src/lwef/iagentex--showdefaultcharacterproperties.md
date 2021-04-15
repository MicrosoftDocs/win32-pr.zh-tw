---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463116"
---
# <a name="iagentexshowdefaultcharacterproperties"></a>IAgentEx::ShowDefaultCharacterProperties

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

顯示 [預設字元屬性] 視窗。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

視窗的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

視窗的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。

</dd> <dt>

<span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*
</dt> <dd>

預設位置旗標。 如果此參數為 **True**，Microsoft Agent 會在其顯示的最後一個位置顯示預設字元的屬性工作表視窗。

> [!Note]  
> 針對 Windows 2000，您可能需要呼叫新的 [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) API，以確保此視窗成為前景視窗。 如需有關在 Windows 2000 下設定前景視窗的詳細資訊，請參閱 Platform SDK 檔。

 

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentNotifySinkEx：:D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 