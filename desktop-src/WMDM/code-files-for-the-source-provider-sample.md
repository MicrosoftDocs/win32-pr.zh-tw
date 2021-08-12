---
title: 來源提供者範例的程式碼檔案
description: 來源提供者範例的程式碼檔案
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Windows媒體裝置管理員、範例
- 裝置管理員，範例
- Windows媒體裝置管理員、服務提供者範例
- 裝置管理員，服務提供者範例
- 服務提供者，範例
- 範例，服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c29127aebea6898868b29adb17a15c8d174e1fedfd3228bd565bf8ef4ce9c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586365"
---
# <a name="code-files-for-the-source-provider-sample"></a>來源提供者範例的程式碼檔案

範例來源提供者專案包含下列原始程式碼檔案，其中包含相關聯的標頭：



| 檔案                   | 描述                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hdsppch .cpp            | 包含標準 ATL 檔案。                                                                                                                                                                                    |
| c。                  | 包含虛擬驗證金鑰。                                                                                                                                                                            |
| loghelp .cpp            | 包含使用 **WMDMLogger** 類別記錄活動和錯誤的函式，該類別會在 WMDMLOG.dll 系統檔案中執行。                                                                         |
| MDServiceProvider .cpp  | 實 CMDServiceProvider 類別，它會實 [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) 和 IComponentAuthenticate 介面。                                                             |
| mdsp .cpp               | DLL 進入點和註冊碼。                                                                                                                                                                          |
| MDSPDevice .cpp         | 實 CMDSPDevice，這個類別會實 [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2)、 [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)和 **ISpecifyPropertyPages** 介面。                          |
| MDSPEnumDevice .cpp     | 實 CMDSPEnumDevice，這個類別會實 [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) 介面。                                                                                                  |
| MDSPEnumStorage .cpp    | 實 CMDSPEnumStorage，這個類別會實 [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) 介面。                                                                                               |
| MDSPStorage .cpp        | 實 CMDSPStorage，這個類別會實 [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2)、 [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)和 [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) 介面。                    |
| MDSPStorageGlobals .cpp | 實 CMDSPStorageGlobals，這個類別會實 [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) 介面。                                                                                      |
| MDSPutil .cpp           | 包含各種適用于裝置和檔案管理的公用程式功能。                                                                                                                                              |
| proppage .cpp           | 會 CPropPage 繼承 ATL 類別的類別，此類別會繼承 ATL 類別 **IPropertyPageImpl** (來執行 IPropertyPage) 和 **CDialogImpl**，這會繼承 atl 類別 CDialogImpl (來管理 windows 和) 的訊息。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**範例服務提供者**](sample-service-provider.md)
</dt> </dl>

 

 




