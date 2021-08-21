---
title: 'MPTHREAT_CATEGORY 列舉 (MpClient .h) '
description: 可能的威脅類別。
ms.assetid: 478ED59E-5D3C-43B3-A89D-44A649EDD086
keywords:
- MPTHREAT_CATEGORY 列舉舊版 Windows 環境功能
- PMPTHREAT_CATEGORY 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_CATEGORY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70cfd95de751d51be3ab4b61bc361687738422a6d31c234576e812efcd57bd4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975968"
---
# <a name="mpthreat_category-enumeration"></a>MPTHREAT \_ 類別列舉

可能的威脅類別。

## <a name="syntax"></a>Syntax

```C++
typedef enum tagMPTHREAT_CATEGORY {
  MP_THREAT_CATEGORY_INVALID                    = 0,
  MP_THREAT_CATEGORY_ADWARE                     = 1,
  MP_THREAT_CATEGORY_SPYWARE                    = 2,
  MP_THREAT_CATEGORY_PASSWORDSTEALER            = 3,
  MP_THREAT_CATEGORY_TROJANDOWNLOADER           = 4,
  MP_THREAT_CATEGORY_WORM                       = 5,
  MP_THREAT_CATEGORY_BACKDOOR                   = 6,
  MP_THREAT_CATEGORY_REMOTEACCESSTROJAN         = 7,
  MP_THREAT_CATEGORY_TROJAN                     = 8,
  MP_THREAT_CATEGORY_EMAILFLOODER               = 9,
  MP_THREAT_CATEGORY_KEYLOGGER                  = 10,
  MP_THREAT_CATEGORY_DIALER                     = 11,
  MP_THREAT_CATEGORY_MONITORINGSOFTWARE         = 12,
  MP_THREAT_CATEGORY_BROWSERMODIFIER            = 13,
  MP_THREAT_CATEGORY_COOKIE                     = 14,
  MP_THREAT_CATEGORY_BROWSERPLUGIN              = 15,
  MP_THREAT_CATEGORY_AOLEXPLOIT                 = 16,
  MP_THREAT_CATEGORY_NUKER                      = 17,
  MP_THREAT_CATEGORY_SECURITYDISABLER           = 18,
  MP_THREAT_CATEGORY_JOKEPROGRAM                = 19,
  MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL      = 20,
  MP_THREAT_CATEGORY_SOFTWAREBUNDLER            = 21,
  MP_THREAT_CATEGORY_STEALTHNOTIFIER            = 22,
  MP_THREAT_CATEGORY_SETTINGSMODIFIER           = 23,
  MP_THREAT_CATEGORY_TOOLBAR                    = 24,
  MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE      = 25,
  MP_THREAT_CATEGORY_TROJANFTP                  = 26,
  MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE  = 27,
  MP_THREAT_CATEGORY_ICQEXPLOIT                 = 28,
  MP_THREAT_CATEGORY_TROJANTELNET               = 29,
  MP_THREAT_CATEGORY_EXPLOIT                    = 30,
  MP_THREAT_CATEGORY_FILESHARINGPROGRAM         = 31,
  MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL      = 32,
  MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE    = 33,
  MP_THREAT_CATEGORY_TOOL                       = 34,
  MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE     = 36,
  MP_THREAT_CATEGORY_TROJAN_DROPPER             = 37,
  MP_THREAT_CATEGORY_TROJAN_MASSMAILER          = 38,
  MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE  = 39,
  MP_THREAT_CATEGORY_TROJAN_PROXYSERVER         = 40,
  MP_THREAT_CATEGORY_VIRUS                      = 42,
  MP_THREAT_CATEGORY_KNOWN                      = 43,
  MP_THREAT_CATEGORY_UNKNOWN                    = 44,
  MP_THREAT_CATEGORY_SPP                        = 45,
  MP_THREAT_CATEGORY_BEHAVIOR                   = 46,
  MP_THREAT_CATEGORY_VULNERABILTIY              = 47,
  MP_THREAT_CATEGORY_POLICY                     = 48
} MPTHREAT_CATEGORY, *PMPTHREAT_CATEGORY;
```

## <a name="constants"></a>常數

