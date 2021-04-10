---
description: Xenroll.dll 程式庫已從作業系統中移除，並由 CertEnroll.dll 取代。
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: 將 Xenroll.dll 對應至 CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694015"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a>將 Xenroll.dll 對應至 CertEnroll.dll

在 Windows Vista 之前，憑證註冊控制項已在 Xenroll.dll 中執行。 Xenroll.dll 程式庫已從作業系統中移除，並由 CertEnroll.dll 取代。

Xenroll.dll 嘗試執行兩個平行的介面集。 [**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll)、 [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2)、 [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)和 [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) 符合自動化規範，且與指令碼語言相容。 對應的介面（[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll)、 [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)和 [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)）無法編寫腳本，但更方便 c + + 程式設計人員。 當它們演進時，兩組介面不會保持同步。 尤其是， **ICEnroll4** 最近表示的雙重介面集會定義 **IEnroll4** 所定義的功能子集。

CertEnroll.dll 會採用一組較大型且更具結構化的 COM 介面。 下列主題討論 Xenroll.dll 如何對應至不同類型功能的 CertEnroll.dll。

-   [憑證要求功能](certificate-request-functions.md)
-   [憑證回應功能](certificate-response-functions.md)
-   [屬性函式](attribute-functions.md)
-   [擴充功能](extension-functions.md)
-   [外部屬性函式](external-property-functions.md)
-   [私用和公開金鑰函數](private-and-public-key-functions.md)
-   [密碼編譯服務提供者函數](cryptographic-service-provider-functions.md)
-   [憑證存放區功能](certificate-store-functions.md)
-   [個人資訊交換功能](personal-information-exchange-functions.md)
-   [Helper 函式](helper-functions.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用憑證註冊 API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
