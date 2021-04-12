---
description: IX509EndorsementKey 介面會公開下列方法。
ms.assetid: 536E5DE6-FF14-45C8-9227-68AF673E5FDC
title: IX509EndorsementKey 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c1eb6a96cd555d4b0a0fdcd2ad52ccf80ec4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195076"
---
# <a name="ix509endorsementkey-methods"></a>IX509EndorsementKey 方法

[**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)介面會公開下列方法。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                        | 描述                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddCertificate 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-addcertificate)<br/>               | 將簽署金鑰憑證新增至支援簽署金鑰 (KSP) 的金鑰儲存提供者。<br/>                                                                                                                                                                                     |
| [**Close 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)<br/>                                 | 關閉簽署金鑰。 您只能在成功呼叫 [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)方法之後呼叫 [**Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)方法。<br/>                                                                                              |
| [**ExportPublicKey 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-exportpublickey)<br/>             | 匯出簽署公開金鑰。<br/>                                                                                                                                                                                                                                                      |
| [**GetCertificateByIndex 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatebyindex)<br/> | 取得與指定索引之金鑰儲存提供者的簽署金鑰相關聯的簽署憑證。<br/>                                                                                                                                                              |
| [**GetCertificateCount 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatecount)<br/>     | 取得金鑰儲存提供者中簽署憑證的計數。<br/>                                                                                                                                                                                                              |
| [**Open 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)<br/>                                   | 開啟簽署金鑰。 簽署金鑰必須先開啟，您才能從簽署金鑰取得資訊、新增或移除憑證，或匯出簽署金鑰。<br/>                                                                                                  |
| [**RemoveCertificate 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)<br/>         | 從金鑰儲存提供者移除簽署金鑰相關的簽署憑證。 您只能在成功呼叫 [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)方法之後呼叫 [**RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)方法。<br/> |



 

 

 




