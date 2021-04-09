---
title: CSecureChannelServer 類別
description: CSecureChannelServer 類別
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Media 裝置管理員、CSecureChannelServer 類別
- 裝置管理員，CSecureChannelServer 類別
- 服務提供者、CSecureChannelServer 類別
- 程式設計參考，CSecureChannelServer 類別
- Windows Media 裝置管理員的參考，CSecureChannelServer 類別
- CSecureChannelServer 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99efdd4d4fa245000d27b5874439375d968591e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682502"
---
# <a name="csecurechannelserver-class"></a>CSecureChannelServer 類別

**CSecureChannelServer** 類別是一個 helper 類別， (不是介面) ，可讓服務提供者或安全內容提供者使用 [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)介面來驗證應用程式、加密和解密資料，以及建立 MAC 簽章。 驗證程式會要求應用程式建立 **CSecureChannelClient** 物件，並讓服務提供者建立 **CSecureChannelServer** 物件。 **CSecureChannelClient** 和 **CSecureChannelServer** 類別是在靜態程式庫（Mssachlp）中宣告。 所有 Windows Media 裝置管理員、服務提供者和安全內容提供者介面的方法，都 \_ 可以 \_ 傳回 WMDM E NOTCERTIFIED，表示呼叫者未成功驗證。

**CSecureChannelServer** 類別會公開下列方法。



| 方法                                                            | 描述                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**DecryptParam**](/previous-versions/bb231598(v=vs.85))         | 解密參數中包含的資料。                                                 |
| [**EncryptParam**](/previous-versions/ms868509(v=msdn.10))         | 加密參數中包含的資料。                                                 |
| [**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) | 確認已成功建立安全驗證通道。            |
| [**GetAppSec**](/previous-versions/bb231601(v=vs.85))               | 抓取本機和遠端元件的應用程式安全性層級。               |
| [**GetSessionKey**](/previous-versions/bb231602(v=vs.85))       | 抓取目前的工作階段金鑰。                                                          |
| [**MACFinal**](/previous-versions/ms868513(v=msdn.10))                 | 釋放 (MAC) 通道的訊息驗證碼，並抓取最終的 MAC 值。     |
| [**MACInit**](/previous-versions/ms868514(v=msdn.10))                   | 取得 (MAC) 通道的訊息驗證碼。                                       |
| [**MACUpdate**](/previous-versions/ms868515(v=msdn.10))               | 使用參數值來更新 (MAC) 值的訊息驗證碼。                 |
| [**SACAuth**](/previous-versions/ms868516(v=msdn.10))                   | 在元件之間建立安全的已驗證通道。                              |
| [**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))   | 報告元件所支援的通訊協定。                                             |
| [**SetCertificate**](/previous-versions/ms868518(v=msdn.10))     | 指定安全驗證通道 (SAC) server 的憑證和私密金鑰。 |
| [**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))       | 設定用來與其他元件通訊的工作階段金鑰。                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CSecureChannelClient 類別**](csecurechannelclient-class.md)
</dt> <dt>

[**IComponentAuthenticate 介面**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**服務提供者的介面**](interfaces-for-service-providers.md)
</dt> <dt>

[**使用安全驗證通道**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 