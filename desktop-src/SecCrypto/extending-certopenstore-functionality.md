---
description: 憑證存放區是所有憑證管理作業的核心。
ms.assetid: e5c7c882-cbfc-4343-952c-b13c67326756
title: 擴充 CertOpenStore 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c770ae56ff597f51248486db2c9eb2d74bea8d63d2e8daad83d5938594b2f1a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007081"
---
# <a name="extending-certopenstore-functionality"></a>擴充 CertOpenStore 功能

[*憑證存放區*](../secgloss/c-gly.md)是所有憑證管理作業的核心。 [**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore)函式的功能可透過使用可安裝的 (或註冊的) 憑證存放區提供者功能來擴充。 如需如何安裝或註冊用於 CryptoAPI 的函式的總覽，請參閱 [OID 總覽](oid-overview.md)。

> [!Note]  
> 執行自動化部署時，不會自動遷移自訂憑證存放區。 若要遷移自訂憑證存放區，您必須建立用來遷移自訂存放區的資訊清單，並使用 Windows 消費者狀態移轉工具 (USMT) 。 您可以從 Microsoft 下載中心的下載 USMT <https://www.microsoft.com/download/details.aspx?id=10837> 。

 

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore)會在記憶體中開啟空的存放區，並使用 *lpszStoreProvider* 參數中所傳遞的 [*物件識別碼*](../secgloss/o-gly.md) (OID) ，呼叫存放區提供者函式 (是否已註冊或安裝) 。 如需 CryptoAPI 提供的預先定義提供者類型清單，請參閱 **CertOpenStore**。

存放區提供者函式會將其憑證和 [*憑證撤銷清單*](../secgloss/c-gly.md) 複製 (crl) 至傳遞給它的 *hCertStore* 控制碼所指定的記憶體中存放區。 新的存放區提供者函式可以使用任何 CryptoAPI 憑證存放區功能（例如 [**CertAddCertificateCoNtextToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore) 或 [**CertAddSerializedElementToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)），將其憑證和 crl 新增至記憶體中的存放區。 此外，存放區提供者函數會選擇性地傳回 [**CERT \_ store \_ >prov \_ 資訊**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) 結構中所有資料成員的值。 如果函數支援其他回呼函式，則此函式只需要更新此結構。 例如，如果存放區是唯讀存放區，則可能不需要其他回呼函數的支援。 如需可能回呼函數的詳細資料和原型，請參閱 [憑證存放區提供者回檔](cryptography-functions.md)函式。

每個使用者 TrustedPeople 存放區僅限於預先定義的實體存放區。 您無法擴充每個使用者 TrustedPeople 存放區。 不過，您可以擴充本機電腦 TrustedPeople 存放區。

**Windows XP 和 Windows Server 2003：** 每個使用者 TrustedPeople 存放區不限於預先定義的實體存放區。

[**CERT \_ STORE \_ >prov \_ 資訊**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info)結構的其中一個資料成員是 *rgpvStoreProvFunc* 陣列。 如果存放區提供者函式需要支援一或多個回呼函式，它必須提供此陣列的指標。 這些指標必須指向要用於其他憑證存放區活動的回呼函式 (例如關閉存放區) 。 下圖顯示此程式的流程。

![certopenstore 功能](images/openstor.png)

如下圖所示，在開啟存放區之後，其他 CryptoAPI 函式 (例如 [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)) 使用指標的陣列來存取執行預期工作的回呼函式。 證書 [**\_ 存儲的 \_ >prov \_ 資訊**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) 結構的定義，以及 CryptoAPI 提供之預設回呼函式的原型會顯示在 [憑證存放區提供者回檔](cryptography-functions.md)函式中。

![certclosestore 功能](images/closstor.png)

存放區 Api 可讓存放區提供者將憑證、Crl 和 [*憑證信任清單*](../secgloss/c-gly.md) 保存在存放 (區快取外的 (ctl) 例如，憑證的外部資料庫，例如 Microsoft 憑證伺服器資料庫) 所提供的憑證。

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) 會透過 *pszStoreProvider* 參數分派至適當的 [**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) 可安裝的提供者函式。 提供者會在 *pStoreProvInfo* 參數中傳回指向 [**CERT \_ STORE \_ >prov \_ 資訊**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) 結構的資訊。 **CERT \_ STORE \_ >prov \_ 資訊** 結構包含 **dwStoreProvFlags** 成員。 \_ \_ 已新增 CERT store >prov \_ 外部 \_ 旗標旗標，以允許提供者指出憑證、crl 和 ctl 在存放區的快取外部。

[**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) 會傳回回呼函數的陣列。 提供者可以執行下列回呼函數：

