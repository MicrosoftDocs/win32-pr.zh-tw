---
title: 應用程式所需的程式庫和標頭檔
description: 應用程式所需的程式庫和標頭檔
ms.assetid: 922627d5-03a8-4b5b-be00-6f2c3500dd66
keywords:
- Windows Media 裝置管理員、程式庫
- 裝置管理員，程式庫
- 程式設計指南，程式庫
- 桌面應用程式，程式庫
- 建立 Windows Media 裝置管理員應用程式、程式庫
- 程式庫
- Windows Media 裝置管理員、標頭檔
- 裝置管理員，標頭檔
- 程式設計指南，標頭檔
- 桌面應用程式，標頭檔
- 建立 Windows Media 裝置管理員應用程式，標頭檔
- 標頭檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4a8a04ee6c3fe603d52139e83f81a49d78dc45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021577"
---
# <a name="required-library-and-header-files-for-an-application"></a>應用程式所需的程式庫和標頭檔

本節會列出您必須包含的程式庫、標頭檔或 IDL 檔案，才能裝置管理員應用程式或外掛程式來開發 Windows Media。 如同 [編譯 sdk 所提供的 idl](compiling-the-idl-files-supplied-with-the-sdk.md)檔案所述，SDK 包含 idl 檔案和預先建立的標頭檔，而您的應用程式可以使用其中一種。  (請注意，某些標頭檔沒有對應的 IDL 檔案，而且您無法自行建立。 ) 如果建立您自己的 IDL 檔案，請在編譯隨附于 SDK 的 IDL 檔案中包含相依性。

並非所有應用程式都需要所有檔案;閱讀描述以瞭解您的應用程式是否需要檔案。



| 預建的標頭或程式庫       | 相等的 IDL                                | Description                                                                                                                                                                                                                                               |
|----------------------------------|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp .lib                     | 無                                          | 所有應用程式都需要。 包含 Windows Media 裝置管理員物件。                                                                                                                                                                              |
| wmvcore .lib                      | 無                                          | 使用 Windows Media 格式 SDK 物件或函式的應用程式所需。                                                                                                                                                                          |
| initguid。h                       | 無 (Platform SDK 標頭)                     | 所有應用程式都需要使用預建的 Mswmdm .h 檔案定義 **GUID** 值。 您必須在專案中只包含 initguid 一次。 此標頭會重新定義 **定義 \_ guid** 宏，以避免外部 **GUID** 命名問題。 |
| mmreg。h                          | 無 (Platform SDK 標頭)                     | 參考各種標準 Windows Media 格式定義的應用程式（例如 **WAVEFORMATEX**）所需。                                                                                                                                      |
| mswmdm。h                         | WMDM. idlicomponentauthenticate .idl<br/> | 所有應用程式都需要。 定義所有的應用程式介面，以及結構、中繼資料、錯誤和其他常數。                                                                                                                        |
| sac. h                            | 無                                          | 所有應用程式都需要。 定義 SAC 通訊協定。                                                                                                                                                                                                      |
| scclient。h                       | 無                                          | 所有應用程式都需要。 宣告 [CSecureChannelClient](csecurechannelclient-class.md) 類別。                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ c。<br/> | Wmdmlog .idl                                   | 使用 [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) 介面的應用程式所需。                                                                                                                                                                       |
| wmdrmdeviceapp。h                 | WMDRMDeviceApp .idl                            | 在裝置上更新 DRM 元件或計量播放次數的應用程式或外掛程式的必要項。                                                                                                                                                          |
| wmsdk。h                          | 無 (Windows Media Format SDK 提供)    | 使用 Windows Media 格式 SDK 方法的應用程式所需。                                                                                                                                                                                      |
| MtpExt。h                         | 無                                          | 在 MTP 裝置上呼叫 [**IWMDMDevice3：:D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) 的應用程式所需。 定義各種標準 MTP 常數和結構。                                                                          |
| C。                            | 無                                          | 定義來自 Microsoft 的金鑰和憑證。 SDK 隨附的版本包含測試虛擬機器碼，可讓您使用非 DRM 保護的 Windows Media 檔案。                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 





