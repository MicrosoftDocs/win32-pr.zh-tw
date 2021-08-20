---
title: 錯誤訊息和通知
description: 錯誤訊息和通知
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- MCIWndGetError 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1626b48bd04d5c7311767ab277abb4cbdd9d1a6104724ca244ab9544077a4f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988556"
---
# <a name="error-messages-and-notifications"></a>錯誤訊息和通知

MCIWnd 使用 MCI 來控制播放和錄製多媒體資料的裝置。 一般情況下，MCIWnd 會在 [錯誤] 對話方塊中顯示 MCI 錯誤。 只要 MCI 命令失敗，就會產生 MCI 錯誤。 例如，如果您的應用程式嘗試使用 [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) 宏繼續暫停播放，而目前的裝置不支援 resume，則會向使用者回報錯誤。

MCIWnd 可讓您選擇兩種方式來處理錯誤訊息：

-   您可以防止錯誤訊息抵達使用者。 若要防止顯示 MCI 錯誤訊息，請 \_ 在使用 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 或 [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數建立 MCIWnd 視窗的實例時，指定 MCIWNDF NOERRORDLG 視窗樣式。
-   您可以將它們重新導向至您的應用程式以供顯示。 若要將 MCI 錯誤訊息重新導向至您的應用程式，請 \_ 在使用 **MCIWndCreate** 或 **CreateWindowEx** 建立 MCIWnd 視窗的實例時，指定 MCIWNDF NOTIFYERROR 視窗樣式。

啟用錯誤通知時，MCIWnd 會將每個通知訊息 ([**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)) 傳送至 MCIWnd 視窗父系的主要訊息處理常式。 您的應用程式必須具有訊息處理常式，才能處理它所收到的通知訊息。

您可以使用 [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) 宏來取得最新的 MCI 錯誤訊息的文字描述。 此宏會傳回應用程式定義緩衝區中的文字。 如果錯誤字串的長度超過緩衝區，MCIWnd 會截斷字串。

您可以使用 [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) 宏將所有通知路由傳送到另一個視窗。

 

 