-   CERT \_ STORE \_ >PROV \_ CLOSE \_ FUNC
-   CERT \_ STORE \_ >PROV \_ READ \_ CERT \_ FUNC
-   CERT \_ STORE \_ >PROV \_ WRITE \_ CERT \_ FUNC
-   CERT \_ STORE \_ >PROV \_ DELETE \_ CERT \_ FUNC
-   CERT \_ STORE \_ >PROV \_ SET \_ CERT \_ PROPERTY \_ FUNC
-   證書 \_ 存儲 \_ >PROV \_ 讀取 \_ CRL \_ FUNC
-   證書 \_ 存儲 \_ >PROV \_ 寫入 \_ CRL \_ FUNC
-   證書 \_ 存儲 \_ >PROV \_ 刪除 \_ CRL \_ FUNC
-   CERT \_ STORE \_ >PROV \_ SET \_ CRL \_ PROPERTY \_ FUNC
-   證書 \_ 存儲 \_ >PROV \_ 讀取 \_ CTL \_ FUNC
-   證書 \_ 存儲 \_ >PROV \_ 寫入 \_ CTL \_ FUNC
-   CERT \_ STORE \_ >PROV \_ DELETE \_ CTL \_ FUNC
-   CERT \_ STORE \_ >PROV \_ SET \_ CTL \_ PROPERTY \_ FUNC

\_ \_ \_ 當設定 cert STORE >prov 寫入新增旗標時，對寫入憑證、寫入 CRL 和寫入 CTL 回呼函數的呼叫 \_ \_ \_ \_ \_ ， *dwFlags* 參數的前16位會包含 *dwAddDisposition* 值。 為了支援外部存放區，提供者可以執行下列回呼函數：

-   CERT \_ STORE \_ >PROV \_ FIND \_ CERT \_ FUNC
-   CERT \_ STORE \_ >PROV \_ FREE \_ FIND \_ CERT \_ FUNC
-   CERT \_ STORE \_ >PROV \_ 取得 \_ CERT \_ 屬性 \_ FUNC
-   CERT \_ STORE \_ >PROV \_ 尋找 \_ CRL \_ FUNC
-   CERT \_ STORE \_ >PROV \_ FREE \_ FIND \_ CRL \_ FUNC
-   CERT \_ STORE \_ >PROV \_ 取得 \_ CRL \_ 屬性 \_ FUNC
-   CERT \_ STORE \_ >PROV \_ 尋找 \_ CTL \_ FUNC
-   CERT \_ STORE \_ >PROV \_ FREE \_ FIND \_ CTL \_ FUNC
-   CERT \_ STORE \_ >PROV \_ 取得 \_ CTL \_ 屬性 \_ FUNC

憑證回呼函式具有下列簽章：

``` syntax
typedef struct _CERT_STORE_PROV_FIND_INFO {
    DWORD               cbSize;
    DWORD               dwMsgAndCertEncodingType;
    DWORD               dwFindFlags;
    DWORD               dwFindType;
    const void          *pvFindPara;
} CERT_STORE_PROV_FIND_INFO, *PCERT_STORE_PROV_FIND_INFO;
typedef const CERT_STORE_PROV_FIND_INFO CCERT_STORE_PROV_FIND_INFO,
    *PCCERT_STORE_PROV_FIND_INFO;

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_STORE_PROV_FIND_INFO pFindInfo,
        IN PCCERT_CONTEXT pPrevCertContext,
        IN DWORD dwFlags,
        IN OUT void **ppvStoreProvFindInfo,
        OUT PCCERT_CONTEXT *ppProvCertContext
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FREE_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN void *pvStoreProvFindInfo,
        IN DWORD dwFlags
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_GET_CERT_PROPERTY)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN DWORD dwPropId,
        IN DWORD dwFlags,
        OUT void *pvData,
        IN OUT DWORD *pcbData
        );
```

CRL 和 CTL 回呼函式的簽章與上述相同，其中的憑證 [**\_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) 指標取代為 [**CRL \_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) 或 [**CTL \_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context)的指標。

\_當商店 api 列舉、尋找或新增憑證時，就會呼叫 FIND CERT 回呼。 *pPrevCertCoNtext* 和 *ppvStoreProvFindInfo* 會設定為 **Null** ，以起始新的 FIND。 傳回的 *ppvStoreProvFindInfo* 會在下一個找出提供者釋出的時候傳回。 提供者可以設定所有、部分或無憑證屬性。 提供者可以選擇延後，直到呼叫取得 \_ 憑證 \_ 屬性回呼為止。 建議提供者盡可能將最多屬性設定為允許複製到另一個存放區。

[**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)支援下列憑證尋找類型：

