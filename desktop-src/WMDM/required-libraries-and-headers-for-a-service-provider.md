---
title: 服務提供者所需的程式庫和標頭
description: 服務提供者所需的程式庫和標頭
ms.assetid: 13ef830d-c1cf-4e4c-8fbd-20b5c38b9208
keywords:
- Windows Media 裝置管理員、程式庫
- 裝置管理員，程式庫
- 程式設計指南，程式庫
- 服務提供者，程式庫
- 建立服務提供者，程式庫
- 程式庫
- Windows Media 裝置管理員、標頭檔
- 裝置管理員，標頭檔
- 程式設計指南，標頭檔
- 服務提供者，標頭檔
- 建立服務提供者，標頭檔
- 標頭檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b987d389216a3349c6797517b48c03bbb4d0f1eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301064"
---
# <a name="required-libraries-and-headers-for-a-service-provider"></a>服務提供者所需的程式庫和標頭

本節會列出您必須包含的程式庫、標頭檔或 IDL 檔案，才能裝置管理員應用程式或外掛程式來開發 Windows Media。 如同 [編譯 sdk 所提供的 idl](compiling-the-idl-files-supplied-with-the-sdk.md)檔案所述，SDK 包含 idl 檔案和預先建立的標頭檔，而您的應用程式可以使用其中一種。  (請注意，某些標頭檔沒有對應的 IDL 檔案，而且您無法自行建立。 ) 如果建立您自己的 IDL 檔案，請在編譯隨附于 SDK 的 IDL 檔案中包含相依性。

並非所有應用程式都需要所有檔案;閱讀描述以瞭解您的應用程式是否需要檔案。



| 預建的標頭或程式庫       | 相等的 IDL                                                                | Description                                                                                                                                                                                                                                                    |
|----------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mssachlp .lib                     | 無                                                                          | 所有服務提供者所需。 定義 Windows Media 裝置管理員物件。                                                                                                                                                                               |
| initguid。h                       | 無 (Platform SDK 標頭)                                                     | 所有服務提供者都需要使用預建的 Mswmdm .h 檔案定義 **GUID** 值。 您必須在專案中只包含 initguid 一次。 此標頭會重新定義 **定義 \_ guid** 宏，以避免外部 **GUID** 命名問題。 |
| mswmdm。h                         | WMDM .idl<br/> WMSP .idl<br/> icomponentauthenticate .idl<br/> | 所有服務提供者所需。 定義所有服務提供者介面、結構、中繼資料、錯誤碼和其他常數。                                                                                                                        |
| sac. h                            | 無                                                                          | 所有服務提供者所需。 定義 SAC 通訊協定。                                                                                                                                                                                                      |
| scserver。h                       | 無                                                                          | 所有服務提供者所需。 宣告 [CSecureChannelServer](csecurechannelserver-class.md) 類別。                                                                                                                                                  |
| wmdmlog. hwmdmlog \_ c。<br/> | Wmdmlog .idl                                                                   | 使用 [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger) 介面的服務提供者所需。                                                                                                                                                                       |
| wmsdk。h                          | 無 (Windows Media Format SDK 提供)                                    | 使用 Windows Media 格式 SDK 方法的服務提供者所需。                                                                                                                                                                                      |
| wmvcore .lib                      | 無                                                                          | 使用 Windows Media 格式 SDK 物件或函式的服務提供者所需。                                                                                                                                                                          |
| mmreg。h                          | 無 (Platform SDK 標頭)                                                     | 參考各種標準 Windows Media 格式定義的服務提供者（例如 **WAVEFORMATEX**）所需。                                                                                                                                      |
| MtpExt。h                         | 無                                                                          | 在 MTP 裝置上處理 [**IMDSPDevice3：:D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-deviceiocontrol) 的服務提供者所需。 定義各種標準 MTP 常數和結構。                                                                        |
| C。                            | 無                                                                          | 定義來自 Microsoft 的金鑰和憑證。 SDK 隨附的版本包含測試虛擬機器碼，可讓您使用非 DRM 保護的 Windows Media 檔案。                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立服務提供者**](creating-a-service-provider.md)
</dt> </dl>

 

 





