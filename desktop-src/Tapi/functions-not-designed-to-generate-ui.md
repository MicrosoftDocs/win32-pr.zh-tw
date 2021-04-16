---
description: 假設服務提供者必須在處理 lineMakeCall 或 lineDial 期間，顯示 (像是 Unimodem 或 ATSP 交談/掛斷對話方塊) 的對話方塊。
ms.assetid: 46f87947-bfcd-48ad-8c33-7ea4d9caa34c
title: 未設計為產生 UI 的函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bd7ed1395136d1a2d2a31b060127395e8804ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513372"
---
# <a name="functions-not-designed-to-generate-ui"></a>未設計為產生 UI 的函式

假設服務提供者必須在處理 [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall)或 [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial)期間，顯示 (像是 Unimodem 或 ATSP **交談/掛斷** 對話方塊) 的對話方塊。 在此情況下，它是服務提供者，而不是應用程式，它會決定必須顯示 UI。

為了在應用程式進程中叫用 UI DLL，服務提供者會呼叫 TSPI [*line \_ 事件*](/windows/win32/api/tspi/nc-tspi-lineevent) 回呼，以產生 [**一行 \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) 訊息，將指標傳遞至 [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)類型的結構。 此結構包含與 UI 相關聯的函式 **dwRequestID** ，可讓 TAPISRV 識別要產生 ui 的用戶端應用程式。

TAPISRV 會要求正確的應用程式 TAPI 實例載入 UI DLL，並在應用程式的進程內建立 UI 的執行緒。 從這個新的 UI 執行緒，TAPI 會呼叫 UI DLL 的 [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) 函式，並傳入傳入的結構中的電話語音服務提供者所指定的資料，並以 [**行 \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) 訊息傳送; ui dll 會顯示適當的對話方塊， (這對 UI DLL 和電話語音服務提供者) 之間的私用設計而言很重要。 在對話方塊關閉之前，UI DLL 不會從 **TUISPI \_ providerGenericDialog** 傳回。

電話語音服務提供者可以產生更新的資料，以便在對話方塊中顯示 (或者，如果已放棄呼叫，或藉由傳送 [**一行 \_ SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md) 訊息) 其他事件發生，則指示對話方塊關閉。 TAPISRV 會將資料傳達給 TAPI，以呼叫 UI DLL 的 [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) 函式。 這種機制提供單向的「傳送」至 UI DLL。 如果 UI DLL 想要通知電話語音服務提供者該對話方塊的結果，或取得其他資料，則可以呼叫 [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) 函式 (在) 呼叫 [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) 時所收到的指標。

當對話方塊關閉時， [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) 會返回 TAPI。 TAPI 會呼叫 [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) 來釋放 ui DLL，並結束它在應用程式內容中建立的 ui 執行緒。 然後，它會要求 TAPISRV 呼叫電話語音服務提供者的 [**TSPI \_ providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) 函式，以便在電話語音服務提供者最初傳送 [**該行 \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) 訊息時，將建立的關聯解除系結。 如果應用程式進程在 **TUISPI \_ providerGenericDialog** 傳回之前未預期地終止，也會呼叫此函式。

 

 
