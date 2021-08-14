---
description: IX509SCEPEnrollment 介面會公開下列方法。
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: IX509SCEPEnrollment 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15fc7de6392c49bd38381771956685ba6c8427b3562e7c81c372c1bab61db49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993538"
---
# <a name="ix509scepenrollment-methods"></a>IX509SCEPEnrollment 方法

[**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)介面會公開下列方法。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                              | 描述                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRequestMessage 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | 建立含有挑戰密碼的 PKCS10 要求訊息。 要求訊息位於以 SCEP 伺服器加密憑證加密，並且由伺服器簽署憑證簽署的封包 PKCS7 中。<br/> |
| [**CreateRetrieveCertificateMessage 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | 取出先前發行的憑證。<br/>                                                                                                                                                                   |
| [**CreateRetrievePendingMessage 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | 為憑證輪詢建立訊息 (手動註冊) 。<br/>                                                                                                                                               |
| [**DeleteRequest 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | 刪除針對要求所建立的任何憑證或金鑰。<br/>                                                                                                                                                    |
| [**Initialize 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | 初始化實例以準備新的要求。<br/>                                                                                                                                                   |
| [**InitializeForPending 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | 初始化實例，以準備產生訊息以取得已發行的憑證，或為簽發者安裝先前要求的回應。<br/>                                              |
| [**ProcessResponseMessage 方法**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | 處理回應訊息並傳回訊息的處置。<br/>                                                                                                                                       |



 

 

 




