---
description: 下圖顯示電話語音服務提供者的一般架構，以及其相關聯的使用者介面動態連結程式庫 (UI Dll) 。
ms.assetid: b5efe57a-19b8-49c5-810f-180633ed50d2
title: " (電話語音 API) 的架構"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14423dba77af1ded38af4a6f2b896e76d28ca2cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977314"
---
# <a name="architecture-telephony-api"></a> (電話語音 API) 的架構

下圖顯示電話語音服務提供者的一般架構，以及其相關聯的使用者介面動態連結程式庫 (UI Dll) 。

![tsp 和相關聯的 ui dll](images/spuidl01.png)

服務提供者至少包含兩個元件。 服務提供者 DLL (在圖例中指定為 MAIN。TSP) 會在 TAPISRV 流程的內容中執行，並執行服務提供者的所有工作，這些工作與特定應用程式的裝置使用方式相關聯的使用者介面元素並不相關 (最有可能的情況是結合圖) 中未顯示的較低層級元件。 但與舊版 TAPI 不同的是，使用者介面程式碼已整合到服務提供者 (並執行，因為先前的架構在應用程式) 的內容中，因此服務提供者現在必須包含可執行使用者介面元素的個別元件。

當應用程式呼叫產生 UI 的 TAPI 功能時，服務提供者 UI DLL 必須匯出由 TAPI 呼叫的函式： [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)、 [**TUISPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit)、 [**TUISPI \_ PhoneConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_phoneconfigdialog)、 [**TUISPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tuispi_providerconfig)、 [**TUISPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall)和 [**TUISPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)。 這些函式中的每一個都是以參數的形式包含在 TAPI 的回呼函式的指標，其型別為 [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)，UI DLL 可用來傳達雙向 (傳送和接收資料) ，以及在 TAPISRV 進程中執行的服務提供者 DLL。 如果服務提供者曾產生自發的 UI （例如 [Unimodem **交談/掛斷** ] 對話方塊），並搭配任何不需要 UI 的 TSPI 函式 (例如，任何沒有 *hwnd* 參數) 的函式，則 UI DLL 必須匯出 [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) 和 [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)。

> [!Note]  
> 原始 TSPI UI 產生的函式 ( [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)、 [**TSPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)、 [**TSPI \_ PhoneConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_phoneconfigdialog)、 [**TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig)、 [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)和 [**TSPI providerRemove \_**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)) 已淘汰，且不會被 TAPI 呼叫。 因此，服務提供者 DLL 不需要匯出這些參數。 但是，如果服務提供者想要列為可由電話語音主控台新增的服務提供者，Windows 電話在1.4 版和更舊版本中提供的公用程式，必須匯出 **TSPI \_ providerInstall**; 如果它想要在電話語音主控台中啟用 [ [**移除**](/windows/win32/api/tapi3if/nn-tapi3if-itcollection2) ] 按鈕，則必須匯出 **TSPI \_ ProviderRemove**; 如果它想要在電話語音主控台中啟用 [ **安裝** ] 按鈕，則必須匯出 **TSPI \_ providerConfig**。 電話語音主控台會檢查服務提供者 TSP 檔案中是否有這些函式，以調整其使用者介面，以反映可執行檔作業。

 

服務提供者 DLL 必須匯出 TAPISRV 進程使用的 [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) 函式，以取得要在應用程式進程中載入的 UI DLL 名稱。 它必須匯出 [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) 函式，以接收和回應 UI DLL 中要顯示的要求，而且它必須匯出 [**TSPI \_ providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) for TAPISRV 進程，以告知服務提供者何時釋放為了產生自發 ui 而建立的關聯，以搭配未定義為向使用者呈現 UI 的函式。 服務提供者 DLL 可以使用新的 TSPI 消息 [**行 \_ SENDDIALOGINSTANCEDATA**](line-senddialoginstancedata.md)，unidirectionally 傳送資料至 UI DLL。

因為 TSPI 和 TUISPI 函式的名稱刻意定義為不同，所以服務提供者 DLL 和 UI DLL 可以是相同的 DLL 檔案（如有需要）。 在適當分割的情況下，這不一定會導致應用程式內容中不必要的記憶體使用量，而且可以簡化目前可在單一 DLL 中執行之服務提供者的安裝程式。 TAPI 只會呼叫使用 DLL 之內容適用的函式。

電話語音服務提供者和 UI DLL 都必須設計成必須記住，UI 函數可以同時從多個應用程式進程叫用。 他們也必須考慮到執行電話語音服務提供者的應用程式和 TAPI 服務可以位於 LAN 的不同電腦上。

 

 
