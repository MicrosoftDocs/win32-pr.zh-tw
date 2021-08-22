---
title: 啟用記錄
description: 啟用記錄
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Windows媒體裝置管理員，記錄
- 裝置管理員，記錄
- 桌面應用程式，記錄
- 服務提供者，記錄
- 程式設計指南，記錄
- logging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff937b2a3abd16f7319c3abb73a3a2159350049fff8c89d343cc5545f8a21ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585116"
---
# <a name="enabling-logging"></a>啟用記錄

WindowsMedia 裝置管理員提供可在執行時間將資訊儲存至文字檔的記錄物件。 應用程式和服務提供者的開發人員可以使用此物件，在其應用程式或服務提供者執行時，將訊息儲存在記錄檔中。 此物件在處理受 drm 保護的檔案時特別有用，因為 Windows 媒體裝置管理員將無法讓您將偵錯工具附加至處理受 drm 保護之檔案的處理常式。

記錄器是具有類別識別碼 CLSID \_ WMDMLogger 的 COM 物件，此物件會公開一個介面 [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)。 元件不需要憑證就能使用記錄物件。

根據預設，不論應用程式是否使用 **IWMDMLogger**，Windows Media 裝置管理員都會維護記錄檔。 此記錄檔是簡單的文字檔，且每個專案都包含一個專案，其前面會加上以 YYYYMMDDHHMMSS.FFFFFF 格式的時間戳記，並使用24小時的當地時間。 Windows媒體裝置管理員會記錄所有 API 呼叫，以及您藉由呼叫 **IWMDMLogger** 訊息新增的任何專案。 在呼叫 [**Reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) 之前，所有記錄檔專案都會附加至檔案，或檔案超過其大小上限。 檔案會在每次記錄作業之後自動關閉。 應用程式專案和系統專案會使用相同的記錄檔。

下列步驟顯示如何使用記錄物件：

1.  在您的專案中包含 wmdmlog。
2.  藉由呼叫 **CoCreateInstance** (CLSID \_ WMDMLogger) 並要求 **IWMDMLogger** 介面，建立記錄物件。 將介面指標指派給全域變數。
3.  藉由呼叫 [**IWMDMLogger：： IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); 驗證記錄是否已啟用。如果不是，請藉由呼叫 [**IWMDMLogger：： enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable)來啟用它。
4.  指定自訂記錄檔的名稱和大小。 這是藉由呼叫 [**IWMDMLogger：： SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) 和 [**IWMDMLogger：： SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams)來完成。
5.  在您的程式碼中，您想要在記錄檔中建立專案的位置點，呼叫 [**IWMDMLogger：： LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) ，以記錄包含變數的字串 (這個方法類似于 **wsprintf** ，方法是讓您將包含變數值的字串格式化) ，或呼叫 [**IWMDMLogger：： LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) 來記錄常數位符串。

如需範例程式碼，請參閱 [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)方法的參考頁面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式和服務提供者的一般工作**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




