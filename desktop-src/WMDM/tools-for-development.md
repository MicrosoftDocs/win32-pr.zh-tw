---
title: 適用于開發的工具
description: 適用于開發的工具
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows媒體裝置管理員，開發工具
- 裝置管理員，開發工具
- Windows媒體裝置管理員，憑證
- 裝置管理員，憑證
- Windows媒體裝置管理員，金鑰
- 裝置管理員，金鑰
- Windows媒體裝置管理員、程式庫
- 裝置管理員，程式庫
- 'Windows媒體裝置管理員、軟體發展工具組 (SDK) '
- '裝置管理員，軟體發展工具組 (SDK) '
- WindowsMedia 裝置管理員 SDK
- 裝置管理員 SDK
- Windows Media PlayerSDK
- Windows媒體格式 SDK
- WindowsMedia Rights Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e517a97246c2bf9b2ac5670a7cf696e714777a2f5926a37e1b2d37ecbe45c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031608"
---
# <a name="tools-for-development"></a>適用于開發的工具

本節說明使用 Windows Media 裝置管理員 SDK 進行程式設計所需的各種憑證和金鑰、程式庫和 sdk。

憑證和金鑰

Windows Media 裝置管理員 SDK 隨附的測試金鑰/)  (憑證組，可供應用程式或服務提供者用來在未受保護的內容上使用 Windows 媒體裝置管理員方法。 此金鑰/憑證組可讓應用程式或服務提供者充分利用 Windows 媒體裝置管理員功能。

不過，若要開發可處理受 DRM 保護之內容的應用程式或服務提供者，您必須從[Windows 媒體授權頁面](https://www.microsoft.com/licensing/default)要求一或多個憑證 (的金鑰) 。 下列應用程式或物件需要憑證：

-   處理受 DRM 保護內容的服務提供者需要 Windows 媒體裝置管理員服務提供者憑證 (和金鑰) 
-   傳送受 DRM 保護內容的應用程式需要 Windows 媒體裝置管理員傳輸憑證 (和金鑰) 
-   播放受 DRM 保護內容的應用程式需要 DRM 憑證 (和金鑰) 。
-   授權計量元件需要計量憑證。 這是由 Windows media Rights Manager SDK 上建的授權計量服務所提供，可在 Windows 媒體授權頁面上要求。

程式庫和標頭

除了[應用程式所需](required-library-and-header-files-for-an-application.md)的程式庫和標頭檔中所述的程式庫和標頭，或是[服務提供者所需](required-libraries-and-headers-for-a-service-provider.md)的程式庫和標頭之外，先前連結至 Windows WMDRMSDK 的任何應用程式或外掛程式，都應該改為連結到 WMDRMSDKStub .lib。 此程式庫檔案是用來存取受 DRM 保護的檔案。 您也可以從 Windows 媒體授權頁面要求此程式庫。

相關 Sdk

下列 Microsoft Sdk 提供您在設計便攜媒體裝置的解決方案時可能需要的元素。



| 需要 SDK                     | 必要的 .。。                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WindowsMedia 裝置管理員 SDK | 與可攜式裝置通訊的桌面媒體播放機應用程式<br/> 可以與可攜式裝置交換檔案或資訊的桌面應用程式<br/> Windows Media Player 計量 COM 物件<br/> |
| Windows Media PlayerSDK         | Windows Media Player 外掛程式<br/> Windows Media Player 計量 COM 物件<br/> Windows Media Player 的外觀<br/>                                                                                                   |
| Windows媒體格式 SDK         | 可以建立或播放檔案 (特別是 ASF 檔案的音訊或影片播放程式) <br/> 音訊或影片編輯應用程式<br/>                                                                                               |
| WindowsMedia Rights Manager SDK | 在桌面或裝置上計量播放次數的應用程式或外掛程式。                                                                                                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**開始使用**](getting-started.md)
</dt> </dl>

 

 





