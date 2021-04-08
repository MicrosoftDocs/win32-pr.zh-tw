---
title: 32位和64位互通性
description: 輔助技術應用程式需要跨進程界限進行通訊，以從 Microsoft Active Accessibility 伺服器和 Microsoft 消費者介面自動化提供者取得 UI 資訊。
ms.assetid: 8b46daed-4fd9-430c-bb4d-24be9c8015b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6897082db00e27d77d90e5fc72d5f229834ce760
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682642"
---
# <a name="32-bit-and-64-bit-interoperability"></a>32位和64位互通性

輔助技術應用程式需要跨進程界限進行通訊，以從 Microsoft Active Accessibility 伺服器和 Microsoft 消費者介面自動化提供者取得 UI 資訊。 本主題說明開發 Windows 協助工具應用程式時，您必須記住的主要處理序間通訊問題。

當應用程式使用 Windows 自動化 API 時，Microsoft Active Accessibility 和消費者介面自動化執行時間元件會自動處理與執行處理序間通訊 (IPC) 相關的所有問題和複雜性，包括當某個程式為32位，另一個進程為64位時所牽涉到的互通性問題。 Microsoft 認為在某些情況下，輔助技術應用程式可能需要使用某種形式的 IPC，而不是 Windows 自動化 API 來與 Microsoft Active Accessibility 的伺服器或消費者介面自動化提供者進行通訊。 在這些情況下，Microsoft 建議您使用 DCOM 或 Windows 訊息 (值小於 **WM \_ 使用者**) 的值，以與其他進程通訊。 如同 Windows Automation API，DCOM 和 Windows 訊息會自動為您處理所有的 IPC 問題，包括32位到64位互通性。

當 Windows Automation API、DCOM 和 Windows 訊息不是選項時，請在執行您所選擇的 IPC 方法時記住下列問題：

-   共用記憶體：使用共用記憶體時，請注意32位程式中的結構可能與64位進程中的相同結構具有不同的大小和配置。 這對於包含指標或控點的結構而言更是如此。
-   指標截斷—雖然32位應用程式可以使用 **LONGLONG** 資料類型來儲存64位值，但在某些情況下，沒有任何 Windows API 專案可讓32位應用程式從64位程式接收64位的值，或將64位值傳送至64位進程。 例如， [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) 和 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式會截斷所有指標值，讓32位應用程式保持無用的值。
-   控制碼—因為 kernel32.dll 和 user32 控制碼在32位和64位的進程中只會有32位的重大問題，因此可以在處理常式之間傳輸，而不會發生問題。 不過，Windows 定義為控制碼的某些專案其實只是包裝的指標 (例如， **HTREEITEM**) 。 如果將這些「控制碼」從64位進程傳遞至32位進程，就會遭到截斷。
-   [New-winevent](winevents-infrastructure.md) 攔截函式：若要向32位伺服器進程註冊同內容攔截函式，攔截函式必須位於32位 DLL 中。 同樣地，若要向64位伺服器進程註冊同內容攔截函式，攔截函式必須位於64位 DLL 中。 如果輔助技術應用程式嘗試使用具有不同位深度的伺服器來註冊同內容攔截函式，則事件仍會傳遞至攔截函式，但它們將會在內容外傳遞。 如需詳細資訊，請參閱 WinEvents 和 [就地](in-context-and-out-of-context-hook-functions.md)內容攔截函式。

如需有關32位和64位互通性的詳細資訊，請參閱 [處理常式互通性](/windows/desktop/WinProg64/process-interoperability)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Automation API 總覽](windows-automation-api-overview.md)
</dt> </dl>

 

 