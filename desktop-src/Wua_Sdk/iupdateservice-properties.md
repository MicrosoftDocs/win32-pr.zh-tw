---
description: IUpdateService 介面會定義下列屬性。
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: IUpdateService 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff3cf92c89a5ba02b7d95f1a1c99f33de3202d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469152"
---
# <a name="iupdateservice-properties"></a>IUpdateService 屬性

[**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)介面會定義下列屬性。



| 屬性                                                              | 描述                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CanRegisterWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | 取得布林值，這個值會指出服務是否可以向自動更新註冊。    |
| [**ContentValidationCert**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | 取得用來簽署服務內容之憑證的 SHA-1 雜湊。         |
| [**ExpirationDate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | 取得授權封包檔到期的日期。                                  |
| [**IsManaged**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | 取得布林值，指出服務是否為 managed 服務。                     |
| [**IsRegisteredWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | 取得布林值，這個值會指出服務是否已向自動更新註冊。     |
| [**IsScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | 取得布林值，指出服務是否以掃描封裝為基礎。               |
| [**IssueDate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | 取得授權封包檔的發出日期。                               |
| [**Name**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | 取得服務的名稱。                                                                   |
| [**OffersWindowsUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | 取得布林值，指出目前的服務是否提供來自 Windows Update 的更新。 |
| [**RedirectUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | 取得重新導向程式封包檔的 URL。                                                   |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | 取得服務的識別碼。                                                              |
| [**ServiceUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | 取得服務的 URL。                                                                   |
| [**SetupPrefix**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | 取得安裝檔的前置詞。                                                            |



 

 

 



