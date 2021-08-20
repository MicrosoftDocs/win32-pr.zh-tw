---
title: EAPHost 的元件
description: 瞭解 EAPHost authentication 的三個元件。 使用 EAPHost authentication 來查看其他可用的資源。
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa86f09473b14df6dbcc8bbc667dc4a1cc1badf9e0b6dd67ac95f8d11f2bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086412"
---
# <a name="components-of-eaphost"></a>EAPHost 的元件

本主題說明 EAPHost authentication 的三個元件。

## <a name="eaphost-components"></a>EAPHost 元件

EAPHost authentication 具有下列三個元件。

-   發出驗證要求的要求者。
-   對等 (或用戶端) EAP 方法，其會在用戶端上執行特定的 EAP 方法和管理驗證會話。
-   驗證器 (或伺服器) EAP 方法，其可執行 EAP 通訊協定的伺服器端。

系統會直接從想要透過 EAPHost 驗證的應用程式呼叫要求者 Api。 不過，對等方法和驗證器方法 Api 是必須針對特定 EAP 驗證方法類型（例如 Microsoft 挑戰交握驗證通訊協定2.0 版 (CHAPv2) ）所執行的函式原型。

如果您正在撰寫將使用 EAPHost 進行驗證的應用程式，請參閱 [EAPHost 要求者 API 參考](eap-host-supplicant-api-reference.md)。

如果您要撰寫新的 EAP 驗證方法以由 EAPHost 管理，請參閱[EAPHost 對等方法 api 參考](eap-host-peer-method-api-reference.md)和[EAPHost Authenticator 方法 api](eaphost-authenticator-method-apis.md)。 請注意，您將會建立這些 Api 的實作為 EAPHost 載入之新 DLL 中公開的 Api，而不是直接呼叫它們。

 

 




