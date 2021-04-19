---
title: 適用于開發的工具
description: 適用于開發的工具
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Media 裝置管理員，開發工具
- 裝置管理員，開發工具
- Windows Media 裝置管理員，憑證
- 裝置管理員，憑證
- Windows Media 裝置管理員，金鑰
- 裝置管理員，金鑰
- Windows Media 裝置管理員、程式庫
- 裝置管理員，程式庫
- 'Windows Media 裝置管理員，軟體發展工具組 (SDK) '
- '裝置管理員，軟體發展工具組 (SDK) '
- Windows Media 裝置管理員 SDK
- 裝置管理員 SDK
- Windows Media Player SDK
- Windows Media Format SDK
- Windows Media Rights Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106967503"
---
# <a name="tools-for-development"></a>適用于開發的工具

本節說明使用 Windows Media 裝置管理員 SDK 進行程式設計所需的各種憑證和金鑰、程式庫和 Sdk。

憑證和金鑰

Windows Media 裝置管理員 SDK 隨附的「測試金鑰/憑證」組 (在可讓應用程式或服務提供者在未受保護的內容上使用 Windows Media 裝置管理員方法的「金鑰」/「憑證」) 。 此金鑰/憑證組可讓應用程式或服務提供者使用大部分的 Windows Media 裝置管理員功能。

不過，若要開發可處理受 DRM 保護內容的應用程式或服務提供者，您必須使用 [Windows Media 授權頁面](https://www.microsoft.com/licensing/default)中的金鑰) ，要求一或多個憑證 (。 下列應用程式或物件需要憑證：

-   處理受 DRM 保護內容的服務提供者需要 Windows Media 裝置管理員 Service Provider 憑證 (和金鑰) 
-   傳送受 DRM 保護內容的應用程式需要 Windows Media 裝置管理員傳輸憑證 (和金鑰) 
-   播放受 DRM 保護內容的應用程式需要 DRM 憑證 (和金鑰) 。
-   授權計量元件需要計量憑證。 這是由 Windows Media Rights Manager SDK 上建的授權計量服務所提供，可以在 Windows Media 授權頁面上要求。

程式庫和標頭

除了 [應用程式所需](required-library-and-header-files-for-an-application.md) 的程式庫和標頭檔中所述的程式庫和標頭，或是 [服務提供者所需](required-libraries-and-headers-for-a-service-provider.md)的程式庫和標頭之外，先前連結至 WMDRMSDK 的任何應用程式或外掛程式，都應該改為連結到 WMDRMSDKStub .lib。 此程式庫檔案是用來存取受 DRM 保護的檔案。 您也可以從 Windows Media 授權頁面要求此程式庫。

相關 Sdk

下列 Microsoft Sdk 提供您在設計便攜媒體裝置的解決方案時可能需要的元素。



| 需要 SDK                     | 必要的 .。。                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media 裝置管理員 SDK | 與可攜式裝置通訊的桌面媒體播放機應用程式<br/> 可以與可攜式裝置交換檔案或資訊的桌面應用程式<br/> Windows Media Player 計量 COM 物件<br/> |
| Windows Media Player SDK         | Windows Media Player 外掛程式<br/> Windows Media Player 計量 COM 物件<br/> Windows Media Player 的外觀<br/>                                                                                                   |
| Windows Media Format SDK         | 可以建立或播放檔案 (特別是 ASF 檔案的音訊或影片播放程式) <br/> 音訊或影片編輯應用程式<br/>                                                                                               |
| Windows Media Rights Manager SDK | 在桌面或裝置上計量播放次數的應用程式或外掛程式。                                                                                                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**開始使用**](getting-started.md)
</dt> </dl>

 

 





