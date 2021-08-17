---
description: 由於 WMI 將高效能提供者載入至 WMI 或用戶端應用程式，因此您必須將高效能提供者設計為同進程伺服器。
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: 執行 High-Performance 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecec9a7b5e5399765adaa7a0e195825493d930ece46c30af3e788795fe08ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108619"
---
# <a name="implementing-the-high-performance-interface"></a>執行 High-Performance 介面

由於 WMI 將高效能提供者載入至 WMI 或用戶端應用程式，因此您必須將高效能提供者設計為同進程伺服器。 此外，您必須在 [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) 和 [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) 介面中執行高效能的提供者方法。

您應該將高效能提供者實作為同進程伺服器。 當您在執行同進程伺服器的安全性時，您應該注意的其中一項功能就是提供者如何識別其本身的位置。 將內含式載入至 WMI 時，WMI 會使用 CLSID 將提供者具現化。 當載入至用戶端應用程式的進程時，用戶端應用程式會使用 **ClientLoadableCLSID** 屬性來具現化提供者。 藉由為 CLSID 和 **ClientLoadableCLSID** 提供不同的值，您可以允許提供者判斷它是否已載入至 WMI 或用戶端應用程式。 如果位於 WMI 進程中，提供者應該使用 **ClientLoadableCLSID** 來執行任何必要的用戶端模擬。 如果位於用戶端進程中，提供者會繼承呼叫它的執行緒存取權杖。 如需有關如何執行同進程伺服器的詳細資訊，請參閱 MSDN 的 [COM 章節](https://msdn.microsoft.com/library/aa139695.aspx) 。

作為同進程伺服器，高效能的提供者會使用重新整理程式物件將遠端用戶端的資料保持在最新的。 下表列出您必須為高效能提供者執行的方法。



| 方法                                                                                              | 功能                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IWbemHiPerfProvider::QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | 查詢                                           |
| [**IWbemHiPerfProvider::GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | 物件抓取                                  |
| [**IWbemHiPerfProvider::CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | 建立複習                               |
| [**IWbemHiPerfProvider::CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | 建立可重新整理的實例物件             |
| [**IWbemHiPerfProvider::CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | 建立可重新整理的列舉值                  |
| [**IWbemHiPerfProvider::StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | 停止重新整理列舉值或實例物件 |
| [**IWbemRefresher：： Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | 建立複習                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[讓執行個體提供者成為 High-Performance 提供者](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



