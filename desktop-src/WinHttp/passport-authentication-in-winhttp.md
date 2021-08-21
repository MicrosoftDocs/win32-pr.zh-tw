---
description: Microsoft Windows HTTP Services (WinHTTP) 完全支援 Microsoft Passport 驗證通訊協定的用戶端使用。 本主題提供 Passport 驗證相關的交易總覽，以及如何處理這些交易。
ms.assetid: 395d7aef-4da0-4664-8328-7d31ce58fedd
title: WinHTTP 中的 Passport 驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d6aff7f8924c307d4e21efb77bc57ebae2469e50361b57d12dce5b348555e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114297"
---
# <a name="passport-authentication-in-winhttp"></a>WinHTTP 中的 Passport 驗證

Microsoft Windows HTTP Services (WinHTTP) 完全支援 Microsoft Passport 驗證通訊協定的用戶端使用。 本主題提供 Passport 驗證相關的交易總覽，以及如何處理這些交易。

> [!Note]  
> 在 WinHTTP 5.1 中，預設會停用 Passport 驗證。

 

## <a name="passport-14"></a>Passport 1。4

Passport 是 Microsoft .NET 大樓 block 服務的核心元件。 它可讓企業在各式各樣的應用程式之間開發和提供分散式 Web 服務，並讓其成員在所有參與的網站上使用一個登入名稱和密碼。

WinHTTP 藉由執行 Passport 1.4 驗證的用戶端通訊協定，提供 Microsoft Passport 1.4 的平臺支援。 它會從與 Passport 基礎結構互動的詳細資料，以及 Windows XP 中儲存的使用者名稱和密碼，來釋出應用程式。 與使用傳統驗證配置（例如基本或摘要）不同的是，此抽象概念可讓您從開發人員的觀點來使用 Passport。

**Windows XP：****HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet 設定 \\ Passport \\ NumRegistrationRuns** 登錄機碼可識別 passport 驗證 Wizard 在需要 passport 驗證時所顯示的次數。 如果此索引鍵的值設定為大於5的數位，則不會顯示嚮導。

下列各節說明從用戶端應用程式觀點來看 Passport 驗證的相關交易。 如需伺服器端 Passport 開發，請參閱 Passport SDK 檔集總覽。

