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
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a><span data-ttu-id="e8b03-103">802.11 無線診斷可延伸的 Helper 類別</span><span class="sxs-lookup"><span data-stu-id="e8b03-103">802.11 Wireless Diagnostics Extensible Helper Classes</span></span>

<span data-ttu-id="e8b03-104">內建的無線診斷基礎結構有兩個擴充點。</span><span class="sxs-lookup"><span data-stu-id="e8b03-104">The built-in wireless diagnostics infrastructure has two extension points.</span></span>

| <span data-ttu-id="e8b03-105">父 Helper 類別</span><span class="sxs-lookup"><span data-stu-id="e8b03-105">Parent Helper Class</span></span>                                | <span data-ttu-id="e8b03-106">目的</span><span class="sxs-lookup"><span data-stu-id="e8b03-106">Purpose</span></span>                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e8b03-107">已修改原生 Wifi (RNWF) 可延伸的 Helper 類別</span><span class="sxs-lookup"><span data-stu-id="e8b03-107">Revised Native Wifi (RNWF) Extensible Helper Class</span></span> | <span data-ttu-id="e8b03-108">診斷與802.11 連接延伸模組相關的問題。</span><span class="sxs-lookup"><span data-stu-id="e8b03-108">Diagnoses issues related to 802.11 connectivity extensions.</span></span>       |
| <span data-ttu-id="e8b03-109">L2Security 可擴充的 Helper 類別</span><span class="sxs-lookup"><span data-stu-id="e8b03-109">L2Security Extensible Helper Class</span></span>                 | <span data-ttu-id="e8b03-110">診斷第2層安全性通訊協定延伸模組的相關問題。</span><span class="sxs-lookup"><span data-stu-id="e8b03-110">Diagnoses issues related to Layer 2 security protocol extensions.</span></span> |



 

