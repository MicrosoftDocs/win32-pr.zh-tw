---
description: 憑證範例。 建立 api 認證的應用程式、安裝 SSL 憑證、伺服器憑證、透過媒體（例如網際網路或內部網路）建立不安全的憑證。
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: 憑證註冊 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511552"
---
# <a name="certificate-enrollment-api"></a>憑證註冊 API

## <a name="purpose"></a>目的

憑證註冊 API 可以用來建立用戶端應用程式，以要求憑證並安裝憑證回應。 此 API 會在從 Windows Vista 開始 CertEnroll.dll 中執行;它會取代 Xenroll.dll。

## <a name="developer-audience"></a>開發人員對象

憑證註冊 API 適用于應用程式開發人員，這些應用程式可讓使用者透過不安全的媒體（例如網際網路或內部網路）建立、要求及取出憑證。 開發人員應該熟悉 C 和 c + + 程式設計語言、元件物件模型 (COM) 和以 Windows 為基礎的程式設計環境。 雖然並非必要，但建議您瞭解密碼編譯和公開金鑰基礎結構。

## <a name="run-time-requirements"></a>執行階段需求求

從 Windows Server 2008 和 Windows Vista 開始支援憑證註冊 API。 如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                       | 描述                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於憑證註冊 API](about-the-certificate-enrollment-api.md)<br/> | 討論有關憑證要求的重要概念。<br/>                                                                                                      |
| [使用憑證註冊 API](using-the-certificate-enrollment-api.md)<br/> | 如何使用憑證註冊 API 擴充 Active Directory 憑證服務的功能。<br/>                                              |
| [憑證註冊 API 參考](certificate-enrollment-api-reference.md)<br/> | 介面、列舉和其他程式設計專案的詳細描述，這些專案可以用來註冊憑證階層中的使用者或電腦。<br/> |



 

 

 




