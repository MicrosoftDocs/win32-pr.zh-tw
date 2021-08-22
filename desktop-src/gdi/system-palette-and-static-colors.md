---
description: 一般來說，系統保留給靜態色彩的系統調色板專案無法變更。
ms.assetid: be258151-36cc-42ba-8005-ff9d8e59b894
title: 系統調色板和靜態色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ffc555331ea7ad14675b4155a76d14cc61f3bef3fa7e92b331ad89449b97884
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613378"
---
# <a name="system-palette-and-static-colors"></a>系統調色板和靜態色彩

一般來說，系統保留給靜態色彩的系統調色板專案無法變更。 應用程式可以覆寫這個預設行為，方法是使用 [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) 函式減少靜態色彩專案的數目，進而增加未使用的系統調色板專案數目。 不過，由於變更靜態色彩可能會對顯示的所有視窗產生立即且顯著的影響，因此應用程式不應該呼叫 **SetSystemPaletteUse**，除非它有最大化的視窗和輸入焦點。

當應用程式使用 SYSPAL NOSTATIC 值來呼叫 [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) 時 \_ ，系統會釋出兩個保留專案，讓這些專案在應用程式後續發現其邏輯元件時，接收新的色彩值。 其餘的兩個靜態色彩專案仍會保留下來，並設定為白色和黑色。 應用程式可以藉由呼叫 **SetSystemPaletteUse** 與 SYSPAL 靜態值來還原保留的專案 \_ 。 它可以使用 [**GetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse) 函式來探索目前的系統元件使用方式。

此外，在將系統選擇區的使用方式設定為 SYSPAL \_ NOSTATIC 之後，應用程式必須立即瞭解其邏輯調色板、呼叫 [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) 函式以儲存目前的系統色彩設定、呼叫 [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) 函式以使用黑色和白色將系統色彩設定為合理的值，最後將 [**WM \_ SYSCOLORCHANGE**](wm-syscolorchange.md) 訊息傳送至其他最上層視窗，以使用新的系統色彩進行重新繪製。 使用黑色和白色設定系統色彩時，應用程式應該確保相鄰或重迭的專案（例如視窗框架和框線）分別設定為黑色和白色。

在應用程式失去輸入焦點之前，關閉視窗或終止，它必須立即以 SYSPAL 靜態值呼叫 [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) \_ 、瞭解其邏輯調色板、將系統色彩還原為先前的值，然後傳送 [**WM \_ SYSCOLORCHANGE**](wm-syscolorchange.md) 訊息。 系統會將 [**WM \_ 油漆**](wm-paint.md) 訊息傳送至受系統色彩變更影響的任何視窗。 具有使用現有系統色彩之筆刷的應用程式應該刪除這些筆刷，然後使用新的系統色彩重新建立這些筆刷。

 

 