威脅類別 | 描述
-|-
<span id="MP_THREAT_CATEGORY_INVALID"></span><span id="mp_threat_category_invalid"></span>**MP \_威脅 \_ 類別 \_ 無效** | 威脅類別不存在或已拼錯。
<span id="MP_THREAT_CATEGORY_ADWARE"></span><span id="mp_threat_category_adware"></span>**MP \_威脅 \_ 類別 \_ 廣告** | 顯示公告的潛在垃圾應用程式。
<span id="MP_THREAT_CATEGORY_SPYWARE"></span><span id="mp_threat_category_spyware"></span>**MP \_威脅 \_ 類別 \_ 間諜軟體** | 在沒有使用者同意或知識的情況下，傳送裝置或使用者相關資訊的惡意程式碼。
<span id="MP_THREAT_CATEGORY_PASSWORDSTEALER"></span><span id="mp_threat_category_passwordstealer"></span>**MP \_威脅 \_ 類別 \_ PASSWORDSTEALER** | 收集和/或傳送密碼給攻擊者的應用程式。
<span id="MP_THREAT_CATEGORY_TROJANDOWNLOADER"></span><span id="mp_threat_category_trojandownloader"></span>**MP \_ 威脅 \_ 類別 \_ TROJANDOWNLOADER** | 將惡意程式碼或潛在的垃圾應用程式下載到受感染裝置的特洛伊木馬程式。
<span id="MP_THREAT_CATEGORY_WORM"></span><span id="mp_threat_category_worm"></span>**MP \_威脅 \_ 類別 \_ WORM** | 自我傳播可透過網路連線自動散發的惡意軟體。
<span id="MP_THREAT_CATEGORY_BACKDOOR"></span><span id="mp_threat_category_backdoor"></span>**MP \_ 威脅 \_ 類別 \_ 後門** | 惡意程式碼，提供略過裝置上一般安全性和驗證通訊協定的方法。
<span id="MP_THREAT_CATEGORY_REMOTEACCESSTROJAN"></span><span id="mp_threat_category_remoteaccesstrojan"></span>**MP \_威脅 \_ 類別 \_ REMOTEACCESSTROJAN** | 提供電腦遠端存取的特洛伊木馬程式。
<span id="MP_THREAT_CATEGORY_TROJAN"></span><span id="mp_threat_category_trojan"></span>**MP \_ 威脅 \_ 類別 \_ 特洛伊** | 隱藏本身為合法軟體的惡意軟體。
<span id="MP_THREAT_CATEGORY_EMAILFLOODER"></span><span id="mp_threat_category_emailflooder"></span>**MP \_威脅 \_ 類別 \_ EMAILFLOODER** | 惡意程式碼會將大量電子郵件傳送至目標。
<span id="MP_THREAT_CATEGORY_KEYLOGGER"></span><span id="mp_threat_category_keylogger"></span>**MP \_威脅 \_ 類別 \_ KEYLOGGER** | 記錄使用者擊鍵的惡意程式碼，可能會竊取密碼和其他機密資料。
<span id="MP_THREAT_CATEGORY_DIALER"></span><span id="mp_threat_category_dialer"></span>**MP \_威脅 \_ 類別 \_ 撥號** 程式 | 發出未經授權通話的惡意程式碼，通常是以高階費率收費。
<span id="MP_THREAT_CATEGORY_MONITORINGSOFTWARE"></span><span id="mp_threat_category_monitoringsoftware"></span>**MP \_威脅 \_ 類別 \_ MONITORINGSOFTWARE** | 一種潛在的垃圾應用程式，可監視使用者活動，例如使用者在其鍵盤上輸入的內容或螢幕上的視圖。
<span id="MP_THREAT_CATEGORY_BROWSERMODIFIER"></span><span id="mp_threat_category_browsermodifier"></span>**MP \_威脅 \_ 類別 \_ BROWSERMODIFIER** | 在沒有使用者同意的情況下，變更網頁瀏覽器設定的潛在垃圾應用程式。
<span id="MP_THREAT_CATEGORY_COOKIE"></span><span id="mp_threat_category_cookie"></span>**MP \_威脅 \_ 類別 \_ COOKIE** | Web 服務器傳送至瀏覽器的資料，可讓它儲存使用者的相關資訊，例如 web 應用程式設定，以及重複造訪。
<span id="MP_THREAT_CATEGORY_BROWSERPLUGIN"></span><span id="mp_threat_category_browserplugin"></span>**MP \_威脅 \_ 類別 \_ BROWSERPLUGIN** | 此軟體可讓標準網頁瀏覽器顯示及執行特定類型的內容，例如媒體檔案、動畫影像和互動式形式。
<span id="MP_THREAT_CATEGORY_AOLEXPLOIT"></span><span id="mp_threat_category_aolexploit"></span>**MP \_威脅 \_ 類別 \_ AOLEXPLOIT** | 攻擊 AOL 網際網路服務使用者的惡意程式碼，通常是藉由抓取密碼或修改設定。
<span id="MP_THREAT_CATEGORY_NUKER"></span><span id="mp_threat_category_nuker"></span>**MP \_威脅 \_ 類別 \_ NUKER** | 惡意程式碼是設計來損毀裝置或使其變得較不穩定。
<span id="MP_THREAT_CATEGORY_SECURITYDISABLER"></span><span id="mp_threat_category_securitydisabler"></span>**MP \_威脅 \_ 類別 \_ SECURITYDISABLER** | 停用安全性設定或產品的惡意程式碼。
<span id="MP_THREAT_CATEGORY_JOKEPROGRAM"></span><span id="mp_threat_category_jokeprogram"></span>**MP \_威脅 \_ 類別 \_ JOKEPROGRAM** | 設計用來 amuse 或怪嚇人使用者的應用程式，而不會實際損害裝置。
<span id="MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL"></span><span id="mp_threat_category_hostileactivexcontrol"></span>**MP \_威脅 \_ 類別 \_ HOSTILEACTIVEXCONTROL** | 由攻擊者所設計的 ActiveX 控制項危害裝置。 ActiveX 控制項是一種 Internet Explorer 專用的瀏覽器附加元件。
<span id="MP_THREAT_CATEGORY_SOFTWAREBUNDLER"></span><span id="mp_threat_category_softwarebundler"></span>**MP \_威脅 \_ 類別 \_ SOFTWAREBUNDLER** | 安裝其他潛在垃圾應用程式的軟體，例如廣告軟體或間諜軟體。 配套軟體的授權合約可能需要這些其他元件才能運作。
<span id="MP_THREAT_CATEGORY_STEALTHNOTIFIER"></span><span id="mp_threat_category_stealthnotifier"></span>**MP \_威脅 \_ 類別 \_ STEALTHNOTIFIER** | 惡意程式碼會透過隱形連線連接到遠端伺服器，以通知攻擊者已安裝惡意程式碼。
<span id="MP_THREAT_CATEGORY_SETTINGSMODIFIER"></span><span id="mp_threat_category_settingsmodifier"></span>**MP \_威脅 \_ 類別 \_ SETTINGSMODIFIER** | 不需要使用者的知識或同意即可變更使用者設定的潛在垃圾應用程式。
<span id="MP_THREAT_CATEGORY_TOOLBAR"></span><span id="mp_threat_category_toolbar"></span>**MP \_威脅 \_ 類別目錄 \_ 工具列** | 在使用者的網頁瀏覽器上安裝工具列的潛在垃圾應用程式 (PUA) ;通常與其他 PUA （例如廣告軟體）配套。
<span id="MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE"></span><span id="mp_threat_category_remotecontrolsoftware"></span>**MP \_威脅 \_ 類別 \_ REMOTECONTROLSOFTWARE** | 提供裝置遠端存取的潛在垃圾應用程式。
<span id="MP_THREAT_CATEGORY_TROJANFTP"></span><span id="mp_threat_category_trojanftp"></span>**MP \_威脅 \_ 類別 \_ TROJANFTP** | 使用 FTP 伺服器的特洛伊木馬程式，可讓攻擊者從裝置上傳或下載檔案。
<span id="MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE"></span><span id="mp_threat_category_potentialunwantedsoftware"></span>**MP \_威脅 \_ 類別 \_ POTENTIALUNWANTEDSOFTWARE** | 也稱為 *潛在的垃圾應用程式* 或 *PUA*;可能會以過度侵入的方式運作的軟體，使用者可能不會預期或完全同意。
<span id="MP_THREAT_CATEGORY_ICQEXPLOIT"></span><span id="mp_threat_category_icqexploit"></span>**MP \_威脅 \_ 類別 \_ ICQEXPLOIT** | 攻擊 ICQ 訊息服務的特洛伊木馬，通常是透過抓取密碼或篡改設定來進行攻擊。
<span id="MP_THREAT_CATEGORY_TROJANTELNET"></span><span id="mp_threat_category_trojantelnet"></span>**MP \_威脅 \_ 類別 \_ TROJANTELNET** | 特洛伊木馬程式，在使用者的電腦上安裝 telnet 伺服器，而不需要使用者的知識或同意。
<span id="MP_THREAT_CATEGORY_EXPLOIT"></span><span id="mp_threat_category_exploit"></span>**MP \_威脅 \_ 類別 \_ 攻擊** | 利用裝置或系統上弱點的惡意程式碼。
<span id="MP_THREAT_CATEGORY_FILESHARINGPROGRAM"></span><span id="mp_threat_category_filesharingprogram"></span>**MP \_威脅 \_ 類別 \_ FILESHARINGPROGRAM** | 潛在的垃圾應用程式，會開啟裝置來對裝置的檔案進行點對點共用。
<span id="MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL"></span><span id="mp_threat_category_malware_creation_tool"></span>**MP \_威脅 \_ 類別 \_ 惡意程式碼 \_ 建立 \_ 工具** | 可以自動產生惡意檔案的應用程式。
<span id="MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE"></span><span id="mp_threat_category_remote_control_software"></span>**MP \_威脅 \_ 類別 \_ 遠端 \_ 控制 \_ 軟體** | 允許遠端存取裝置的潛在垃圾應用程式。
<span id="MP_THREAT_CATEGORY_TOOL"></span><span id="mp_threat_category_tool"></span>**MP \_威脅 \_ 類別 \_ 工具** | 協助攻擊者在裝置上執行惡意動作的公用程式。
<span id="MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE"></span><span id="mp_threat_category_trojan_denialofservice"></span>**MP \_威脅 \_ 類別 \_ 特洛伊 \_ DENIALOFSERVICE** | 一種特洛伊木馬程式，其設計是為了將大量的網路要求傳送到目標，作為阻絕服務 (DoS) 攻擊的一部分。
<span id="MP_THREAT_CATEGORY_TROJAN_DROPPER"></span><span id="mp_threat_category_trojan_dropper"></span>**MP \_威脅 \_ 類別 \_ 特洛伊木馬 \_** 程式的植 | 一種特洛伊木馬程式，可在目標上下載及安裝惡意程式碼或潛在的垃圾應用程式。
<span id="MP_THREAT_CATEGORY_TROJAN_MASSMAILER"></span><span id="mp_threat_category_trojan_massmailer"></span>**MP \_威脅 \_ 類別 \_ 特洛伊 \_ MASSMAILER** | 將大量電子郵件傳送至目標的特洛伊木馬程式，目的是要讓目標的收件匣過多。
<span id="MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE"></span><span id="mp_threat_category_trojan_monitoringsoftware"></span>**MP \_威脅 \_ 類別 \_ 特洛伊 \_ MONITORINGSOFTWARE** | 一種特洛伊木馬程式，可監視使用者活動，例如使用者在鍵盤上輸入的內容，或螢幕上的視圖。
<span id="MP_THREAT_CATEGORY_TROJAN_PROXYSERVER"></span><span id="mp_threat_category_trojan_proxyserver"></span>**MP \_威脅 \_ 類別 \_ 特洛伊 \_ PROXYSERVER** | 特洛伊木馬程式所安裝的 proxy 伺服器，提供看似不中斷的網際網路連線，同時允許未經授權存取受感染的裝置。
<span id="MP_THREAT_CATEGORY_VIRUS"></span><span id="mp_threat_category_virus"></span>**MP \_威脅 \_ 類別 \_ 病毒** | 複寫的惡意程式碼（通常是藉由感染系統中的其他檔案），因此在啟用這些檔案時，允許執行惡意程式碼和傳播。
<span id="MP_THREAT_CATEGORY_KNOWN"></span><span id="mp_threat_category_known"></span>**MP \_\_ \_ 已知的威脅類別** | 未指定的惡意程式碼威脅。
<span id="MP_THREAT_CATEGORY_UNKNOWN"></span><span id="mp_threat_category_unknown"></span>**MP \_威脅 \_ 類別 \_ 不明** | 尚未定義的未指定惡意程式碼威脅。
<span id="MP_THREAT_CATEGORY_SPP"></span><span id="mp_threat_category_spp"></span>**MP \_威脅 \_ 類別 \_ SPP** | 一種反盜版技術，要求 Windows 產品的每個安裝都必須與 Microsoft 一起啟用。
<span id="MP_THREAT_CATEGORY_BEHAVIOR"></span><span id="mp_threat_category_behavior"></span>**MP \_威脅 \_ 類別 \_ 行為** | 根據經常與惡意活動相關聯的檔案動作進行的偵測類型。
<span id="MP_THREAT_CATEGORY_VULNERABILTIY"></span><span id="mp_threat_category_vulnerabiltiy"></span>**MP \_威脅 \_ 類別 \_ VULNERABILTIY** | 使裝置容易受到威脅惡意探索的任何弱點、系統管理程式或活動。
<span id="MP_THREAT_CATEGORY_POLICY"></span><span id="mp_threat_category_policy"></span>**MP \_威脅 \_ 類別目錄 \_ 原則** | 一組由系統管理員定義的規則，可控制桌上型電腦和行動裝置上的功能，例如軟體更新。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 最低支援的用戶端 | Windows 8 只 (桌面應用程式)  |
| 最低支援的伺服器 | Windows Server 2012 只 (桌面應用程式)  |
| 標頭 | MpClient。h |
