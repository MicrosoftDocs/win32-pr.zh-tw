---
description: Windows 10 中的認證提供者
ms.assetid: BCF69196-D4E4-41D0-B372-5000FD50164B
title: Windows 10 中的認證提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38543127709007407c013a2a8ff047f7c91f4440351653061e894f4e7c2d90d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008796"
---
# <a name="credential-providers-in-windows-10"></a>Windows 10 中的認證提供者

認證提供者是使用者驗證的主要機制，它們目前是唯一的方法，可讓使用者證明登入和其他系統驗證案例所需的身分識別。 使用 Windows 10 和引入 Microsoft Passport，認證提供者比以往更重要;這些應用程式會用來驗證應用程式、網站等等。

Microsoft 提供各種不同的認證提供者作為 Windows 的一部分，例如密碼、PIN、智慧卡和 Windows Hello (指紋、臉部和鳶尾花辨識) 。 在本文中，這些稱為「系統認證提供者」。 Oem、企業和其他實體可以撰寫自己的認證提供者，並輕鬆地將其整合至 Windows。 在本文中，這些稱為「協力廠商認證提供者」。 請注意，Windows 10 中支援 V1 和 V2 認證提供者。 協力廠商認證提供者的建立者和管理員必須瞭解這些建議。

## <a name="system-credential-providers"></a>系統認證提供者

強烈建議裝置上的每個使用者，除了任何協力廠商認證提供者之外，一律至少有一個可用的系統認證提供者。 此外，在協力廠商認證提供者的設定期間，如果沒有其他可用的修復選項，則裝置上的每個使用者都應該會提示至少設定一個系統認證提供者 (;請參閱以下) 的案例 A。

### <a name="scenario-a"></a>案例 A

本機帳戶使用者已設定協力廠商認證提供者，並會定期使用它來登入裝置。 一天，使用者會將某些更新安裝到中斷協力廠商認證提供者的裝置，而且使用者在重新開機電腦之前不會察覺到這項變更。

在下次重新開機時，使用者會在登入畫面上，而且無法使用預期的協力廠商認證提供者。 如果使用者已設定系統認證提供者，使用者將能夠使用它登入電腦。 如果沒有，使用者就無法復原電腦上的帳戶。

### <a name="scenario-b"></a>案例 B

MSA/AD/AAD 帳戶使用者已設定協力廠商認證提供者，並會定期使用它來登入裝置。 一天，使用者會將某些更新安裝到中斷協力廠商認證提供者的裝置，而且使用者在重新開機電腦之前不會察覺到這項變更。

在下次重新開機時，使用者會在登入畫面上，而且無法使用預期的協力廠商認證提供者。 如果使用者已設定系統認證提供者，使用者將能夠使用它登入電腦。 或者，如果系統的密碼認證提供者可供使用，則使用者可以從遠端要求/重設密碼，並使用它來登入電腦。 如果沒有可用的選項，使用者就無法復原電腦上的帳戶。

### <a name="conclusion"></a>結論

總而言之，我們想要防止停用裝置上的所有系統認證提供者。 雖然協力廠商認證提供者可以滿足特定使用者群組的其他驗證需求，但請務必確保使用者隨時都能在發生重大變更時重新取得電腦的存取權。 系統認證提供者會提供此保證。

## <a name="custom-credential-providers"></a>自訂認證提供者

Windows 的認證提供者架構可讓開發人員建立自訂認證提供者。 當 [Winlogon](winlogon.md) 想要收集認證時，登入 UI 會查詢每個認證提供者，以瞭解其想要列舉的認證數目。 當所有提供者都列舉其磚之後，登入 UI 就會向使用者顯示。 然後，使用者會與磚互動以提供必要的認證。 登入 UI 會提交這些認證以進行驗證。 認證提供者也可以在需要認證時由認證 UI 使用。 請參閱 [**認證 \_ 提供者 \_ 使用 \_ 案例**](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario) ，以取得可支援認證提供者的案例清單。

感謝這個系統，建立比以往更容易的認證提供者。 大部分的工作都是由 [Winlogon](winlogon.md)、登入 UI 和認證 ui 的組合來處理。 若要這樣做，您必須建立自己的 [**ICredentialProvider**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider) 和 [**ICredentialProviderCredential**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential)執行。 如果您正在執行 V2 認證提供者，建議您也需要執行 [**ICredentialProviderCredential2**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential2)。

請務必注意，認證提供者不是強制性機制。 它們只是用來收集和序列化認證，並提交認證以供授權之用。 本機授權單位和驗證套件將會處理，以及任何必要的安全性強制。

結合認證提供者與支援的硬體，您可以擴充 Windows，以支援使用生物識別資訊、密碼、pin、智慧卡憑證或您選擇建立的任何自訂驗證套件來進行登入。 您也可以透過各種方式自訂使用者的登入體驗。 例如，當登入 UI 查詢認證提供者的認證提供者時，您可以指定預設磚來為使用者提供自訂的體驗。 認證提供者甚至可以設計成支援單一登入 (SSO) 、驗證使用者對安全存取點以及電腦登入。

認證提供者會在 Windows 電腦上註冊，並負責下列各項。

-   描述驗證所需的認證資訊。
-   使用任何外部驗證授權單位處理通訊和邏輯。
-   封裝互動式和網路登入的認證。

> [!TIP]
>
> 請記住，您可以在單一電腦上安裝多個認證提供者。

## <a name="wrapping-credential-providers"></a>包裝認證提供者

若要將功能加入至非原生支援的認證提供者，可以完成包裝系統認證提供者。 不建議這麼做，因為它可能會導致有問題的行為。 您可以對認證提供者進行變更，這可能會與包裝函式發生衝突，而導致使用者體驗不佳，甚至讓使用者無法進入其裝置。 這特別適用于 Windows 10 頻繁的更新步調。

如果需要認證提供者中未以原生方式包含的功能，建議的路徑是建立自訂認證提供者。 這是更穩定的方法，不會依賴系統提供者。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[認證提供者導向的 Windows 登入體驗](https://go.microsoft.com/fwlink/?LinkId=717287)
</dt> <dt>

[ICredentialProvider](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider)
</dt> <dt>

[認證 \_ 提供者 \_ 認證 \_ 序列化](/windows/desktop/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization)
</dt> <dt>

[認證 \_ 提供者 \_ 使用 \_ 案例](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario)
</dt> </dl>

 

 