-   [初始要求](#initial-request)
-   [Passport 登入伺服器](#passport-login-server)
-   [驗證的要求](#authenticated-request)

### <a name="initial-request"></a>初始要求

當用戶端要求需要 Passport 驗證的伺服器上的資源時，伺服器會檢查要求是否有 [*票證*](glossary.md)。 如果與要求一起傳送有效的 *票證* ，伺服器會以要求的資源回應。 如果用戶端上沒有 *票證* 存在，伺服器就會以302狀態碼回應。 回應包括挑戰標頭：「WWW-驗證： Passport 1.4」。 未使用 Passport 的用戶端可能會遵循重新導向至 Passport 登入伺服器。 更先進的用戶端通常會聯繫 Passport 結點，以判斷 Passport 登入伺服器的位置。

> [!Note]  
> Microsoft Passport 網路的核心是 Passport 網站地圖，可加速 Passport 參與者網站的同步 *處理，以* 確保每個網站都具有網路設定和其他問題的最新詳細資料。 每個 Passport 元件 (Passport Manager、登入伺服器、補救伺服器等) 會定期與該結點進行通訊，以取得其所需的資訊，並與 Passport 網路中的其他元件適當地進行通訊。 這項資訊會以稱為元件設定檔或 CCD 的 XML 檔的形式抓取。

 

下圖顯示 Passport 分支機搆的初始要求。

![影像會顯示 passport 分支機搆的初始要求。](images/art-passport1.png)

### <a name="passport-login-server"></a>Passport 登入伺服器

Passport 登入伺服器會處理 Passport *網域授權* 單位中任何資源的所有 [*票證*](glossary.md)要求。 用戶端應用程式必須連線到登入伺服器才能取得適當的 *票證*，才能使用 Passport 來驗證要求。

當用戶端要求 Passport 登入伺服器的 [*票證*](glossary.md) 時，登入伺服器通常會以401狀態碼回應，指出必須提供使用者認證。 當提供這些認證時，登入伺服器會回應在伺服器上存取指定資源所需的 *票證* ，其中包含原始要求的資源。 登入伺服器也可以將用戶端重新導向至可提供所要求資源的另一部伺服器。

![影像顯示 passport 登入伺服器的用戶端票證要求。](images/art-passport2.png)

### <a name="authenticated-request"></a>驗證的要求

當用戶端具有對應至指定伺服器的 [*票證*](glossary.md) 時，這些 *票證* 會隨附于該伺服器的所有要求。 如果 *票證* 在從 Passport 登入伺服器抓取之後未曾修改過，而且 *票證* 對資源伺服器是有效的，則資源伺服器會傳送包含所要求資源的回應，以及表示使用者已通過驗證以取得未來要求的 cookie。

回應中的其他 cookie 是為了加速驗證程式。 相同 Passport 網域授權單位中伺服器上資源的相同會話中的其他要求全都包含這些額外的 cookie。 在 cookie 過期之前，不需要再次將認證傳送到登入伺服器。

![影像會顯示對 passport 登入伺服器的驗證要求。](images/art-passport3.png)

## <a name="using-passport-in-winhttp"></a>在 WinHTTP 中使用 Passport

WinHTTP 中的 Passport 驗證與其他驗證配置非常類似。 請參閱 [winHTTP 中的驗證](authentication-in-winhttp.md) ，以取得 winHTTP 中的驗證總覽。

在 WinHTTP 5.1 中，預設會停用 Passport 驗證，而且必須在使用之前以 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 明確地啟用。

WinHTTP 會在內部處理 Passport 驗證的許多交易詳細資料。 在初始要求期間，當需要驗證時，伺服器會回應302狀態碼。 302狀態碼實際上表示重新導向，而且是 Passport 通訊協定的一部分，以提供回溯相容性。 WinHTTP 會隱藏302狀態碼，並與 Passport 結點聯繫，然後連線到登入伺服器。 當登入伺服器傳送的401狀態碼要求使用者認證時，會通知 WinHTTP 應用程式。 不過，在應用程式中，它看起來就像是來自要求資源的伺服器，401狀態。 如此一來，WinHTTP 應用程式就不會察覺與其他伺服器之間的互動，而且可以使用處理其他驗證配置的相同程式碼來處理 Passport 驗證。

一般而言，WinHTTP 應用程式會藉由提供驗證認證來回應401狀態碼。 使用 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) 或 [**SetCredentials**](iwinhttprequest-setcredentials.md) 為 passport 驗證提供認證時，會實際將認證傳送到登入伺服器，而不是傳送到要求中所指定的伺服器。

不過，當回應407狀態碼時，WinHTTP 應用程式必須使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 來提供 proxy 認證，而不是 [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)。 因為 **WinHttpSetOption** 是較不安全的方式來提供認證，所以通常應該避免。

經過抓取之後， [*票證*](glossary.md) 會在內部進行管理，並會在未來的要求中自動傳送至適用的伺服器。

> [!Note]  
> WinHTTP 可讓您藉由呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函式，為 [**winHTTP \_ 選項停用 \_ \_ 功能**](option-flags.md) 旗標，並指定 WINHTTP 停用重新導向的值，以停用自動重新 [**\_ \_ 導向**](option-flags.md)。 停用重新導向不會干擾 WinHTTP 在內部為 Passport 交易處理的重新導向。

 

即使應用程式停用自動重新導向，WinHTTP 仍可順利完成 Passport 驗證。 不過，在完成 Passport 驗證之後，必須從 Passport 登入伺服器 URL 將隱含的重新導向回到原始 URL。 此重新導向不是由 302 HTTP 回應所觸發，但在 Passport 通訊協定中是隱含的。

WinHTTP 會特別處理這種隱含的重新導向。 如果應用程式已停用自動重新導向，則在這個特殊情況下，WinHTTP 要求應用程式提供 WinHTTP 「許可權」來自動重新導向。

為了在驗證之後讓 WinHTTP 重新導向回到原始 URL，應用程式必須使用 [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)註冊回呼函式。 WinHTTP 接著可以使用 WINHTTP 回呼狀態重新導向回呼來通知應用程式 \_ \_ \_ ，這可讓應用程式取消重新導向。 應用程式不需要在回呼函數中提供任何功能;回呼的註冊足以讓 WinHTTP 遵循這個特殊案例重新導向。

\_ \_ \_ 如果應用程式未設定回呼函式，則會產生錯誤 WINHTTP 登入失敗訊息。

### <a name="passport-cobranding"></a>Passport Cobranding

不同于 WinHTTP 所支援的傳統驗證配置，Passport 可以廣泛地 [*在*](glossary.md)。 收到指出挑戰的401狀態碼時，應用程式可以取出 *cobranding* 圖形和文字。 使用 WINHTTP 選項[](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) \_ \_ PASSPORT \_ cobranding \_ URL 旗標來呼叫 WinHttpQueryOption，以取出 cobranding 圖形的 URL。 使用 WINHTTP  [](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) \_ 選項 \_ PASSPORT \_ cobranding \_ text 旗標呼叫 WinHttpQueryOption，以取出 cobranding 文字。 這些專案可以用來自訂認證收集對話方塊。

### <a name="stored-user-names-and-passwords"></a>儲存的使用者名稱與密碼

WindowsXP 引進了預存使用者名稱和密碼的概念。 如果使用者的 Passport 認證是透過 **Passport 註冊嚮導** 或標準 **認證對話方塊** 來儲存，則會儲存在儲存的使用者名稱和密碼中。 在 Windows XP 或更新版本上使用 winHTTP 時，如果未明確設定認證，WinHTTP 會自動使用預存使用者名稱和密碼中的認證。 這類似于支援 NTLM/Kerberos 的預設登入認證。 不過，使用預設的 Passport 認證並不受自動登入原則設定的規定。

### <a name="disabling-passport-authentication"></a>停用 Passport 驗證

有些應用程式可能需要停用 Passport 驗證的功能。 例如，當 Passport 分支機搆以最初的302狀態碼回應時，最好是遵循指示的重新導向並轉譯 HTML Passport 驗證頁面，而不是讓 WinHTTP 在內部處理驗證。 在 WinHTTP 中停用 Passport 驗證，方法是呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函式與 winHTTP \_ 選項 [ \_ 設定 \_ PASSPORT 驗證] \_ 選項，並傳遞值 winHTTP \_ DISABLE \_ passport \_ auth。 您稍後可以使用 WINHTTP \_ 啟用 PASSPORT 驗證來重新啟用它 \_ \_ 。

使用 [**WinHttpRequest**](winhttprequest.md) 物件時，無法停用 Passport 驗證。

如本節稍早所述，在 WinHTTP 5.1 中預設會停用 Passport 驗證，而且必須在使用之前明確啟用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 。

## <a name="passport-configuration-overrides-used-for-testing"></a>用於測試的 Passport 設定覆寫

WinHTTP 依賴它從 passport 結點伺服器下載的設定資訊，以支援 Passport 1.4 驗證。 根據預設，此安全 (SSL) server nexus.passport.com，而設定資源是 rdr/pprdr .asp，也就是所謂的「即時」 passport 設定。 此資訊的格式是自訂 HTTP 標頭 "PassportURLs"，後面接著逗點分隔的屬性/值配對。

例如，"" 會傳回 https://nexus.passport.com/rdr/pprdr.asp 下列設定資訊：

``` syntax
PassportURLs: DARealm=Passport.net,
DALogin=login.passport.com/login2.asp,
DAReg=https://register.passport.com/defaultwiz.asp,
Properties=https://memberservices.passport.com/ppsecure/MSRV_EditProfile.asp,
Privacy=https://www.passport.com/consumer/privacypolicy.asp,
GeneralRedir=https://nexusrdr.passport.com/redir.asp,
Help=https://memberservices.passport.com/UI/MSRV_UI_Help.asp,
ConfigVersion=2
\r\n
```

與 WinHTTP 相關的部分是 DARealm、DALogin 和 ConfigVersion。 基於效能考慮，系統會在 WinHTTP 會話的存留期間快取它們。 這三個值可以由應用程式覆寫，而這些應用程式必須與其他 passport 基礎結構搭配運作，而非「即時」生產環境設定，方法是變更以下的適當登錄設定：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
LoginServerRealm (REG_SZ)    For example: abc.net
LoginServerUrl (REG_SZ)      For example: https://private-login.passport.com/login2.asp
ConfigVersion (REG_DWORD)    For example: 10
```

如果登錄中有 LoginServerUrl，WinHTTP 將不會與伺服器上的其他設定值連線。 在此情況下，您也應該透過登錄來設定 LoginServerRealm 和 ConfigVersion，以修正值。

基於測試目的，應用程式可能需要從私用的結點伺服器下載 passport 設定。 這可以藉由覆寫下列兩個登錄值來完成：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
NexusHost (REG_SZ)    e.g. private-nexus.passport.com
NexusObj(REG_SZ)      e.g. config/passport.asp
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WinHTTP 中的驗證](authentication-in-winhttp.md)
</dt> </dl>

 

 



