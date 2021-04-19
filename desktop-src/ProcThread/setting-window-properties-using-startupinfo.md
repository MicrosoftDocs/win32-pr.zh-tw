---
description: 父進程可以指定與其子進程主視窗相關聯的屬性。
ms.assetid: 12547da4-8d41-48c5-8efc-f0423f64caa7
title: 使用 STARTUPINFO 設定視窗屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff59f9ae4473174325880a863f5b1f2fc4203e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977048"
---
# <a name="setting-window-properties-using-startupinfo"></a>使用 STARTUPINFO 設定視窗屬性

父進程可以指定與其子進程主視窗相關聯的屬性。 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)函式會採用 [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)結構的指標作為其參數的其中一個。 您可以使用此結構的成員來指定子進程主視窗的特性。 **DwFlags** 成員包含一個位，可決定要使用結構的其他成員。 這可讓您指定視窗屬性之任何子集的值。 系統會針對您未指定的屬性使用預設值。 **DwFlags** 成員也可以在初始化新的進程期間，強制顯示意見反應資料指標。

若是 GUI 進程， [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) 結構會指定當新的進程第一次呼叫 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 和 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函式來建立和顯示重迭的視窗時，所要使用的預設值。 您可以指定下列預設值：

-   由 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)建立之視窗的寬度和高度（以圖元為單位）。
-   由 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)建立的視窗在螢幕座標中的位置。
-   [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)的 *nCmdShow* 參數。

若為主控台進程，請在建立新主控台時使用 [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) 結構來指定視窗屬性 (使用 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 搭配 CREATE \_ new \_ console 或 [**AllocConsole**](/windows/console/allocconsole) 函數) 。 **STARTUPINFO** 結構可以用來指定下列主控台視窗屬性：

-   新主控台視窗的大小（以字元儲存格為限）。
-   新主控台視窗的位置（以螢幕座標為單位）。
-   新主控台螢幕緩衝區的大小（以字元資料格為限）。
-   新主控台螢幕緩衝區的文字和背景色彩屬性。
-   新主控台視窗的標題。

 

 
