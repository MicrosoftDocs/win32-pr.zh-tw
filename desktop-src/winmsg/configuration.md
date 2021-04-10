---
description: 組態
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: 'Configuration (Windows 和訊息) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac66d2ba25e81582734eb13148d2651b276ea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194566"
---
# <a name="configuration-windows-and-messages"></a>Configuration (Windows 和訊息) 

*顯示元素* 是視窗的元件，以及顯示在系統顯示畫面上的顯示。 *系統計量* 是各種顯示元素的維度。 一般系統計量包括視窗框線寬度、圖示高度等等。 系統計量也會描述系統的其他層面，例如是否已安裝滑鼠、支援雙位元組字元，或是已安裝作業系統的偵錯工具版本。 [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)函式會捕獲指定的系統計量。

應用程式也可以分別使用 [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) 和 [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) 函式，來抓取和設定視窗元素（例如功能表、捲軸和按鈕）的色彩。

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)函式會捕獲或設定各種系統屬性，例如按兩下時間、螢幕保護裝置超時時間、視窗框線寬度和桌面圖案。 當應用程式使用 **SystemParametersInfo** 來設定參數時，會立即進行變更。 此功能也可讓應用程式更新使用者設定檔，因此系統重新開機時，系統將會保留系統的變更。

 

 
