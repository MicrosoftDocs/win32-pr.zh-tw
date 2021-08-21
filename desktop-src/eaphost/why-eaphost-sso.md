---
title: SSO EAPHost 案例總覽
description: 包含兩種案例，示範單一登入 (SSO) 已啟用要求者的優點。
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc9be7af26844004073f21154df5ac12cb44d4eaa04fddc457b729ffe5e1083
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042776"
---
# <a name="sso-eaphost-scenario-overview"></a>SSO EAPHost 案例總覽

下列主題包含兩個案例，示範單一登入 (SSO) 已啟用要求者的優點。

## <a name="about-the-scenarios"></a>關於案例

SSO 提供的功能可保留比傳統儲存在 EAP 使用者 BLOB 中更多的使用者認證資訊。 與其他認證程式不同的是，啟用 SSO 的要求者可以解決登入情況（例如 AP 漫遊）和密碼變更，而不需要使用者介入。

## <a name="sso-eap-tls-pin-caching-behavior"></a>SSO EAP-TLS PIN 快取行為

要求者可以使用以智慧卡為基礎的 EAP 方法（例如可延伸的驗證通訊協定傳輸層安全性 (EAP-TLS) ）來嘗試進行網路驗證。 在這種與類似的案例中，要求者會取得使用者的智慧卡 PIN，並取得使用者憑證以進行網路驗證，接著再呼叫本機電腦上的 WinLogin。 成功驗證之後，要求者會快取使用者 BLOB，而且不會儲存使用者 PIN 資訊。

當使用者漫遊到不同的位置會話繼續時，就必須重新驗證。 由於憑證無法儲存預先登入，使用者驗證將會失敗，而要求者會排清使用者 BLOB。 此時需要使用者 PIN 才能從智慧卡取出使用者憑證，以進行網路驗證。 因為 SSO 會快取 PIN，所以不需要使用者介入即可取出憑證。 如果沒有 SSO，EAP-TLS 就必須再次引發 PIN 集合 UI。

如需逐步方法，請參閱 [SSO EAP-TLS PIN](sso-eap-tls-pin-caching-behavior-.md)快取行為。

## <a name="sso-password-change-behavior"></a>SSO 密碼變更行為

要求者可以使用以密碼為基礎的 EAP 方法（例如 Microsoft 挑戰交握驗證通訊協定2.0 版 (CHAPv2) ，設定為使用 WinLogin 認證）來嘗試網路驗證。 在此案例中，要求者會收集一次使用者認證，並將其提供給 EAPHost 進行網路驗證。 成功驗證網路之後，要求者會針對 WinLogin 使用同一組認證。

但是，如果在未啟用 SSO 的要求者的網路驗證期間變更了使用者密碼等認證，後續的 WinLogin 呼叫將會導致失敗。 SSO 會保留新的認證，並允許成功的 WinLogin，而不需要額外的使用者介入。

如需逐步方法，請參閱 [SSO 密碼變更行為](sso-password-change-behavior-.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[SSO 和 PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




