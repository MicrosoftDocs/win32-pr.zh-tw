---
description: 數據機設定功能可讓您在建立連線之前設定數據機。
ms.assetid: 67d8f3c4-0295-4028-8b12-1a5e26979df5
title: 數據機設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7abd6c5319011b8821487b6adf0351dc799e61f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847470"
---
# <a name="modem-configuration"></a>數據機設定

數據機設定功能可讓您在建立連線之前設定數據機。 應用程式可以設定數據機選項，並判斷數據機的功能，而不需使用任何數據機裝置的特定命令。 以下是應用程式在進行呼叫之前可以設定的一般功能：

-   作業的主要模式 (同步、非同步，以及是否已啟用) 的錯誤控制。
-   42個錯誤控制 (由 CCITT 建議的) 所定義，包括特定參數。 CCITT 代表國際電報與電話諮詢委員會。
-   42bis (由 CCITT 建議的 42bis) 和 MNP5 資料壓縮所定義。
-   超時選項，包括呼叫設定、非活動及緩衝的資料傳遞。

在設定數據機的設定之前，應用程式應該使用 [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) 函式來判斷數據機裝置的功能。 此函數會填入 [**COMMPROP**](/windows/desktop/api/WinBase/ns-winbase-commprop) 結構。 此結構包含適用于所有通訊裝置的一般部分，以及每個提供者子類型特有的部分。 針對數據機裝置， **COMMPROP** 結構的提供者特定部分是 [**MODEMDEVCAPS**](/windows/desktop/api/Mcx/ns-mcx-modemdevcaps) 結構。

應用程式可以使用 [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) 和 [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) 函式來取得和設定數據機目前的設定，這兩個函式都使用 [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) 結構。 此結構包含適用于所有通訊裝置的一般部分，以及每個提供者子類型特有的部分。 針對數據機裝置， **COMMCONFIG** 結構的提供者特定部分是 [**MODEMSETTINGS**](/windows/desktop/api/Mcx/ns-mcx-modemsettings) 結構。

設定數據機之後，應用程式就可以使用電話語音應用程式開發介面 (TAPI) 來實際建立連接。

數據機設定功能不提供數據機的長期管理和維護。 數據機服務提供者應該提供 [數據機設定] 對話方塊以供此用途。

 

 