-   CERT \_ 尋找 \_ 任何
-   CERT \_ 尋找 \_ SHA1 \_ 雜湊
-   CERT \_ FIND \_ MD5 \_ 雜湊
-   CERT \_ FIND \_ 屬性
-   CERT \_ FIND \_ 公開金鑰 \_
-   CERT \_ 尋找 \_ 主體 \_ 名稱
-   CERT \_ 尋找 \_ 主體 \_ ATTR
-   CERT \_ 尋找 \_ 簽發者 \_ 名稱
-   CERT \_ 尋找 \_ 簽發者的 \_ ATTR
-   CERT \_ 尋找 \_ 主體 \_ STR \_ A
-   CERT \_ 尋找 \_ 主體 \_ STR \_ W
-   CERT \_ 尋找 \_ 簽發者 \_ STR \_ A
-   CERT \_ 尋找 \_ 簽發者 \_ STR \_ W
-   CERT \_ FIND \_ KEY \_ 規格
-   CERT \_ FIND \_ ENHKEY \_ 使用方式

\_針對上述每個尋找類型呼叫尋找憑證回呼。 傳遞至 [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) 的參數會在 \_ \_ \_ \_ \_ 呼叫 find CERT 回呼之前，直接複製到 CERT STORE >prov FIND INFO 結構。 如需 CERT STORE >prov find INFO 結構的不同尋找類型之域值的詳細資訊 \_ \_ \_ \_ ，請參閱 **CertFindCertificateInStore**。

下列憑證尋找類型支援 [**CertGetSubjectCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) 和 [**CertGetIssuerCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore) api，並且有助於判斷憑證是否已存在於存放區中，然後再新增：

-   CERT \_ 尋找 \_ 主體 \_ 憑證
-   CERT \_ 尋找 \_ 簽發者 \_
-   CERT \_ 尋找 \_ 現有的

針對 CERT \_ FIND \_ subject \_ cert， *pvFindPara* 參數會指向憑證 [**\_ 資訊**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_info) 結構，其中包含主體的簽發者和 SerialNumber。 針對 CERT \_ FIND \_ 簽發者 \_ ， *pvFindPara* 會指向主體的憑證 [**\_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) 結構。 若是 CERT \_ FIND \_ EXISTING， *pvFindPara* 會指向憑證的憑證 **\_ 內容** ，以檢查其是否存在於存放區中。

當「 \_ \_ 尋找」憑證回呼所傳回的憑證 \_ 未藉由在後續的「尋找」憑證中使用 \_ ，因此其 [*參考計數*](../secgloss/r-gly.md) 減少為零，或藉由呼叫 [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)釋出時，就會呼叫 FREE FIND cert 回呼。 呼叫 CLOSE 回呼之前，會將尋找憑證回呼所傳回的所有憑證都 \_ 傳給提供者，方法是傳遞給尋找憑證回呼的呼叫， \_ 或呼叫 FREE \_ FIND \_ cert 回呼。 這同樣適用于 CRL 和 CTL 回呼。

如果找 \_ \_ 不到 *pCertCoNtext* 參數的指定屬性， [**CertGetCertificateCoNtextProperty**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)會呼叫取得憑證屬性回呼。 GET \_ CRL \_ PROPERTY 和 get \_ CTL 屬性也是如此 \_ 。

\_當商店 api 列舉或取得 crl，以及新增 crl 之前，會呼叫尋找 crl 回呼。 將會定義下列 CRL 尋找類型：

針對 CRL 的「 \_ 尋找 \_ 物件」 \_ ， *pvFindPara* 是 crl 簽發者的憑證 [**\_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) 指標。 針對 CRL \_ FIND \_ EXISTING， *pvFindPara* 是 crl 的 [**crl \_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) 指標，可判斷該 crl 是否已存在於存放區中。

\_當商店 api 列舉或尋找 ctl 時，會呼叫尋找 ctl 回呼。 [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore)支援下列 CTL 尋找類型：

-   CTL \_ 尋找 \_ 任何
-   CTL \_ 尋找 \_ SHA1 \_ 雜湊
-   CTL \_ 尋找 \_ MD5 \_ 雜湊
-   CTL \_ 尋找 \_ 使用方式
-   CTL \_ 尋找 \_ 主體
-   CTL \_ 尋找 \_ 現有的

\_針對上述每個尋找類型呼叫「尋找 CTL 回呼」。 傳遞至 [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore) 的參數會在 \_ \_ \_ \_ \_ 呼叫 find CTL 回呼之前，直接複製到 CERT STORE >prov FIND INFO 結構。 如需 CERT STORE >prov find INFO 結構的不同尋找類型之域值的詳細資訊 \_ \_ \_ \_ ，請參閱 **CertFindCTLInStore**。

CTL \_ 尋找 \_ 現有的 ctl 尋找類型有助於判斷 ctl 是否已存在於存放區中，然後再進行 ctl 新增。

針對 CTL \_ FIND \_ EXISTING， *pvFindPara* 是 ctl [**\_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context) 結構的指標，可判斷它是否已存在於存放區中。

 

 
