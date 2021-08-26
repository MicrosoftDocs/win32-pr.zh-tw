---
title: SDK 隨附的功能
description: SDK 隨附的功能
ms.assetid: c17de30b-d4b4-4698-accf-721b6c267769
keywords:
- 'Windows媒體裝置管理員、軟體發展工具組 (SDK) '
- '裝置管理員，軟體發展工具組 (SDK) '
- WindowsMedia 裝置管理員 SDK
- 裝置管理員 SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36e621ac4de7fee296bf9d2c3ffb4e1d357824510b37a6ded73efd66b91f38d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004898"
---
# <a name="whats-included-with-the-sdk"></a>SDK 隨附的功能

下表說明 Windows 媒體裝置管理員 SDK 的內容。 所有檔案或資料夾都有相關說明，與根 SDK 安裝路徑有關。



| 檔案                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM\\                     | Windows 媒體裝置管理員 SDK 的最上層資料夾。 此資料夾包含用來建立所有範例應用程式的 makefile。                                                                                                                                                                                                                                                                                                              |
| Idl\\                      | 資料夾，其中包含建立 Windows 媒體裝置管理員方法所需之標頭所需的所有 IDL 檔案。 不過，您可以使用 inc 資料夾中提供的標頭檔，而不是使用這些檔案 \\ 。<br/> 若要查看這些 IDL 檔案的清單，並瞭解哪些標頭檔是由哪些 IDL 檔案所建立，請參閱 [編譯 SDK 提供的 idl](compiling-the-idl-files-supplied-with-the-sdk.md)檔案。<br/> |
| inc. \\ .。<br/>       | 資料夾，其中包含定義此 SDK 中介面和資料類型的所有標頭。                                                                                                                                                                                                                                                                                                                                                         |
| mswmdm。h                   | 定義所有應用程式介面、服務提供者介面、安全內容提供者介面、錯誤碼、常數、結構和 [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) 介面。                                                                                                                                                                                                                            |
| mswmdm \_ c。                | 定義 [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) 介面。                                                                                                                                                                                                                                                                                                                                                                               |
| MtpExt。h                   | 針對呼叫 [**IWMDMDevice3：:D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol)的應用程式，定義所需的 MTP 特定結構。                                                                                                                                                                                                                                                                                                            |
| 資源。h                 | 定義 SDK 範例所使用的各種資源常數。                                                                                                                                                                                                                                                                                                                                                                                         |
| sac. h                      | 定義所有應用程式和服務提供者所需的安全驗證通道資料。                                                                                                                                                                                                                                                                                                                                                       |
| scclient。h                 | 定義所有應用程式所需的 [CSecureChannelClient](csecurechannelclient-class.md) 類別。                                                                                                                                                                                                                                                                                                                                              |
| scserver。h                 | 定義所有服務提供者所需的 [CSecureChannelServer](csecurechannelserver-class.md) 類別。                                                                                                                                                                                                                                                                                                                                         |
| wmdm \_ ver. h                | Windows 媒體裝置管理員的選用版本資訊。                                                                                                                                                                                                                                                                                                                                                                                    |
| wmdmlog .h、wmdmlog \_ c。    | 使用 [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) 介面的應用程式或服務提供者所需。                                                                                                                                                                                                                                                                                                                                           |
| wmdrmdeviceapp。h           | 處理內容計量的應用程式需要 (參閱 [計量內容使用](metering-content-usage.md)) 。                                                                                                                                                                                                                                                                                                                                  |
| wmsstd。h                   | 定義 SDK 範例所使用的 helper 宏。                                                                                                                                                                                                                                                                                                                                                                                                      |
| 自由\\                      | 保存 Windows 媒體裝置管理員程式庫的資料夾。                                                                                                                                                                                                                                                                                                                                                                                       |
| mssachlp .lib               | 所有 Windows 媒體裝置管理員應用程式和服務提供者所需的靜態程式庫。                                                                                                                                                                                                                                                                                                                                                 |
| drmcrypto .lib              | 所有 Windows 媒體裝置管理員使用 DRM 的應用程式和服務提供者所需的靜態程式庫。                                                                                                                                                                                                                                                                                                                                    |
| mdsp \\ .。。<br/>      | 包含範例服務提供者程式碼的資料夾。 如需此範例的詳細資訊，包括如何編譯和執行此範例，請參閱 [範例服務提供者](sample-service-provider.md)。                                                                                                                                                                                                                                                    |
| 應用程式 \\ .。。<br/>      | 資料夾，其中包含兩個子資料夾，其中包含 SDK 所提供之範例桌面應用程式的兩個程式碼。 如需此範例的相關資訊，包括如何進行編譯，請參閱 [範例桌面應用程式](sample-desktop-application.md)。                                                                                                                                                                                      |
| devicekit \\ .。。<br/> | 包含一組工具的資料夾，可用來測試您的可攜式裝置（使用 Windows 媒體裝置管理員11）。 測試包括裝置和檔案列舉和傳輸、DRM 功能和 MTP 合規性。 這些工具有自己的檔檔。                                                                                                                                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**開始使用**](getting-started.md)
</dt> </dl>

 

 





