---
title: 如何執行狀態列圖示的工具提示
description: 顯示狀態列圖示之解釋性訊息的不造成干擾方式是執行工具提示。 按一下時，工具提示就會消失，但是您也可以指定超時值。
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2bd100dc6edb2aac7b4c8c5df3781e76391ae2d9d0ad456533384ed8701f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958577"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a>如何執行狀態列圖示的工具提示

顯示狀態列圖示之解釋性訊息的不造成干擾方式是執行工具提示。 按一下時，工具提示就會消失，但是您也可以指定超時值。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="implement-tooltips-for-status-bar-icons"></a>執行狀態列圖示的工具提示

下列程式碼片段說明如何將氣球工具提示新增至狀態列圖示。


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a>備註

如需狀態列的詳細討論，請參閱 [工作列](/windows/desktop/shell/taskbar)。

若要顯示氣球工具提示，您需要 \_ 在 [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) 結構中設定 n 資訊旗標，並使用 **szInfo** 和 **uTimeout** 成員來指定工具提示文字和超時時間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工具提示控制項](using-tooltip-contro.md)
</dt> </dl>

 

 