---
description: 等候調試函式
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: 等候調試函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8f1de3d19ce7408625a5ab42f230d23ce401728e9fa7cf060edae62e19fcfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049198"
---
# <a name="wait-debugging-functions"></a>等候調試函式

Microsoft DirectShow 提供數個函式來偵測無限期等候。

在零售組建中， [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md)和 [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)函式的運作方式，就像是其 Windows API 對應專案（ **WaitForMultipleObjects** 和 **WaitForSingleObject**），且具有無限逾時間隔。

在 debug 組建中，這些函數會使用全域超時值。 如果超時時間過期，函式就會觸發判斷提示。 下列登錄機碼會指定超時時間值（以毫秒為單位）：

**HKEY \_ 本機 \_ 電腦 \\ <DebugRoot> \\ <Module Name> \\ 超時**

其中 *<DebugRoot>* 是 [Debug Output 函數](debug-output-functions.md)主題所描述的登錄路徑。

如果機碼不存在，超時值會預設為無限。 您可以使用 [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) 函數來覆寫登錄專案。



| 函式                                                       | 描述                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | 設定調試超時值。                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | 等候指定物件的任何 (或所有) 都收到信號。 |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | 等候物件變成信號。                         |



 

 

 



