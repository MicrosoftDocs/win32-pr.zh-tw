---
description: 系統電源狀態指出電腦的電源來源是否為系統電池或 AC 電源。 針對使用電池的電腦，系統電源狀態也會指出電池的存留期，以及電池是否正在充電。
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: 系統電源狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977316"
---
# <a name="system-power-status"></a>系統電源狀態

系統電源狀態指出電腦的電源來源是否為系統電池或 AC 電源。 針對使用電池的電腦，系統電源狀態也會指出電池的存留期，以及電池是否正在充電。

透過 [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) 函式註冊電源設定通知，即可抓取電源資訊。 此功能可讓應用程式註冊特定的電源設定，並在變更時收到通知。

> [!Note]  
> 若要查詢沒有通知的電源狀態資訊，請使用 [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)。

 

應用程式和可安裝的驅動程式通常會使用系統電源狀態來判斷是否可以繼續運作。 例如，在應用程式執行背景作業（例如將檔案壓縮或分頁）之前，它應該檢查系統是否為電池。 另一個範例是，開始進行冗長作業的應用程式應該檢查狀態，以判斷是否有足夠的電池電力來完成作業。

根據預設，系統不會在睡眠轉換期間查詢應用程式或驅動程式。

> [!Note]  
> 如果電力不足，應用程式可以要求使用者介入，或要求系統暫停本身。 您可以使用 [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) 函數來暫停系統作業。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於電源管理](about-power-management.md)
</dt> </dl>

 

 



