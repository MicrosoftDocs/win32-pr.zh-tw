---
title: WNet 函式
description: Windows網路功能可提供用來管理網路資源的資訊與公用程式。
ms.assetid: 8a83186f-a912-4c61-8137-1f6be1f3afd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771974bcc2967ddba32439bb655173f62b8478ad367e086e620ca02825a2567f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330783"
---
# <a name="wnet-functions"></a>WNet 函式

Windows網路功能可提供用來管理網路資源的資訊與公用程式。 Windows 的網路功能可以依下列方式分組：

-   [連接函數](#connection-functions)
-   [列舉函數](#enumeration-functions)
-   [資訊函數](#information-functions)
-   [使用者函式](#user-functions)

## <a name="connection-functions"></a>連接函數

呼叫下列 WNet 連線函式，將本機裝置連線到網路資源，並取消網路連線。



| 函式                                                                     | 描述                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MultinetGetConnectionPerformance**](/windows/win32/api/winnetwk/nf-winnetwk-multinetgetconnectionperformancea) | 傳回網路資源連線的預期效能相關資訊。                                                                                                                                      |
| [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)                               | 將本機裝置連接到網路資源。  (提供與16位版本的 Windows 相容性。 )                                                                                                                    |
| [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)                             | 將本機裝置連接到網路資源。                                                                                                                                                                                 |
| [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)                             | 將本機裝置連接到網路資源。 這個函式包含一個以上的參數，而非 **WNetAddConnection2** 函式，這是一個視窗的控制碼，可供網路提供者作為對話方塊的主視窗。 |
| [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)                         | 取消網路連接。  (提供與16位版本的 Windows 相容性。 )                                                                                                                                     |
| [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)                       | 取消網路連線，讓您能夠使用持續連線的相關資訊來更新使用者設定檔。                                                                                                  |
| [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog)                         | 啟動一般流覽對話方塊，以連接到網路資源。                                                                                                                                                      |
| [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a)                       | 使用 [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) 結構啟動一般流覽對話方塊，以連接到網路資源。                                                                                  |
| [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog)                         | 啟動從網路資源中斷連線的一般流覽對話方塊。                                                                                                                                                 |
| [**WNetDisconnectDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a)                       | 開始使用 [**DISCDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-discdlgstructa) 結構，從網路資源中斷連接的一般流覽對話方塊。                                                                                   |
| [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona)                               | 抓取與本機裝置相關聯之網路資源的名稱。                                                                                                                                                     |
| [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea)                         | 針對網路資源提供以磁片磁碟機為基礎的路徑時，會傳回更通用的名稱格式。                                                                                                                               |
| [**WNetRestoreConnectionW**](/windows/win32/api/winnetwk/nf-winnetwk-wnetrestoreconnectionw)                     | 將連接還原至網路資源，並在必要時提示使用者輸入名稱和密碼。                                                                                                                      |
| [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona)                               | 將本機裝置連接到網路資源;自動選取未使用的本機裝置，以重新導向至網路資源。                                                                                               |



 

> [!Note]  
> [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)和 [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)函數支援與工作組的 Windows 相容。 不過，新的應用程式應該使用 [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) 或 [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)，以及 [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)。

 

## <a name="enumeration-functions"></a>列舉函數

呼叫下列 WNet 函式來列舉網路資源。



| 函式                                     | 描述                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)       | 結束網路資源列舉。                                                    |
| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) | 繼續列舉 **WNetOpenEnum** 函式所啟動的網路資源。 |
| [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)         | 啟動網路資源的列舉。                                             |



 

## <a name="information-functions"></a>資訊函數

呼叫下列 WNet 資訊和公用程式函式，以取得網路提供者和其他資訊。



| 函式                                                         | 描述                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora)                     | 傳回由網路提供者所報告的 WNet 函式所設定的最新錯誤碼。  |
| [**WNetGetNetworkInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa)   | 傳回與特定網路提供者相關的擴充資訊。                                     |
| [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)               | 傳回特定網路類型的提供者名稱。                                           |
| [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) | 傳回擁有資源的網路提供者，並取得資源類型的相關資訊。 |
| [**WNetGetResourceParent**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceparenta)           | 傳回網路資源的父系。                                                           |



 

## <a name="user-functions"></a>使用者函式

呼叫下列 WNet 函式，以取得與本機裝置相關聯的使用者名稱。



| 函式                           | 描述                                                                              |
|------------------------------------|------------------------------------------------------------------------------------------|
| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) | 傳回目前的預設使用者名稱，或建立連接的使用者名稱。 |



 

許多 WNet 函數會使用 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) 結構來儲存網路資源的相關資訊。

 

 