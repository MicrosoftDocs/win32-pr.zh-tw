---
title: 遠端桌面閘道介面
description: 遠端桌面閘道 (RD 閘道) API 支援下列介面。 您可以使用這些介面來執行提供自訂驗證與授權的外掛程式。
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931943"
---
# <a name="remote-desktop-gateway-interfaces"></a>遠端桌面閘道介面

遠端桌面閘道 (RD 閘道) API 支援下列介面。 您可以使用這些介面來執行提供自訂驗證與授權的外掛程式。 驗證外掛程式與授權外掛程式之間沒有相依性，而且您可以在選擇的情況下，只執行一個外掛程式。

驗證外掛程式為 [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) 和 [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)。

授權外掛程式為 [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)、 [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)、 [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)和 [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

公開方法，以提供有關建立或關閉連接之會話的資訊。

</dd> <dt>

[**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

公開通知 RD 閘道有關驗證事件的方法。

</dd> <dt>

[**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

公開驗證使用者以進行 RD 閘道的方法。

</dd> <dt>

[**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

公開通知 RD 閘道有關嘗試授權連接之結果的方法。

</dd> <dt>

[**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

公開方法，以通知 RD 閘道有關嘗試授權資源的結果。

</dd> <dt>

[**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

公開授權連接和資源的方法。

</dd> </dl>

 

 




