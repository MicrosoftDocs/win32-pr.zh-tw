---
title: 鍵盤喜好設定參數
description: 鍵盤喜好設定參數表示使用者依賴鍵盤而非滑鼠，因此應用程式應該會顯示其他隱藏的鍵盤介面。
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c074078cdd548b6b3614213d6086edb3f5a6a412d84e418417dc0b4fcd2800e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998478"
---
# <a name="keyboard-preference-parameter"></a>鍵盤喜好設定參數

鍵盤喜好設定參數表示使用者依賴鍵盤而非滑鼠，因此應用程式應該會顯示其他隱藏的鍵盤介面。

使用者可以使用主控台中的輕鬆存取中心來控制鍵盤喜好設定參數的設定，或使用其他應用程式來自訂環境。 應用程式會使用 **spi \_ GETKEYBOARDPREF** 和 **spi \_ SETKEYBOARDPREF** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來取得和設定鍵盤喜好設定參數。

此外，在 Windows 2000 上，使用者可以設定一個參數，指出功能表便捷鍵是否一律加上底線。 應用程式會使用 **spi \_ GETMENUUNDERLINES** 和 **spi \_ SETMENUUNDERLINES** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來取得和設定功能表底線參數。

當應用程式收到鍵盤喜好設定或功能表底線參數的 [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) 訊息時，建議應用程式呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 來更新這兩個參數的資訊。

請注意 **， \_ spi GETMENUUNDERLINES** 與 **spi \_ GETKEYBOARDCUES** 相同，且 **spi \_ SETMENUUNDERLINES** 與 **spi \_ SETKEYBOARDCUES** 相同。

 

 