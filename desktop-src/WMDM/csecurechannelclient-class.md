---
title: CSecureChannelClient 類別
description: CSecureChannelClient 類別
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- WindowsMedia 裝置管理員、CSecureChannelClient 類別
- 裝置管理員，CSecureChannelClient 類別
- 桌面應用程式，CSecureChannelClient 類別
- 程式設計參考，CSecureChannelClient 類別
- Windows 媒體裝置管理員、CSecureChannelClient 類別的參考
- CSecureChannelClient 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef469c1e7a73b04124850952ef0690bd18c82ecb3fc624d08df081b7b669637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585611"
---
# <a name="csecurechannelclient-class"></a>CSecureChannelClient 類別

**CSecureChannelClient** 類別是一個 helper 類別， (不是可讓應用程式自行驗證、加密和解密資料，以及建立 mac 的介面) 。

**CSecureChannelClient** 類別會公開下列方法。



| 方法                                                            | 描述                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**身份 驗證**](/previous-versions/ms983906(v=msdn.10))         | 觸發元件之間的憑證交換以建立信任。                                              |
| [**DecryptParam**](/previous-versions/bb231586(v=vs.85))         | 解密透過參數接收的資料。                                                                               |
| [**EncryptParam**](/previous-versions/bb231587(v=vs.85))         | 加密透過參數送出的資料。                                                                         |
| [**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10)) | 確認已成功建立安全驗證通道。 應用程式不會使用這個方法。 |
| [**GetAppSec**](/previous-versions/ms868498(v=msdn.10))               | 抓取本機和遠端元件的應用程式安全性層級。                                             |
| [**GetSessionKey**](/previous-versions/bb231590(v=vs.85))       | 抓取目前的工作階段金鑰。 應用程式不會使用這個方法。                                               |
| [**MACFinal**](/previous-versions/bb231591(v=vs.85))                 | 釋放 (MAC) 通道的訊息驗證碼，並抓取最終的 MAC 值。                                   |
| [**MACInit**](/previous-versions/bb231592(v=vs.85))                   | 取得 (MAC) 通道的訊息驗證碼。                                                                     |
| [**MACUpdate**](/previous-versions/bb231593(v=vs.85))               | 將值新增至 (MAC) 的訊息驗證程式代碼。                                                                      |
| [**SetCertificate**](/previous-versions/ms868504(v=msdn.10))     | 指定安全驗證通道 (SAC) 用戶端的憑證和私密金鑰。                               |
| [**SetInterface**](/previous-versions/bb231595(v=vs.85))         | 選取用於安全驗證通道 (SAC) 通訊的介面。                                         |
| [**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))       | 設定用來與其他元件通訊的工作階段金鑰。 應用程式不會使用這個方法。         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CSecureChannelServer 類別**](csecurechannelserver-class.md)
</dt> <dt>

[**IComponentAuthenticate 介面**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**應用程式的介面**](interfaces-for-applications.md)
</dt> </dl>

 

 