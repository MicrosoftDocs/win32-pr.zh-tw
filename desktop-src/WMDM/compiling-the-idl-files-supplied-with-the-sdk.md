---
title: 編譯 SDK 提供的 IDL 檔案
description: 編譯 SDK 提供的 IDL 檔案
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows媒體裝置管理員，IDL 檔案
- 裝置管理員，IDL 檔案
- 桌面應用程式，IDL 檔案
- 服務提供者，IDL 檔案
- 程式設計指南，IDL 檔案
- IDL 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d89ae614d6e20d0b05d9b7b6f054505433f4a4d33e2f9feaff60a37f7605e9ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586337"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a>編譯 SDK 提供的 IDL 檔案

Windows Media 裝置管理員 SDK 包含這些標頭檔的標頭檔和來源 IDL 檔案。 標頭檔位於 \\ \\ SDK 安裝路徑的 inc. 資料夾中。 IDL 檔案位於 \\ idl \\ 資料夾中。

先行編譯的標頭很容易使用，而且有數個 IDL 檔案會合並成單一提供的標頭。 但是，如果您決定要從提供的 IDL 檔案處理自己的標頭檔，本主題將說明哪些 IDL 檔案會建立哪些標頭檔，以及描述每個 IDL 檔案的相依性。

**相等的 IDL 和提供的標頭檔**



| **Idl**                                                                                            | **對等提供的標頭**               | **說明**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM .idl<br/> WMSP .idl<br/> WMSCP .idl<br/> icomponentauthenticate .idl<br/> | Mswmdm。h                                     | 這四個 IDL 檔案都包含在這個單一提供的標頭中。<br/> **WMDM** 會定義所有的應用程式介面，以及所需的結構、常數和錯誤碼。<br/> **WMSP** 會定義所有服務提供者介面。<br/> **WMSCP** 會定義安全內容提供者所需的所有介面、GUID 值和常數。<br/> **icomponentauthenticate** 會定義 [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) 介面。<br/> |
| Wmdmlog .idl                                                                                        | Wmdmlog。h<br/> wmdmlog \_ c。<br/> | 定義記錄介面。<br/> 由於 IDL 檔案有問題，因此必須使用所提供的標頭檔，而不只是 .h 檔案。<br/>                                                                                                                                                                                                                                                                                                                                                |
| WMDRMDeviceApp .idl                                                                                 | Wmdrmdeviceapp。h                             | 定義應用程式所使用的 [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) 和 [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) 介面，以更新裝置上的 DRM 或裝置上的計量播放次數。                                                                                                                                                                                                                                                                                                                 |



 

**IDL 相依性**

許多提供的 IDL 檔案都有組建相依性。 如果您打算自行編譯 IDL 檔案，您必須依照下表所示的順序來處理這些外部相依性。



|   Idl                      |   相依性                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| icomponentauthenticate .idl | 匯入 "oaidl.idl .idl";<br/> \#包含 "icomponentauthenticate .idl"<br/> |
| WMDM .idl                   | 沒有外部相依性                                                         |
| WmdmLog .idl                | 沒有外部相依性                                                         |
| WMDRMDeviceApp .idl         | 沒有外部相依性                                                         |
| WMSCP .idl                  | \#包含 "WMDRMDeviceApp .idl"<br/> \#包含 "WMSP .idl"<br/>        |
| WMSP .idl                   | \#包含 "WMDM .idl"                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式和服務提供者的一般工作**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





