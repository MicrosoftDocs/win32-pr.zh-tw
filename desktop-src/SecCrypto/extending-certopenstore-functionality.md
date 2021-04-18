---
description: 憑證存放區是所有憑證管理作業的核心。
ms.assetid: e5c7c882-cbfc-4343-952c-b13c67326756
title: 擴充 CertOpenStore 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce198578cc482ba0488bd97ae0f1d7f923511b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551643"
---
# <a name="extending-certopenstore-functionality"></a><span data-ttu-id="2c973-103">擴充 CertOpenStore 功能</span><span class="sxs-lookup"><span data-stu-id="2c973-103">Extending CertOpenStore Functionality</span></span>

<span data-ttu-id="2c973-104">[*憑證存放區*](../secgloss/c-gly.md)是所有憑證管理作業的核心。</span><span class="sxs-lookup"><span data-stu-id="2c973-104">The [*certificate store*](../secgloss/c-gly.md) is central to all certificate management operations.</span></span> <span data-ttu-id="2c973-105">[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore)函式的功能可透過使用可安裝的 (或註冊的) 憑證存放區提供者功能來擴充。</span><span class="sxs-lookup"><span data-stu-id="2c973-105">The functionality of the [**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) function can be extended through the use of an installable (or registered) certificate-store-provider function.</span></span> <span data-ttu-id="2c973-106">如需如何安裝或註冊用於 CryptoAPI 的函式的總覽，請參閱 [OID 總覽](oid-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="2c973-106">For an overview of how to install or register functions for use with the CryptoAPI, see [OID Overview](oid-overview.md).</span></span>

> [!Note]  
> <span data-ttu-id="2c973-107">執行自動化部署時，不會自動遷移自訂憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="2c973-107">Custom certificate stores are not automatically migrated when performing automated deployments.</span></span> <span data-ttu-id="2c973-108">若要遷移自訂憑證存放區，您必須建立用來遷移自訂存放區的資訊清單，並使用 Windows 消費者狀態移轉工具 (USMT) 。</span><span class="sxs-lookup"><span data-stu-id="2c973-108">To migrate custom certificate stores, you must create a manifest for migrating the custom stores and use the Windows User State Migration Tool (USMT).</span></span> <span data-ttu-id="2c973-109">您可以從 Microsoft 下載中心的下載 USMT <https://www.microsoft.com/download/details.aspx?id=10837> 。</span><span class="sxs-lookup"><span data-stu-id="2c973-109">The USMT is available for download from the Microsoft Download Center at <https://www.microsoft.com/download/details.aspx?id=10837>.</span></span>

 

<span data-ttu-id="2c973-110">[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore)會在記憶體中開啟空的存放區，並使用 *lpszStoreProvider* 參數中所傳遞的 [*物件識別碼*](../secgloss/o-gly.md) (OID) ，呼叫存放區提供者函式 (是否已註冊或安裝) 。</span><span class="sxs-lookup"><span data-stu-id="2c973-110">[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) opens an empty store in memory and calls the store provider function (if it is registered or installed) by using the [*object identifier*](../secgloss/o-gly.md) (OID) that was passed in the *lpszStoreProvider* parameter.</span></span> <span data-ttu-id="2c973-111">如需 CryptoAPI 提供的預先定義提供者類型清單，請參閱 **CertOpenStore**。</span><span class="sxs-lookup"><span data-stu-id="2c973-111">For a list of the predefined provider types that are supplied with the CryptoAPI, see **CertOpenStore**.</span></span>

<span data-ttu-id="2c973-112">存放區提供者函式會將其憑證和 [*憑證撤銷清單*](../secgloss/c-gly.md) 複製 (crl) 至傳遞給它的 *hCertStore* 控制碼所指定的記憶體中存放區。</span><span class="sxs-lookup"><span data-stu-id="2c973-112">The store provider function copies its certificates and [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs) to the in-memory store specified by the *hCertStore* handle passed to it.</span></span> <span data-ttu-id="2c973-113">新的存放區提供者函式可以使用任何 CryptoAPI 憑證存放區功能（例如 [**CertAddCertificateCoNtextToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore) 或 [**CertAddSerializedElementToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)），將其憑證和 crl 新增至記憶體中的存放區。</span><span class="sxs-lookup"><span data-stu-id="2c973-113">The new store provider function can use any of the CryptoAPI certificate store functions, such as, [**CertAddCertificateContextToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore) or [**CertAddSerializedElementToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore), to add its certificates and CRLs to the in-memory store.</span></span> <span data-ttu-id="2c973-114">此外，存放區提供者函數會選擇性地傳回 [**CERT \_ store \_ >prov \_ 資訊**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) 結構中所有資料成員的值。</span><span class="sxs-lookup"><span data-stu-id="2c973-114">In addition, the store-provider function optionally returns values for all of the data members of the [**CERT\_STORE\_PROV\_INFO**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) structure.</span></span> <span data-ttu-id="2c973-115">如果函數支援其他回呼函式，則此函式只需要更新此結構。</span><span class="sxs-lookup"><span data-stu-id="2c973-115">The function only needs to update this structure if it supports additional callback functions.</span></span> <span data-ttu-id="2c973-116">例如，如果存放區是唯讀存放區，則可能不需要其他回呼函數的支援。</span><span class="sxs-lookup"><span data-stu-id="2c973-116">For example, if the store was to be a read-only store, the support of other callback functions probably would not be needed.</span></span> <span data-ttu-id="2c973-117">如需可能回呼函數的詳細資料和原型，請參閱 [憑證存放區提供者回檔](cryptography-functions.md)函式。</span><span class="sxs-lookup"><span data-stu-id="2c973-117">For details and prototypes of the possible callback functions, see [Certificate Store Provider Callback Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="2c973-118">每個使用者 TrustedPeople 存放區僅限於預先定義的實體存放區。</span><span class="sxs-lookup"><span data-stu-id="2c973-118">The per user TrustedPeople store is restricted to predefined physical stores.</span></span> <span data-ttu-id="2c973-119">您無法擴充每個使用者 TrustedPeople 存放區。</span><span class="sxs-lookup"><span data-stu-id="2c973-119">You cannot extend the per user TrustedPeople store.</span></span> <span data-ttu-id="2c973-120">不過，您可以擴充本機電腦 TrustedPeople 存放區。</span><span class="sxs-lookup"><span data-stu-id="2c973-120">However, you can extend the local machine TrustedPeople store.</span></span>

<span data-ttu-id="2c973-121">**WINDOWS XP 和 Windows Server 2003：** 每個使用者 TrustedPeople 存放區不限於預先定義的實體存放區。</span><span class="sxs-lookup"><span data-stu-id="2c973-121">**Windows XP and Windows Server 2003:** The per user TrustedPeople store is not restricted to predefined physical stores.</span></span>

<span data-ttu-id="2c973-122">[**CERT \_ STORE \_ >prov \_ 資訊**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info)結構的其中一個資料成員是 *rgpvStoreProvFunc* 陣列。</span><span class="sxs-lookup"><span data-stu-id="2c973-122">One of the data members of the [**CERT\_STORE\_PROV\_INFO**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) structure is the *rgpvStoreProvFunc* array.</span></span> <span data-ttu-id="2c973-123">如果存放區提供者函式需要支援一或多個回呼函式，它必須提供此陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="2c973-123">If the store provider function needs to support one or more of the callback functions, it must provide pointers for this array.</span></span> <span data-ttu-id="2c973-124">這些指標必須指向要用於其他憑證存放區活動的回呼函式 (例如關閉存放區) 。</span><span class="sxs-lookup"><span data-stu-id="2c973-124">These pointers must point to the callback functions that are to be used for other certificate-store activities (such as closing the store).</span></span> <span data-ttu-id="2c973-125">下圖顯示此程式的流程。</span><span class="sxs-lookup"><span data-stu-id="2c973-125">The following illustration shows the flow of this process.</span></span>

![certopenstore 功能](images/openstor.png)

<span data-ttu-id="2c973-127">如下圖所示，在開啟存放區之後，其他 CryptoAPI 函式 (例如 [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)) 使用指標的陣列來存取執行預期工作的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="2c973-127">As shown in the following illustration, after the store has been opened, other CryptoAPI functions (such as [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)) use the array of pointers to access the callback functions that perform the intended task.</span></span> <span data-ttu-id="2c973-128">證書 [**\_ 存儲的 \_ >prov \_ 資訊**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) 結構的定義，以及 CryptoAPI 提供之預設回呼函式的原型會顯示在 [憑證存放區提供者回檔](cryptography-functions.md)函式中。</span><span class="sxs-lookup"><span data-stu-id="2c973-128">The definition of the [**CERT\_STORE\_PROV\_INFO**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) structure and the prototypes of the default callback functions that are supplied with the CryptoAPI are shown in [Certificate Store Provider Callback Functions](cryptography-functions.md).</span></span>

![certclosestore 功能](images/closstor.png)

<span data-ttu-id="2c973-130">存放區 Api 可讓存放區提供者將憑證、Crl 和 [*憑證信任清單*](../secgloss/c-gly.md) 保存在存放 (區快取外的 (ctl) 例如，憑證的外部資料庫，例如 Microsoft 憑證伺服器資料庫) 所提供的憑證。</span><span class="sxs-lookup"><span data-stu-id="2c973-130">The store APIs allow a store provider to maintain the certificates, CRLs, and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) outside the cache of the store (for example, an external database of certificates, such as provided by the Microsoft Certificate Server Database).</span></span>

<span data-ttu-id="2c973-131">[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) 會透過 *pszStoreProvider* 參數分派至適當的 [**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) 可安裝的提供者函式。</span><span class="sxs-lookup"><span data-stu-id="2c973-131">[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) dispatches through the *pszStoreProvider* parameter to the appropriate [**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) installable provider function.</span></span> <span data-ttu-id="2c973-132">提供者會在 *pStoreProvInfo* 參數中傳回指向 [**CERT \_ STORE \_ >prov \_ 資訊**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) 結構的資訊。</span><span class="sxs-lookup"><span data-stu-id="2c973-132">The provider returns information in the *pStoreProvInfo* parameter that points to a [**CERT\_STORE\_PROV\_INFO**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) structure.</span></span> <span data-ttu-id="2c973-133">**CERT \_ STORE \_ >prov \_ 資訊** 結構包含 **dwStoreProvFlags** 成員。</span><span class="sxs-lookup"><span data-stu-id="2c973-133">The **CERT\_STORE\_PROV\_INFO** structure contains a **dwStoreProvFlags** member.</span></span> <span data-ttu-id="2c973-134">\_ \_ 已新增 CERT store >prov \_ 外部 \_ 旗標旗標，以允許提供者指出憑證、crl 和 ctl 在存放區的快取外部。</span><span class="sxs-lookup"><span data-stu-id="2c973-134">The CERT\_STORE\_PROV\_EXTERNAL\_FLAG flag was added to allow the provider to indicate that the certificates, CRLs, and CTLs are external to the cache of the store.</span></span>

<span data-ttu-id="2c973-135">[**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) 會傳回回呼函數的陣列。</span><span class="sxs-lookup"><span data-stu-id="2c973-135">[**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) returns an array of callback functions.</span></span> <span data-ttu-id="2c973-136">提供者可以執行下列回呼函數：</span><span class="sxs-lookup"><span data-stu-id="2c973-136">A provider can implement the following callback functions:</span></span>

-   <span data-ttu-id="2c973-137">CERT \_ STORE \_ >PROV \_ CLOSE \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-137">CERT\_STORE\_PROV\_CLOSE\_FUNC</span></span>
-   <span data-ttu-id="2c973-138">CERT \_ STORE \_ >PROV \_ READ \_ CERT \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-138">CERT\_STORE\_PROV\_READ\_CERT\_FUNC</span></span>
-   <span data-ttu-id="2c973-139">CERT \_ STORE \_ >PROV \_ WRITE \_ CERT \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-139">CERT\_STORE\_PROV\_WRITE\_CERT\_FUNC</span></span>
-   <span data-ttu-id="2c973-140">CERT \_ STORE \_ >PROV \_ DELETE \_ CERT \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-140">CERT\_STORE\_PROV\_DELETE\_CERT\_FUNC</span></span>
-   <span data-ttu-id="2c973-141">CERT \_ STORE \_ >PROV \_ SET \_ CERT \_ PROPERTY \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-141">CERT\_STORE\_PROV\_SET\_CERT\_PROPERTY\_FUNC</span></span>
-   <span data-ttu-id="2c973-142">證書 \_ 存儲 \_ >PROV \_ 讀取 \_ CRL \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-142">CERT\_STORE\_PROV\_READ\_CRL\_FUNC</span></span>
-   <span data-ttu-id="2c973-143">證書 \_ 存儲 \_ >PROV \_ 寫入 \_ CRL \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-143">CERT\_STORE\_PROV\_WRITE\_CRL\_FUNC</span></span>
-   <span data-ttu-id="2c973-144">證書 \_ 存儲 \_ >PROV \_ 刪除 \_ CRL \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-144">CERT\_STORE\_PROV\_DELETE\_CRL\_FUNC</span></span>
-   <span data-ttu-id="2c973-145">CERT \_ STORE \_ >PROV \_ SET \_ CRL \_ PROPERTY \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-145">CERT\_STORE\_PROV\_SET\_CRL\_PROPERTY\_FUNC</span></span>
-   <span data-ttu-id="2c973-146">證書 \_ 存儲 \_ >PROV \_ 讀取 \_ CTL \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-146">CERT\_STORE\_PROV\_READ\_CTL\_FUNC</span></span>
-   <span data-ttu-id="2c973-147">證書 \_ 存儲 \_ >PROV \_ 寫入 \_ CTL \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-147">CERT\_STORE\_PROV\_WRITE\_CTL\_FUNC</span></span>
-   <span data-ttu-id="2c973-148">CERT \_ STORE \_ >PROV \_ DELETE \_ CTL \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-148">CERT\_STORE\_PROV\_DELETE\_CTL\_FUNC</span></span>
-   <span data-ttu-id="2c973-149">CERT \_ STORE \_ >PROV \_ SET \_ CTL \_ PROPERTY \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-149">CERT\_STORE\_PROV\_SET\_CTL\_PROPERTY\_FUNC</span></span>

<span data-ttu-id="2c973-150">\_ \_ \_ 當設定 cert STORE >prov 寫入新增旗標時，對寫入憑證、寫入 CRL 和寫入 CTL 回呼函數的呼叫 \_ \_ \_ \_ \_ ， *dwFlags* 參數的前16位會包含 *dwAddDisposition* 值。</span><span class="sxs-lookup"><span data-stu-id="2c973-150">On calls to the WRITE\_CERT, WRITE\_CRL, and WRITE\_CTL callback functions when the CERT\_STORE\_PROV\_WRITE\_ADD\_FLAG is set, the upper 16 bits of the *dwFlags* parameter contains the *dwAddDisposition* value.</span></span> <span data-ttu-id="2c973-151">為了支援外部存放區，提供者可以執行下列回呼函數：</span><span class="sxs-lookup"><span data-stu-id="2c973-151">To support external stores, a provider can implement the following callback functions:</span></span>

-   <span data-ttu-id="2c973-152">CERT \_ STORE \_ >PROV \_ FIND \_ CERT \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-152">CERT\_STORE\_PROV\_FIND\_CERT\_FUNC</span></span>
-   <span data-ttu-id="2c973-153">CERT \_ STORE \_ >PROV \_ FREE \_ FIND \_ CERT \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-153">CERT\_STORE\_PROV\_FREE\_FIND\_CERT\_FUNC</span></span>
-   <span data-ttu-id="2c973-154">CERT \_ STORE \_ >PROV \_ 取得 \_ CERT \_ 屬性 \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-154">CERT\_STORE\_PROV\_GET\_CERT\_PROPERTY\_FUNC</span></span>
-   <span data-ttu-id="2c973-155">CERT \_ STORE \_ >PROV \_ 尋找 \_ CRL \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-155">CERT\_STORE\_PROV\_FIND\_CRL\_FUNC</span></span>
-   <span data-ttu-id="2c973-156">CERT \_ STORE \_ >PROV \_ FREE \_ FIND \_ CRL \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-156">CERT\_STORE\_PROV\_FREE\_FIND\_CRL\_FUNC</span></span>
-   <span data-ttu-id="2c973-157">CERT \_ STORE \_ >PROV \_ 取得 \_ CRL \_ 屬性 \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-157">CERT\_STORE\_PROV\_GET\_CRL\_PROPERTY\_FUNC</span></span>
-   <span data-ttu-id="2c973-158">CERT \_ STORE \_ >PROV \_ 尋找 \_ CTL \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-158">CERT\_STORE\_PROV\_FIND\_CTL\_FUNC</span></span>
-   <span data-ttu-id="2c973-159">CERT \_ STORE \_ >PROV \_ FREE \_ FIND \_ CTL \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-159">CERT\_STORE\_PROV\_FREE\_FIND\_CTL\_FUNC</span></span>
-   <span data-ttu-id="2c973-160">CERT \_ STORE \_ >PROV \_ 取得 \_ CTL \_ 屬性 \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="2c973-160">CERT\_STORE\_PROV\_GET\_CTL\_PROPERTY\_FUNC</span></span>

<span data-ttu-id="2c973-161">憑證回呼函式具有下列簽章：</span><span class="sxs-lookup"><span data-stu-id="2c973-161">The certificate callback functions have the following signatures:</span></span>

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

<span data-ttu-id="2c973-162">CRL 和 CTL 回呼函式的簽章與上述相同，其中的憑證 [**\_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) 指標取代為 [**CRL \_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) 或 [**CTL \_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context)的指標。</span><span class="sxs-lookup"><span data-stu-id="2c973-162">The signatures for the CRL and CTL callback functions are identical to the above with the pointer to the [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) replaced with a pointer to a [**CRL\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) or [**CTL\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context).</span></span>

<span data-ttu-id="2c973-163">\_當商店 api 列舉、尋找或新增憑證時，就會呼叫 FIND CERT 回呼。</span><span class="sxs-lookup"><span data-stu-id="2c973-163">The FIND\_CERT callback is called when the store APIs enumerate, find, or add certificates.</span></span> <span data-ttu-id="2c973-164">*pPrevCertCoNtext* 和 *ppvStoreProvFindInfo* 會設定為 **Null** ，以起始新的 FIND。</span><span class="sxs-lookup"><span data-stu-id="2c973-164">*pPrevCertContext* and *ppvStoreProvFindInfo* are set to **NULL** to initiate a new FIND.</span></span> <span data-ttu-id="2c973-165">傳回的 *ppvStoreProvFindInfo* 會在下一個找出提供者釋出的時候傳回。</span><span class="sxs-lookup"><span data-stu-id="2c973-165">The returned *ppvStoreProvFindInfo* is passed back on the next find at which time it may be freed by the provider.</span></span> <span data-ttu-id="2c973-166">提供者可以設定所有、部分或無憑證屬性。</span><span class="sxs-lookup"><span data-stu-id="2c973-166">The provider may set all, some, or none of the certificate properties.</span></span> <span data-ttu-id="2c973-167">提供者可以選擇延後，直到呼叫取得 \_ 憑證 \_ 屬性回呼為止。</span><span class="sxs-lookup"><span data-stu-id="2c973-167">The provider has the option to defer until the GET\_CERT\_PROPERTY callback is called.</span></span> <span data-ttu-id="2c973-168">建議提供者盡可能將最多屬性設定為允許複製到另一個存放區。</span><span class="sxs-lookup"><span data-stu-id="2c973-168">It is recommended for providers to set as many properties as possible to allow copying to another store.</span></span>

<span data-ttu-id="2c973-169">[**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)支援下列憑證尋找類型：</span><span class="sxs-lookup"><span data-stu-id="2c973-169">The following certificate find types are supported in [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore):</span></span>

-   <span data-ttu-id="2c973-170">CERT \_ 尋找 \_ 任何</span><span class="sxs-lookup"><span data-stu-id="2c973-170">CERT\_FIND\_ANY</span></span>
-   <span data-ttu-id="2c973-171">CERT \_ 尋找 \_ SHA1 \_ 雜湊</span><span class="sxs-lookup"><span data-stu-id="2c973-171">CERT\_FIND\_SHA1\_HASH</span></span>
-   <span data-ttu-id="2c973-172">CERT \_ FIND \_ MD5 \_ 雜湊</span><span class="sxs-lookup"><span data-stu-id="2c973-172">CERT\_FIND\_MD5\_HASH</span></span>
-   <span data-ttu-id="2c973-173">CERT \_ FIND \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="2c973-173">CERT\_FIND\_PROPERTY</span></span>
-   <span data-ttu-id="2c973-174">CERT \_ FIND \_ 公開金鑰 \_</span><span class="sxs-lookup"><span data-stu-id="2c973-174">CERT\_FIND\_PUBLIC\_KEY</span></span>
-   <span data-ttu-id="2c973-175">CERT \_ 尋找 \_ 主體 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="2c973-175">CERT\_FIND\_SUBJECT\_NAME</span></span>
-   <span data-ttu-id="2c973-176">CERT \_ 尋找 \_ 主體 \_ ATTR</span><span class="sxs-lookup"><span data-stu-id="2c973-176">CERT\_FIND\_SUBJECT\_ATTR</span></span>
-   <span data-ttu-id="2c973-177">CERT \_ 尋找 \_ 簽發者 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="2c973-177">CERT\_FIND\_ISSUER\_NAME</span></span>
-   <span data-ttu-id="2c973-178">CERT \_ 尋找 \_ 簽發者的 \_ ATTR</span><span class="sxs-lookup"><span data-stu-id="2c973-178">CERT\_FIND\_ISSUER\_ATTR</span></span>
-   <span data-ttu-id="2c973-179">CERT \_ 尋找 \_ 主體 \_ STR \_ A</span><span class="sxs-lookup"><span data-stu-id="2c973-179">CERT\_FIND\_SUBJECT\_STR\_A</span></span>
-   <span data-ttu-id="2c973-180">CERT \_ 尋找 \_ 主體 \_ STR \_ W</span><span class="sxs-lookup"><span data-stu-id="2c973-180">CERT\_FIND\_SUBJECT\_STR\_W</span></span>
-   <span data-ttu-id="2c973-181">CERT \_ 尋找 \_ 簽發者 \_ STR \_ A</span><span class="sxs-lookup"><span data-stu-id="2c973-181">CERT\_FIND\_ISSUER\_STR\_A</span></span>
-   <span data-ttu-id="2c973-182">CERT \_ 尋找 \_ 簽發者 \_ STR \_ W</span><span class="sxs-lookup"><span data-stu-id="2c973-182">CERT\_FIND\_ISSUER\_STR\_W</span></span>
-   <span data-ttu-id="2c973-183">CERT \_ FIND \_ KEY \_ 規格</span><span class="sxs-lookup"><span data-stu-id="2c973-183">CERT\_FIND\_KEY\_SPEC</span></span>
-   <span data-ttu-id="2c973-184">CERT \_ FIND \_ ENHKEY \_ 使用方式</span><span class="sxs-lookup"><span data-stu-id="2c973-184">CERT\_FIND\_ENHKEY\_USAGE</span></span>

<span data-ttu-id="2c973-185">\_針對上述每個尋找類型呼叫尋找憑證回呼。</span><span class="sxs-lookup"><span data-stu-id="2c973-185">The FIND\_CERT callback is called for each of the above find types.</span></span> <span data-ttu-id="2c973-186">傳遞至 [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) 的參數會在 \_ \_ \_ \_ \_ 呼叫 find CERT 回呼之前，直接複製到 CERT STORE >prov FIND INFO 結構。</span><span class="sxs-lookup"><span data-stu-id="2c973-186">The parameters passed to [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) are copied directly to the CERT\_STORE\_PROV\_FIND\_INFO structure before the FIND\_CERT callback is called.</span></span> <span data-ttu-id="2c973-187">如需 CERT STORE >prov find INFO 結構的不同尋找類型之域值的詳細資訊 \_ \_ \_ \_ ，請參閱 **CertFindCertificateInStore**。</span><span class="sxs-lookup"><span data-stu-id="2c973-187">For details about the field values for the different find types of the CERT\_STORE\_PROV\_FIND\_INFO structure, see **CertFindCertificateInStore**.</span></span>

<span data-ttu-id="2c973-188">下列憑證尋找類型支援 [**CertGetSubjectCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) 和 [**CertGetIssuerCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore) api，並且有助於判斷憑證是否已存在於存放區中，然後再新增：</span><span class="sxs-lookup"><span data-stu-id="2c973-188">The following certificate find types support the [**CertGetSubjectCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) and [**CertGetIssuerCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore) APIs and help determine whether the certificate already exists in the store before adding:</span></span>

-   <span data-ttu-id="2c973-189">CERT \_ 尋找 \_ 主體 \_ 憑證</span><span class="sxs-lookup"><span data-stu-id="2c973-189">CERT\_FIND\_SUBJECT\_CERT</span></span>
-   <span data-ttu-id="2c973-190">CERT \_ 尋找 \_ 簽發者 \_</span><span class="sxs-lookup"><span data-stu-id="2c973-190">CERT\_FIND\_ISSUER\_OF</span></span>
-   <span data-ttu-id="2c973-191">CERT \_ 尋找 \_ 現有的</span><span class="sxs-lookup"><span data-stu-id="2c973-191">CERT\_FIND\_EXISTING</span></span>

<span data-ttu-id="2c973-192">針對 CERT \_ FIND \_ subject \_ cert， *pvFindPara* 參數會指向憑證 [**\_ 資訊**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_info) 結構，其中包含主體的簽發者和 SerialNumber。</span><span class="sxs-lookup"><span data-stu-id="2c973-192">For CERT\_FIND\_SUBJECT\_CERT, the *pvFindPara* parameter points to a [**CERT\_INFO**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_info) structure that contains the Issuer and SerialNumber of the subject.</span></span> <span data-ttu-id="2c973-193">針對 CERT \_ FIND \_ 簽發者 \_ ， *pvFindPara* 會指向主體的憑證 [**\_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) 結構。</span><span class="sxs-lookup"><span data-stu-id="2c973-193">For CERT\_FIND\_ISSUER\_OF, *pvFindPara* points to a [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) structure, of the subject.</span></span> <span data-ttu-id="2c973-194">若是 CERT \_ FIND \_ EXISTING， *pvFindPara* 會指向憑證的憑證 **\_ 內容** ，以檢查其是否存在於存放區中。</span><span class="sxs-lookup"><span data-stu-id="2c973-194">For CERT\_FIND\_EXISTING, *pvFindPara* points to a **CERT\_CONTEXT** of the certificate to check for its existence in the store.</span></span>

<span data-ttu-id="2c973-195">當「 \_ \_ 尋找」憑證回呼所傳回的憑證 \_ 未藉由在後續的「尋找」憑證中使用 \_ ，因此其 [*參考計數*](../secgloss/r-gly.md) 減少為零，或藉由呼叫 [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)釋出時，就會呼叫 FREE FIND cert 回呼。</span><span class="sxs-lookup"><span data-stu-id="2c973-195">The FREE\_FIND\_CERT callback is called when the certificate returned by the FIND\_CERT callback was not released by being used in a subsequent next FIND\_CERT, thus having its [*reference count*](../secgloss/r-gly.md) decremented to zero, or by being released by a call to [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore).</span></span> <span data-ttu-id="2c973-196">呼叫 CLOSE 回呼之前，會將尋找憑證回呼所傳回的所有憑證都 \_ 傳給提供者，方法是傳遞給尋找憑證回呼的呼叫， \_ 或呼叫 FREE \_ FIND \_ cert 回呼。</span><span class="sxs-lookup"><span data-stu-id="2c973-196">Before the CLOSE callback is called, all certificates returned by the FIND\_CERT callback should be released to the provider by being passed to a call to the FIND\_CERT callback or a call to the FREE\_FIND\_CERT callback.</span></span> <span data-ttu-id="2c973-197">這同樣適用于 CRL 和 CTL 回呼。</span><span class="sxs-lookup"><span data-stu-id="2c973-197">The same applies to the CRL and CTL callbacks.</span></span>

<span data-ttu-id="2c973-198">如果找 \_ \_ 不到 *pCertCoNtext* 參數的指定屬性， [**CertGetCertificateCoNtextProperty**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)會呼叫取得憑證屬性回呼。</span><span class="sxs-lookup"><span data-stu-id="2c973-198">The GET\_CERT\_PROPERTY callback is called by [**CertGetCertificateContextProperty**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) if it cannot find the specified property for the *pCertContext* parameter.</span></span> <span data-ttu-id="2c973-199">GET \_ CRL \_ PROPERTY 和 get \_ CTL 屬性也是如此 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2c973-199">The same is true for GET\_CRL\_PROPERTY and GET\_CTL\_PROPERTY.</span></span>

<span data-ttu-id="2c973-200">\_當商店 api 列舉或取得 crl，以及新增 crl 之前，會呼叫尋找 crl 回呼。</span><span class="sxs-lookup"><span data-stu-id="2c973-200">The FIND\_CRL callback is called when the store APIs enumerate or get CRLs and before adding a CRL.</span></span> <span data-ttu-id="2c973-201">將會定義下列 CRL 尋找類型：</span><span class="sxs-lookup"><span data-stu-id="2c973-201">The following CRL find types will be defined:</span></span>

<span data-ttu-id="2c973-202">針對 CRL 的「 \_ 尋找 \_ 物件」 \_ ， *pvFindPara* 是 crl 簽發者的憑證 [**\_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) 指標。</span><span class="sxs-lookup"><span data-stu-id="2c973-202">For CRL\_FIND\_ISSUED\_BY, *pvFindPara* is a pointer to a [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) of the CRL issuer.</span></span> <span data-ttu-id="2c973-203">針對 CRL \_ FIND \_ EXISTING， *pvFindPara* 是 crl 的 [**crl \_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) 指標，可判斷該 crl 是否已存在於存放區中。</span><span class="sxs-lookup"><span data-stu-id="2c973-203">For CRL\_FIND\_EXISTING, *pvFindPara* is a pointer to a [**CRL\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) of the CRL to determine whether it already exists in the store.</span></span>

<span data-ttu-id="2c973-204">\_當商店 api 列舉或尋找 ctl 時，會呼叫尋找 ctl 回呼。</span><span class="sxs-lookup"><span data-stu-id="2c973-204">The FIND\_CTL callback is called when the store APIs enumerate or find CTLs.</span></span> <span data-ttu-id="2c973-205">[**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore)支援下列 CTL 尋找類型：</span><span class="sxs-lookup"><span data-stu-id="2c973-205">The following CTL find types are supported in [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore):</span></span>

-   <span data-ttu-id="2c973-206">CTL \_ 尋找 \_ 任何</span><span class="sxs-lookup"><span data-stu-id="2c973-206">CTL\_FIND\_ANY</span></span>
-   <span data-ttu-id="2c973-207">CTL \_ 尋找 \_ SHA1 \_ 雜湊</span><span class="sxs-lookup"><span data-stu-id="2c973-207">CTL\_FIND\_SHA1\_HASH</span></span>
-   <span data-ttu-id="2c973-208">CTL \_ 尋找 \_ MD5 \_ 雜湊</span><span class="sxs-lookup"><span data-stu-id="2c973-208">CTL\_FIND\_MD5\_HASH</span></span>
-   <span data-ttu-id="2c973-209">CTL \_ 尋找 \_ 使用方式</span><span class="sxs-lookup"><span data-stu-id="2c973-209">CTL\_FIND\_USAGE</span></span>
-   <span data-ttu-id="2c973-210">CTL \_ 尋找 \_ 主體</span><span class="sxs-lookup"><span data-stu-id="2c973-210">CTL\_FIND\_SUBJECT</span></span>
-   <span data-ttu-id="2c973-211">CTL \_ 尋找 \_ 現有的</span><span class="sxs-lookup"><span data-stu-id="2c973-211">CTL\_FIND\_EXISTING</span></span>

<span data-ttu-id="2c973-212">\_針對上述每個尋找類型呼叫「尋找 CTL 回呼」。</span><span class="sxs-lookup"><span data-stu-id="2c973-212">The FIND\_CTL callback is called for each of the above find types.</span></span> <span data-ttu-id="2c973-213">傳遞至 [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore) 的參數會在 \_ \_ \_ \_ \_ 呼叫 find CTL 回呼之前，直接複製到 CERT STORE >prov FIND INFO 結構。</span><span class="sxs-lookup"><span data-stu-id="2c973-213">The parameters passed to [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore) are copied directly to the CERT\_STORE\_PROV\_FIND\_INFO structure before the FIND\_CTL callback is called.</span></span> <span data-ttu-id="2c973-214">如需 CERT STORE >prov find INFO 結構的不同尋找類型之域值的詳細資訊 \_ \_ \_ \_ ，請參閱 **CertFindCTLInStore**。</span><span class="sxs-lookup"><span data-stu-id="2c973-214">For details about the field values for the different find types of the CERT\_STORE\_PROV\_FIND\_INFO structure, see **CertFindCTLInStore**.</span></span>

<span data-ttu-id="2c973-215">CTL \_ 尋找 \_ 現有的 ctl 尋找類型有助於判斷 ctl 是否已存在於存放區中，然後再進行 ctl 新增。</span><span class="sxs-lookup"><span data-stu-id="2c973-215">The CTL\_FIND\_EXISTING CTL find type helps determine whether the CTL already exists in the store before doing a CTL add.</span></span>

<span data-ttu-id="2c973-216">針對 CTL \_ FIND \_ EXISTING， *pvFindPara* 是 ctl [**\_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context) 結構的指標，可判斷它是否已存在於存放區中。</span><span class="sxs-lookup"><span data-stu-id="2c973-216">For CTL\_FIND\_EXISTING, *pvFindPara* is a pointer to the [**CTL\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context) structure of the CTL to determine whether it already exists in the store.</span></span>

 

 