> [!Note]  
> <span data-ttu-id="e8b03-111">協力廠商協助程式類別應該註冊兩個父項 helper 類別，以確保呼叫協力廠商類別。</span><span class="sxs-lookup"><span data-stu-id="e8b03-111">A third-party helper class should register with both parent helper classes to ensure that the third-party class gets called.</span></span> <span data-ttu-id="e8b03-112">如需註冊的詳細資訊，請參閱 [註冊 NDF Helper 類別延伸](registering-ndf-helper-class-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="e8b03-112">For more information about registration, see [Registering NDF Helper Class Extensions](registering-ndf-helper-class-extensions.md).</span></span>

 

## <a name="rnwf-extensible-helper-class"></a><span data-ttu-id="e8b03-113">RNWF 可擴充的 Helper 類別</span><span class="sxs-lookup"><span data-stu-id="e8b03-113">RNWF Extensible Helper Class</span></span>

<span data-ttu-id="e8b03-114">父 Helper 類別名稱</span><span class="sxs-lookup"><span data-stu-id="e8b03-114">Parent Helper Class Name</span></span>

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

<span data-ttu-id="e8b03-115">修訂的原生 Wifi (RNWF) 可延伸的協助程式類別，是協力廠商協助程式類別的父系，可診斷與擴充原生 Wifi 使用的802.11 通訊協定相關的問題。</span><span class="sxs-lookup"><span data-stu-id="e8b03-115">The Revised Native Wifi (RNWF) extensible helper class is the parent for third-party helper classes that diagnose issues related to extending 802.11 protocols used by Native Wifi.</span></span>

<span data-ttu-id="e8b03-116">RNWF helper 類別所提供的兩個索引鍵屬性是發生問題之介面的 GUID，以及連接內容。</span><span class="sxs-lookup"><span data-stu-id="e8b03-116">The two key attributes provided by the RNWF helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="e8b03-117">介面 GUID：此屬性的名稱為 "Interface ID"，且類型 **為 \_ GUID**。</span><span class="sxs-lookup"><span data-stu-id="e8b03-117">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="e8b03-118">連接內容：這個屬性的名稱為 Network ID，且的類型為 \_ 八位 \_ 字串。</span><span class="sxs-lookup"><span data-stu-id="e8b03-118">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="e8b03-119">此字串實際上是 \_ \_ Wlanihv 中定義的 WDIAG IHV WLAN \_ 識別碼結構的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e8b03-119">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in Wlanihv.h.</span></span> <span data-ttu-id="e8b03-120">此結構的定義如下。</span><span class="sxs-lookup"><span data-stu-id="e8b03-120">This structure is defined as follows.</span></span>

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
> <span data-ttu-id="e8b03-121">**WDIAG \_啟用的 IHV \_ WLAN \_ 識別碼 \_ 旗標 \_ 安全性 \_** 是唯一可能的 **dwFlags** 值。</span><span class="sxs-lookup"><span data-stu-id="e8b03-121">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="e8b03-122">協力廠商協助程式類別的相符屬性應該與其對應的軟體模組的服務識別碼相同。</span><span class="sxs-lookup"><span data-stu-id="e8b03-122">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="e8b03-123">這也是要在登錄中註冊協力廠商的相同名稱。</span><span class="sxs-lookup"><span data-stu-id="e8b03-123">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="e8b03-124">無線診斷將會在發生問題的無線會話期間查詢服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8b03-124">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="e8b03-125">這項資訊會傳回給 NDF，以判斷協力廠商協助程式類別是否存在並註冊，然後再呼叫。</span><span class="sxs-lookup"><span data-stu-id="e8b03-125">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="e8b03-126">下表列出 RNWF 可擴充 helper 類別的相符屬性。</span><span class="sxs-lookup"><span data-stu-id="e8b03-126">The following table lists the matching attributes for the RNWF extensible helper class.</span></span>



| <span data-ttu-id="e8b03-127">名稱</span><span class="sxs-lookup"><span data-stu-id="e8b03-127">Name</span></span>          | <span data-ttu-id="e8b03-128">類型</span><span class="sxs-lookup"><span data-stu-id="e8b03-128">Type</span></span>    | <span data-ttu-id="e8b03-129">值</span><span class="sxs-lookup"><span data-stu-id="e8b03-129">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="e8b03-130">DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="e8b03-130">DiagnosticsID</span></span> | <span data-ttu-id="e8b03-131">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="e8b03-131">REG\_SZ</span></span> | <span data-ttu-id="e8b03-132">\[DiagnosticsID \_ GUID \_ 字串</span><span class="sxs-lookup"><span data-stu-id="e8b03-132">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="l2security-extensible-helper-class"></a><span data-ttu-id="e8b03-133">L2Security 可擴充的 Helper 類別</span><span class="sxs-lookup"><span data-stu-id="e8b03-133">L2Security Extensible Helper Class</span></span>

<span data-ttu-id="e8b03-134">父 Helper 類別名稱</span><span class="sxs-lookup"><span data-stu-id="e8b03-134">Parent Helper Class Name</span></span>

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

<span data-ttu-id="e8b03-135">第2層安全性 (L2Security) 可延伸的 helper 類別是協力廠商協助程式類別的父系，可診斷與取代第2層安全性功能的對應服務和軟體模組相關的問題。</span><span class="sxs-lookup"><span data-stu-id="e8b03-135">The Layer 2 Security (L2Security) extensible helper class is the parent for third-party helper classes that diagnose issues related to corresponding services and software modules that replace Layer 2 Security functionality.</span></span>

<span data-ttu-id="e8b03-136">第2層安全性協助程式類別所提供的兩個索引鍵屬性是發生問題之介面的 GUID，以及連接內容。</span><span class="sxs-lookup"><span data-stu-id="e8b03-136">The two key attributes provided by the Layer 2 Security helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="e8b03-137">介面 GUID：此屬性的名稱為 "Interface ID"，且類型 **為 \_ GUID**。</span><span class="sxs-lookup"><span data-stu-id="e8b03-137">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="e8b03-138">連接內容：這個屬性的名稱為 Network ID，且的類型為 \_ 八位 \_ 字串。</span><span class="sxs-lookup"><span data-stu-id="e8b03-138">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="e8b03-139">此字串實際上是 \_ \_ wlanihv 中定義的 WDIAG IHV WLAN \_ 識別碼結構的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e8b03-139">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in wlanihv.h.</span></span> <span data-ttu-id="e8b03-140">此結構的定義如下。</span><span class="sxs-lookup"><span data-stu-id="e8b03-140">This structure is defined as follows.</span></span>

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
> <span data-ttu-id="e8b03-141">**WDIAG \_啟用的 IHV \_ WLAN \_ 識別碼 \_ 旗標 \_ 安全性 \_** 是唯一可能的 **dwFlags** 值。</span><span class="sxs-lookup"><span data-stu-id="e8b03-141">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="e8b03-142">協力廠商協助程式類別的相符屬性應該與其對應的軟體模組的服務識別碼相同。</span><span class="sxs-lookup"><span data-stu-id="e8b03-142">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="e8b03-143">這也是要在登錄中註冊協力廠商的相同名稱。</span><span class="sxs-lookup"><span data-stu-id="e8b03-143">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="e8b03-144">無線診斷將會在發生問題的無線會話期間查詢服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8b03-144">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="e8b03-145">這項資訊會傳回給 NDF，以判斷協力廠商協助程式類別是否存在並註冊，然後再呼叫。</span><span class="sxs-lookup"><span data-stu-id="e8b03-145">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="e8b03-146">下表列出第2層安全性可延伸 helper 類別的相符屬性。</span><span class="sxs-lookup"><span data-stu-id="e8b03-146">The following table lists the matching attributes for the Layer 2 Security extensible helper class.</span></span>



| <span data-ttu-id="e8b03-147">名稱</span><span class="sxs-lookup"><span data-stu-id="e8b03-147">Name</span></span>          | <span data-ttu-id="e8b03-148">類型</span><span class="sxs-lookup"><span data-stu-id="e8b03-148">Type</span></span>    | <span data-ttu-id="e8b03-149">值</span><span class="sxs-lookup"><span data-stu-id="e8b03-149">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="e8b03-150">DiagnosticsID</span><span class="sxs-lookup"><span data-stu-id="e8b03-150">DiagnosticsID</span></span> | <span data-ttu-id="e8b03-151">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="e8b03-151">REG\_SZ</span></span> | <span data-ttu-id="e8b03-152">\[DiagnosticsID \_ GUID \_ 字串</span><span class="sxs-lookup"><span data-stu-id="e8b03-152">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="matching-attributes"></a><span data-ttu-id="e8b03-153">相符屬性</span><span class="sxs-lookup"><span data-stu-id="e8b03-153">Matching Attributes</span></span>

<span data-ttu-id="e8b03-154">**DiagnosticsID**</span><span class="sxs-lookup"><span data-stu-id="e8b03-154">**DiagnosticsID**</span></span>

<span data-ttu-id="e8b03-155">802.11 無線診斷將會從核心原生 Wifi 服務查詢 *DiagnosticsID* ，以找出是否已安裝任何協力廠商無線延伸模組或安全性模組，以及是否包含在連接中。</span><span class="sxs-lookup"><span data-stu-id="e8b03-155">802.11 Wireless Diagnostics will query the *DiagnosticsID* from the core Native Wifi service in order to find out if any third-party wireless extensions or security modules are installed and involved in the connection.</span></span> <span data-ttu-id="e8b03-156">接著，無線診斷會使用 *DiagnosticsID* 做為相符的屬性，為這些協力廠商協助程式類別提供假設。</span><span class="sxs-lookup"><span data-stu-id="e8b03-156">Wireless Diagnostics will then provide hypotheses to these third-party helper classes using the *DiagnosticsID* as the matching attribute.</span></span> <span data-ttu-id="e8b03-157">任何協力廠商協助程式類別都應該包含在中，並隨相關聯的驅動程式套件一起安裝。</span><span class="sxs-lookup"><span data-stu-id="e8b03-157">Any third-party helper classes should be included in and installed with the associated driver package.</span></span> <span data-ttu-id="e8b03-158">*DiagnosticsID* 將會定義在微型功能 INF 檔案中，做為 [AddReg](https://msdn.microsoft.com/library/ms794514.aspx)指示詞中的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="e8b03-158">The *DiagnosticsID* will be defined in the miniport INF file as a registry key in the [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) directive.</span></span>

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

<span data-ttu-id="e8b03-159">此機碼定義協力廠商軟體模組的無線協助程式類別的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8b03-159">This key defines the ID of the wireless helper class for the third-party software module.</span></span> <span data-ttu-id="e8b03-160">這是擴充性架構的選擇性索引鍵，但如果此執行包含的 IHV 無線協助程式類別會插入 NDF 並可診斷與 RNWF 無線或安全性延伸模組相關的連線問題，則需要此金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8b03-160">This key is optional for the extensibility framework, but it is needed if the implementation includes an IHV Wireless Helper Class that plugs into NDF and can diagnose connectivity problems related to the RNWF wireless or security extensions.</span></span> <span data-ttu-id="e8b03-161">MS WLAN 診斷協助程式類別將會在安裝 IHV 模組時，從無線自動設定服務查詢此識別碼，並在診斷會話期間提供此識別碼做為 NDF 的參考或相符屬性，讓 NDF 可以在必要時呼叫適當的協力廠商無線協助程式類別。</span><span class="sxs-lookup"><span data-stu-id="e8b03-161">MS WLAN diagnostics helper classes will query this ID from the Wireless Auto Configuration Service when IHV modules are installed and will provide this ID as the reference or matching attribute to NDF during a diagnostics session so that NDF can call the appropriate third-party wireless helper class when necessary.</span></span>

<span data-ttu-id="e8b03-162">**\[DiagnosticsID \_ GUID \_ 字串\]**</span><span class="sxs-lookup"><span data-stu-id="e8b03-162">**\[DiagnosticsID\_GUID\_String\]**</span></span>

<span data-ttu-id="e8b03-163">此值必須是所有大寫字母的字串。</span><span class="sxs-lookup"><span data-stu-id="e8b03-163">This value must be a string of all uppercase letters.</span></span> <span data-ttu-id="e8b03-164">例如，"{12345678-9ABC-DEF0-1234-56789ABCDEF0}"。</span><span class="sxs-lookup"><span data-stu-id="e8b03-164">For example, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".</span></span>

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a><span data-ttu-id="e8b03-165">802.11 無線診斷 Helper 類別的範圍</span><span class="sxs-lookup"><span data-stu-id="e8b03-165">Scope of 802.11 Wireless Diagnostics Helper Classes</span></span>

<span data-ttu-id="e8b03-166">802.11 無線診斷協助程式類別目前會診斷下欄區域中的無線問題。</span><span class="sxs-lookup"><span data-stu-id="e8b03-166">802.11 wireless diagnostics helper classes currently diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="e8b03-167">任何802.11 連線問題，包括802.11 關聯、802.11 驗證、與802.11 標準相關的802.11 安全性設定 & 在作業系統中原本就支援的通訊協定，以及效能問題。</span><span class="sxs-lookup"><span data-stu-id="e8b03-167">Any 802.11 connectivity issues including 802.11 association, 802.11 authentication, 802.11 security settings related to 802.11 standards & protocols natively supported in the operating system, and performance issues.</span></span>
-   <span data-ttu-id="e8b03-168">802.1 x 設定和第2層驗證相關問題的第2層安全性問題，其使用 Windows Vista 和 Windows Server 2008 原生支援的方法。</span><span class="sxs-lookup"><span data-stu-id="e8b03-168">Layer 2 Security issues with regards to 802.1x configurations and any issues related to layer 2 authentication using methods natively supported on Windows Vista and Windows Server 2008.</span></span>
-   <span data-ttu-id="e8b03-169">用戶端與存取點之間的設定檔設定不符，或是網路基礎結構和服務。</span><span class="sxs-lookup"><span data-stu-id="e8b03-169">Configuration mismatches in profile settings between the client and the Access Point or the network infrastructure and services.</span></span>

<span data-ttu-id="e8b03-170">802.11 無線診斷協助程式類別目前不會診斷下欄區域中的無線問題。</span><span class="sxs-lookup"><span data-stu-id="e8b03-170">802.11 wireless diagnostics helper classes currently do not diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="e8b03-171">與協力廠商802.11 延伸模組相關的問題，包括與這些擴充功能相關的任何設定檔或驅動程式設定。</span><span class="sxs-lookup"><span data-stu-id="e8b03-171">Issues related to third-party 802.11 extensions including any profile or driver settings related to these extensions.</span></span>
-   <span data-ttu-id="e8b03-172">協力廠商 EAP 方法的相關問題。</span><span class="sxs-lookup"><span data-stu-id="e8b03-172">Issues related to third-party EAP methods.</span></span>
-   <span data-ttu-id="e8b03-173">無線微型埠驅動程式問題。</span><span class="sxs-lookup"><span data-stu-id="e8b03-173">Wireless miniport driver issues.</span></span>
-   <span data-ttu-id="e8b03-174">任何802.11 和第2層安全性通訊協定，或非原生支援的標準相關問題。</span><span class="sxs-lookup"><span data-stu-id="e8b03-174">Any 802.11 and layer 2 security protocol or standards-related issues that are not natively supported.</span></span>
-   <span data-ttu-id="e8b03-175">可能會影響無線連線能力的系統或元件層級問題，例如電源管理、磁碟空間不足、記憶體狀況和硬體問題。</span><span class="sxs-lookup"><span data-stu-id="e8b03-175">System or component-level issues that might impact wireless connectivity, such as power management, low disk space, memory conditions, and hardware problems.</span></span>

<span data-ttu-id="e8b03-176">此外，802.11 無線診斷無法分析 [**HighUtilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) 案例。</span><span class="sxs-lookup"><span data-stu-id="e8b03-176">Additionally, 802.11 Wireless Diagnostics does not analyze [**HighUtilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) cases.</span></span> <span data-ttu-id="e8b03-177">已識別的無線效能問題將會進行分析，並回報為 [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) 案例。</span><span class="sxs-lookup"><span data-stu-id="e8b03-177">Identified wireless performance issues will be analyzed and reported as [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) cases.</span></span>

 

 




