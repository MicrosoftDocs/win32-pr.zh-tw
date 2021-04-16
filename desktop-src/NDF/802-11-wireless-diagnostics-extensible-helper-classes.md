---
title: 802.11 無線診斷可延伸的 Helper 類別
description: 內建的無線診斷基礎結構有兩個擴充點。父協助程式 ClassPurposeRevised 原生 Wifi (RNWF) 可延伸的協助程式 ClassDiagnoses 與802.11 連線擴充功能相關的問題。
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde49561c68044157c9d518571b8241c49dcf25
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104507812"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a>802.11 無線診斷可延伸的 Helper 類別

內建的無線診斷基礎結構有兩個擴充點。

| 父 Helper 類別                                | 目的                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| 已修改原生 Wifi (RNWF) 可延伸的 Helper 類別 | 診斷與802.11 連接延伸模組相關的問題。       |
| L2Security 可擴充的 Helper 類別                 | 診斷第2層安全性通訊協定延伸模組的相關問題。 |



 

> [!Note]  
> 協力廠商協助程式類別應該註冊兩個父項 helper 類別，以確保呼叫協力廠商類別。 如需註冊的詳細資訊，請參閱 [註冊 NDF Helper 類別延伸](registering-ndf-helper-class-extensions.md)。

 

## <a name="rnwf-extensible-helper-class"></a>RNWF 可擴充的 Helper 類別

父 Helper 類別名稱

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

修訂的原生 Wifi (RNWF) 可延伸的協助程式類別，是協力廠商協助程式類別的父系，可診斷與擴充原生 Wifi 使用的802.11 通訊協定相關的問題。

RNWF helper 類別所提供的兩個索引鍵屬性是發生問題之介面的 GUID，以及連接內容。

-   介面 GUID：此屬性的名稱為 "Interface ID"，且類型 **為 \_ GUID**。

-   連接內容：這個屬性的名稱為 Network ID，且的類型為 \_ 八位 \_ 字串。 此字串實際上是 \_ \_ Wlanihv 中定義的 WDIAG IHV WLAN \_ 識別碼結構的緩衝區。 此結構的定義如下。

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_啟用的 IHV \_ WLAN \_ 識別碼 \_ 旗標 \_ 安全性 \_** 是唯一可能的 **dwFlags** 值。

 

協力廠商協助程式類別的相符屬性應該與其對應的軟體模組的服務識別碼相同。 這也是要在登錄中註冊協力廠商的相同名稱。 無線診斷將會在發生問題的無線會話期間查詢服務識別碼。 這項資訊會傳回給 NDF，以判斷協力廠商協助程式類別是否存在並註冊，然後再呼叫。

下表列出 RNWF 可擴充 helper 類別的相符屬性。



| 名稱          | 類型    | 值                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | REG \_ SZ | \[DiagnosticsID \_ GUID \_ 字串 |



 

## <a name="l2security-extensible-helper-class"></a>L2Security 可擴充的 Helper 類別

父 Helper 類別名稱

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

第2層安全性 (L2Security) 可延伸的 helper 類別是協力廠商協助程式類別的父系，可診斷與取代第2層安全性功能的對應服務和軟體模組相關的問題。

第2層安全性協助程式類別所提供的兩個索引鍵屬性是發生問題之介面的 GUID，以及連接內容。

-   介面 GUID：此屬性的名稱為 "Interface ID"，且類型 **為 \_ GUID**。

-   連接內容：這個屬性的名稱為 Network ID，且的類型為 \_ 八位 \_ 字串。 此字串實際上是 \_ \_ wlanihv 中定義的 WDIAG IHV WLAN \_ 識別碼結構的緩衝區。 此結構的定義如下。

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_啟用的 IHV \_ WLAN \_ 識別碼 \_ 旗標 \_ 安全性 \_** 是唯一可能的 **dwFlags** 值。

 

協力廠商協助程式類別的相符屬性應該與其對應的軟體模組的服務識別碼相同。 這也是要在登錄中註冊協力廠商的相同名稱。 無線診斷將會在發生問題的無線會話期間查詢服務識別碼。 這項資訊會傳回給 NDF，以判斷協力廠商協助程式類別是否存在並註冊，然後再呼叫。

下表列出第2層安全性可延伸 helper 類別的相符屬性。



| 名稱          | 類型    | 值                         |
|---------------|---------|-------------------------------|
| DiagnosticsID | REG \_ SZ | \[DiagnosticsID \_ GUID \_ 字串 |



 

## <a name="matching-attributes"></a>相符屬性

**DiagnosticsID**

802.11 無線診斷將會從核心原生 Wifi 服務查詢 *DiagnosticsID* ，以找出是否已安裝任何協力廠商無線延伸模組或安全性模組，以及是否包含在連接中。 接著，無線診斷會使用 *DiagnosticsID* 做為相符的屬性，為這些協力廠商協助程式類別提供假設。 任何協力廠商協助程式類別都應該包含在中，並隨相關聯的驅動程式套件一起安裝。 *DiagnosticsID* 將會定義在微型功能 INF 檔案中，做為 [AddReg](https://msdn.microsoft.com/library/ms794514.aspx)指示詞中的登錄機碼。

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

此機碼定義協力廠商軟體模組的無線協助程式類別的識別碼。 這是擴充性架構的選擇性索引鍵，但如果此執行包含的 IHV 無線協助程式類別會插入 NDF 並可診斷與 RNWF 無線或安全性延伸模組相關的連線問題，則需要此金鑰。 MS WLAN 診斷協助程式類別將會在安裝 IHV 模組時，從無線自動設定服務查詢此識別碼，並在診斷會話期間提供此識別碼做為 NDF 的參考或相符屬性，讓 NDF 可以在必要時呼叫適當的協力廠商無線協助程式類別。

**\[DiagnosticsID \_ GUID \_ 字串\]**

此值必須是所有大寫字母的字串。 例如，"{12345678-9ABC-DEF0-1234-56789ABCDEF0}"。

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a>802.11 無線診斷 Helper 類別的範圍

802.11 無線診斷協助程式類別目前會診斷下欄區域中的無線問題。

-   任何802.11 連線問題，包括802.11 關聯、802.11 驗證、與802.11 標準相關的802.11 安全性設定 & 在作業系統中原本就支援的通訊協定，以及效能問題。
-   802.1 x 設定和第2層驗證相關問題的第2層安全性問題，其使用 Windows Vista 和 Windows Server 2008 原生支援的方法。
-   用戶端與存取點之間的設定檔設定不符，或是網路基礎結構和服務。

802.11 無線診斷協助程式類別目前不會診斷下欄區域中的無線問題。

-   與協力廠商802.11 延伸模組相關的問題，包括與這些擴充功能相關的任何設定檔或驅動程式設定。
-   協力廠商 EAP 方法的相關問題。
-   無線微型埠驅動程式問題。
-   任何802.11 和第2層安全性通訊協定，或非原生支援的標準相關問題。
-   可能會影響無線連線能力的系統或元件層級問題，例如電源管理、磁碟空間不足、記憶體狀況和硬體問題。

此外，802.11 無線診斷無法分析 [**HighUtilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) 案例。 已識別的無線效能問題將會進行分析，並回報為 [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) 案例。

 

 




