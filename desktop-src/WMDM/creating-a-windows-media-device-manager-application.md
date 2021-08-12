---
title: 建立 Windows 媒體裝置管理員應用程式
description: 建立 Windows 媒體裝置管理員應用程式
ms.assetid: 6a200bd9-19dd-4130-acb4-e038b469c334
keywords:
- Windows媒體裝置管理員，建立應用程式
- 裝置管理員，建立應用程式
- Windows媒體裝置管理員，程式設計手冊
- 裝置管理員，程式設計手冊
- 桌面應用程式程式設計指南
- 程式設計手冊、Windows 媒體裝置管理員
- 程式設計指南，外掛程式
- 程式設計指南，建立應用程式
- Windows媒體裝置管理員，桌面應用程式
- 裝置管理員，桌面應用程式
- Windows媒體裝置管理員、外掛程式
- 裝置管理員、外掛程式 insp
- 外掛程式，建立
- 外掛程式，程式設計指南
- 桌面應用程式，建立
- 建立 Windows 媒體裝置管理員應用程式，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba468d4d9a04176847259087b8ba2626c2ffa3e0cac089f8433993320a7e125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585555"
---
# <a name="creating-a-windows-media-device-manager-application"></a>建立 Windows 媒體裝置管理員應用程式

本節說明如何在您的應用程式中使用 Windows 媒體裝置管理員。 這裡的「應用程式」一詞是指可執行檔（例如，媒體播放機）或 COM 外掛程式（例如計量外掛程式）。

Microsoft 包含數個 Windows XP 和 Windows Media Player 10 的服務提供者，包括 MTP 服務提供者、Windows CE 服務提供者 (，適用于執行 Windows CE 和使用 RAPI 通訊協定（例如 Pocket PC) ）的裝置，以及適用于大型儲存體分類 (services.msc) 裝置的服務提供者。 您也可以建立自己的服務提供者，以確保與您自己的裝置進行通訊;如需詳細資訊，請參閱 [建立服務提供者](creating-a-service-provider.md)。

有一些協力廠商舊版服務提供者，可處理特定制造商的非 MTP、非 RAPI 或非 SERVICES.MSC 裝置。 這些服務提供者包含在隨附于這些裝置的驅動程式磁片中。

使用 Windows 媒體裝置管理員的應用程式必須執行下列步驟。

1.  **留意與開發應用程式相關的隱私權問題。** 請參閱[隱私權聲明](privacy-statement.md)，以瞭解關於開發 Windows 媒體裝置管理員應用程式的一些隱私權問題。
2.  **包含應用程式所需的程式庫和標頭檔。** 請參閱 [應用程式所需的程式庫和標頭檔](required-library-and-header-files-for-an-application.md) ，以瞭解您需要將哪些檔案包含在專案中。
3.  **驗證應用程式並取得根 IWMDMDevice 介面。** 應用程式必須執行才能使用 Windows 媒體裝置管理員的第一個工作是自行驗證。 此程式會驗證應用程式的身分識別，以 Windows 媒體裝置管理員使用 Windows 媒體裝置管理員功能有限的虛擬憑證，或使用正式的憑證來取得完整功能。 如需詳細資訊，請參閱 [驗證應用程式](authenticating-the-application.md)。
4.  **列舉已連線的裝置。** 與裝置通訊的第一個步驟是找出哪些裝置已連線，並可存取 Windows 媒體裝置管理員。 如需詳細資訊，請參閱 [列舉裝置](enumerating-devices.md)。
5.  **檢查裝置 DRM 元件的狀態。** 若要使用受 DRM 保護的檔案，裝置必須建立在可攜式裝置的某些 Windows 媒體 DRM 版本上，而且 DRM 元件必須是最新的。 在您開始處理裝置上的檔案之前，最好先查看裝置是否支援受 DRM 保護的檔案，以及是否需要更新裝置。 如需詳細資訊，請參閱 [在應用程式中處理受保護的內容](handling-protected-content-in-the-application.md)。
6.  **探索裝置。** 找到您想要的裝置之後，您可以流覽該裝置的內容。 如需詳細資訊，請參閱 [探索裝置](exploring-a-device.md)。
7.  **從裝置讀取檔案，並將檔案寫入至裝置。** 當您知道裝置的版面配置之後，就可以開始在裝置之間傳輸檔案。 如需詳細資訊，請參閱 [從裝置讀取](reading-files-from-the-device.md) 檔案，並 [將檔案寫入至裝置](writing-files-to-the-device.md)。
8.  **在裝置上建立播放清單。** 您可以寫入至裝置的一種檔案是抽象檔，也就是其他檔案的參考集合。 雖然將抽象檔寫入裝置的功能取決於服務提供者和裝置，但通常只有 MTP 裝置具有這項功能。 如需詳細資訊，請參閱在 [裝置上建立播放清單](creating-a-playlist-on-the-device.md)。

除了這些步驟之外，您還可以在應用程式中啟用數個功能：

-   **通知。** 您可以讓應用程式在裝置與電腦連線或中斷連線時接收通知。 如需詳細資訊，請參閱 [啟用通知](enabling-notifications.md)。
-   **測 井。** Windows媒體裝置管理員使用記錄物件，將其動作的記錄儲存至本機文字檔。 您可以將訊息新增至此記錄檔，以協助您分析應用程式中的錯誤或效能。 如需詳細資訊，請參閱 [啟用記錄](enabling-logging.md)。
-   **計量內容使用方式。** 您可以針對授與此許可權的授權，取得其內容使用統計資料。 然後可以將這些統計資料傳送到 Web 服務器，以計算內容擁有者的專利款項。 如需詳細資訊，請參閱 [計量內容使用](metering-content-usage.md)方式。

**注意事項**

您的應用程式可能需要使用各種不同的裝置，包括您未開發的某些裝置，而且從未針對您的程式碼進行測試。 這些裝置可能會或可能無法精確地回應查詢和命令，或執行 MTP 或其他規格。 請務必包含健全的錯誤檢查和回溯功能來處理非預期的。 程式依舊撰寫,。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 




