---
title: 用戶端應用程式函數
description: Windows 生物特徵辨識架構 API 所支援的用戶端應用程式開發功能。
ms.assetid: 57c9378d-b170-4ba8-8eee-8078531540d5
keywords:
- Windows 生物特徵辨識架構 API Windows 生物特徵辨識架構 API，用戶端應用程式函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a552c10bf242d87e23428a08e497fd0efaf98d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840603"
---
# <a name="client-application-functions"></a>用戶端應用程式函數

Windows 生物特徵辨識架構 API 開發用戶端應用程式時，支援下列功能。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                       | 描述                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WinBioAcquireFocus**](/windows/desktop/api/Winbio/nf-winbio-winbioacquirefocus)<br/>                                 | 取得視窗焦點。<br/>                                                                                                                                                                                                        |
| [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits)<br/>           | 以非同步方式列舉符合輸入因數類型的所有附加生物特徵辨識單位。<br/>                                                                                                                                      |
| [**WinBioAsyncEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumdatabases)<br/>                     | 以非同步方式列舉符合指定類型的所有已註冊資料庫。<br/>                                                                                                                                               |
| [**WinBioAsyncEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumserviceproviders)<br/>       | 以非同步方式傳回已安裝之生物識別服務提供者的相關資訊。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                  |
| [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges)<br/> | 開始對生物特徵辨識架構進行變更的非同步監視。<br/>                                                                                                                                                         |
| [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework)<br/>                     | 開啟生物特徵辨識架構的控制碼。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                                                       |
| [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession)<br/>                         | 以非同步方式連線到生物特徵辨識服務提供者，以及一或多個生物特徵辨識單位。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                         |
| [**WinBioCancel**](/windows/desktop/api/Winbio/nf-winbio-winbiocancel)<br/>                                             | 取消指定會話的所有擱置中生物特徵辨識作業。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                                |
| [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)<br/>                               | 會捕捉生物特徵辨識範例，並使用原始或已處理的資料 (BIR) 填滿生物特徵辨識資訊記錄。<br/>                                                                                                                    |
| [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback)<br/>       | 以非同步方式捕獲生物特徵辨識範例，並傳回 (BIR) 的生物特徵辨識資訊記錄中未經處理或已處理的資料。<br/>                                                                                                     |
| [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework)<br/>                             | 關閉先前以 [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework)開啟的 framework 控制碼。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                   |
| [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession)<br/>                                 | 關閉生物識別會話，並釋放相關聯的資源。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                                    |
| [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit)<br/>                                   | 允許呼叫者在生物特徵辨識單位上執行廠商定義的控制作業。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                              |
| [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)<br/>               | 允許呼叫者在生物特徵辨識單位上執行具有特殊許可權的廠商定義控制作業。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                   |
| [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)<br/>                             | 從範本存放區刪除生物特徵辨識範本。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                                            |
| [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin)<br/>                                   | 起始生物特徵辨識註冊順序，並建立空白的生物特徵辨識範本。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                               |
| [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture)<br/>                               | 捕捉生物特徵辨識範例，並將它新增至範本。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                                           |
| [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback)<br/>       | 以非同步方式捕獲生物特徵辨識範例，並將它新增至範本。<br/>                                                                                                                                                         |
| [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)<br/>                                 | 完成擱置的生物特徵辨識範本，並將它儲存到與用於註冊的生物識別單位相關聯的資料庫。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>      |
| [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard)<br/>                               | 結束註冊順序並捨棄擱置的生物特徵辨識範本。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                          |
| [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect)<br/>                                 | 指定當範例緩衝區中有表示多個人的資料時，您想要註冊的個人。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/> |
| [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)<br/>                     | 列舉符合輸入類型的所有附加生物特徵辨識單位。<br/>                                                                                                                                                            |
| [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)<br/>                               | 列舉符合指定之類型的所有已註冊資料庫。<br/>                                                                                                                                                              |
| [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)<br/>                           | 抓取為指定身分識別和生物特徵辨識單位註冊的生物特徵辨識子要素。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                        |
| [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)<br/>                 | 抓取已安裝生物特徵辨識服務提供者的相關資訊。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                               |
| [**WinBioFree**](/windows/desktop/api/Winbio/nf-winbio-winbiofree)<br/>                                                 | 藉由稍早的 Windows 生物特徵辨識架構 API 函式呼叫，釋放為用戶端應用程式所配置的記憶體。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>           |
| [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)<br/>                     | 取得值，這個值會指定是否已為指定的使用者設定認證。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                       |
| [**WinBioGetDomainLogonSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetdomainlogonsetting)<br/>               | 抓取值，這個值會指定使用者是否可以使用生物特徵辨識資訊登入網域。<br/>                                                                                                                         |
| [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting)<br/>                       | 抓取值，這個值會指定 Windows 生物特徵辨識架構目前是否已啟用。<br/>                                                                                                                                |
| [**WinBioGetEnrolledFactors**](/windows/desktop/api/winbio/nf-winbio-winbiogetenrolledfactors)<br/>                     | 取得指定使用者在電腦上的生物識別註冊的相關資訊。<br/>                                                                                                                                 |
| [**WinBioGetLogonSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetlogonsetting)<br/>                           | 抓取值，指出使用者是否可以使用生物特徵辨識資訊登入。<br/>                                                                                                                                     |
| [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)<br/>                                   | 抓取會話、單位或範本屬性。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                                                 |
| [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)<br/>                                         | 捕捉生物特徵辨識範例，並判斷它是否符合現有的生物特徵辨識範本。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                    |
| [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback)<br/>                 | 以非同步方式捕獲生物特徵辨識範例，並判斷它是否符合現有的生物特徵辨識範本。<br/>                                                                                                                  |
| [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor)<br/>                                 | 抓取使用者以互動方式選取的生物特徵辨識單位 ID 編號。<br/>                                                                                                                                                 |
| [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback)<br/>         | 以非同步方式抓取使用者以互動方式選取的生物特徵辨識單位 ID 編號。<br/>                                                                                                                                |
| [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit)<br/>                                         | 鎖定單一會話專屬使用的生物特徵辨識單位。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                                    |
| [**WinBioLogonIdentifiedUser**](/windows/desktop/api/Winbio/nf-winbio-winbiologonidentifieduser)<br/>                   | 導致快速使用者切換至與生物識別會話所執行之上次成功識別作業相關聯的帳戶。<br/>                                                                                     |
| [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)<br/>                           | 為指定的生物識別單位開啟臉部辨識或鳶尾花監視機制。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                     |
| [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession)<br/>                                   | 連接到生物特徵辨識服務提供者，以及一或多個生物特徵辨識單位。<br/>                                                                                                                                                     |
| [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)<br/>                 | 註冊回呼函式，以從與開啟的會話相關聯的服務提供者接收事件通知。<br/>                                                                                                       |
| [**WinBioReleaseFocus**](/windows/desktop/api/Winbio/nf-winbio-winbioreleasefocus)<br/>                                 | 釋放視窗焦點。<br/>                                                                                                                                                                                                        |
| [**WinBioRemoveAllCredentials**](/windows/desktop/api/Winbio/nf-winbio-winbioremoveallcredentials)<br/>                 | 從存放區移除所有認證。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                                                          |
| [**WinBioRemoveAllDomainCredentials**](/windows/desktop/api/Winbio/nf-winbio-winbioremovealldomaincredentials)<br/>     | 從存放區移除目前網域的所有使用者認證。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                              |
| [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)<br/>                         | 刪除指定使用者的生物識別登入認證。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                                       |
| [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)<br/>                               | 為目前的使用者儲存生物特徵辨識登入認證。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                                                                         |
| [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)<br/>                                   | 設定與生物識別會話、單位、範本或帳戶相關聯之標準屬性的值。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                           |
| [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit)<br/>                                     | 釋放指定之生物識別單位上的會話鎖定。<br/>                                                                                                                                                                    |
| [**WinBioUnregisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbiounregistereventmonitor)<br/>             | 從與開啟生物識別會話相關聯的服務提供者取消事件通知。<br/>                                                                                                                              |
| [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)<br/>                                             | 捕捉生物特徵辨識範例，並判斷範例是否對應到指定的使用者身分識別。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                        |
| [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)<br/>                     | 以非同步方式捕獲生物特徵辨識範例，並判斷範例是否對應到指定的使用者身分識別。<br/>                                                                                                      |
| [**WinBioWait**](/windows/desktop/api/Winbio/nf-winbio-winbiowait)<br/>                                                 | 封鎖呼叫端執行，直到會話的所有擱置中生物特徵辨識作業都已完成或取消為止。 從 Windows 10 開始，組建1607，此函式可用於行動映射。<br/>                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端應用程式參考](client-application-reference.md)
</dt> </dl>

 

 





