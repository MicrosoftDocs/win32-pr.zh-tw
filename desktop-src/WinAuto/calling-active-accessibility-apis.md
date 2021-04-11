---
title: 呼叫 Active Accessibility Api
description: Microsoft Active Accessibility 為用戶端和伺服器提供 (Api) 的應用程式程式設計介面。
ms.assetid: c40441d2-7294-4c76-8b42-08ed66eccb7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a239495fddbcaf2275f095abc889295568b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023619"
---
# <a name="calling-active-accessibility-apis"></a>呼叫 Active Accessibility Api

Microsoft Active Accessibility 為用戶端和伺服器提供 (Api) 的應用程式程式設計介面。 大部分是在 Microsoft Active Accessibility 動態連結程式庫中執行，Oleacc.dll，但 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)、 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)和 [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) 會在 user32.dll 中執行，這是 Microsoft Windows 作業系統的核心元件。

執行 Windows 95 或 Microsoft Windows NT 4.0 的電腦未安裝 Oleacc.dll 和正確的 user32.dll 版本，因為 Microsoft Active Accessibility 已合併至 Windows 的後續版本。 因此，在這些平臺上執行的應用程式會使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式在執行時間明確連結到 Oleacc.dll，而不是依賴匯入程式庫。 Active Accessibility 1.3 支援 Windows 95 和 Microsoft Windows NT 4.0。 Microsoft Active Accessibility 不支援舊版的 Windows。

伺服器應用程式會使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來取出 Microsoft Active Accessibility 函式的位址，然後透過函式指標進行呼叫。 如果呼叫在 Oleacc.dll 中執行的函式，則伺服器應用程式會使用在調用調用中從 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)傳回的句 **柄。** 如果呼叫 user32.dll 中定義的函式，則伺服器應用程式會呼叫指定 "USER32" 的 [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) ，並在調用中使用傳回的模組控制碼來進行 **GetProcAddress**。

例如，如果應用程式使用 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)，它會使用 user32.dll 的模組控制碼來呼叫 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) ，以取得函數的位址。 如果呼叫成功 (表示這個版本的 Windows 支援 Microsoft Active Accessibility) ，則應用程式會設定旗標，指出可以安全地呼叫 **NotifyWinEvent**。 從 **GetProcAddress** 接收的位址會儲存在函式指標變數中，並在整個程式碼中使用。

 

 