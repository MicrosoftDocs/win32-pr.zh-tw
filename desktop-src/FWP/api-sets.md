---
title: WFP API
description: Windows 的篩選平臺 (WFP) API 分成下列元件。
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eadbb3fb6383999b2bb8ef14c99ecb8beab3f88
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470145"
---
# <a name="wfp-api"></a>WFP API

Windows 的篩選平臺 (WFP) API 分成下列元件。




| 元件 | 描述 | 標頭檔 | 
|-----------|-------------|--------------|
| <a href="/windows-hardware/drivers/ddi/_netvista/">標注 API</a> (FWPS) $ {REMOVE} $<br /> | 由標注使用的<a href="/windows-hardware/drivers/ddi/_netvista/">資料類型</a>。<strong>注意</strong> 這些資料類型記載于 Microsoft Windows 驅動程式開發工具組 (DDK) 。<br /> | <dl> fwpstypes。h<br />fwpstypes .idl<br /></dl> | 
| 用來執行標注的<a href="/windows-hardware/drivers/ddi/_netvista/">函數</a>和<a href="/windows-hardware/drivers/ddi/_netvista/">列舉類型</a>。<strong>注意</strong> 這些函式和列舉類型記載于 DDK 中。<br /> | <dl> fwpsu。h<br />fwpsk。h<br /></dl> | 
| IKE/AuthIP API (IKEEXT) $ {REMOVE} $<br /> | 用來管理 IKE 和 AuthIP 主要模式 (MM) 原則和安全性關聯的<a href="fwp-enums.md">列舉類型</a>和<a href="fwp-structs.md">結構</a>。 | <dl> iketypes。h<br />iketypes .idl<br /></dl> | 
| <a href="fwp-ike-functions.md">用來</a> 管理 IKE 和 AuthIP MM 原則和安全性關聯的函式。 | <dl> fwpmu。h<br />fwpmk。h<br /></dl> | 
| IPsec API (IPSEC) $ {REMOVE} $<br /> | 用來管理 IPsec 原則和安全性關聯的<a href="fwp-enums.md">列舉類型</a>和<a href="fwp-structs.md">結構</a>。 | <dl> ipsectypes。h<br />ipsectypes .idl<br /></dl> | 
| <a href="fwp-ipsec-functions.md">用來</a> 管理 IPsec 原則和安全性關聯的函式。 | <dl> fwpmu。h<br />fwpmk。h<br /></dl> | 
| 管理 API (FWPM) $ {REMOVE} $<br /> | 用來管理篩選引擎的<a href="fwp-enums.md">列舉類型</a>和<a href="fwp-structs.md">結構</a>。 | <dl> fwpmtypes。h<br />fwpmtypes .idl<br /></dl> | 
| 用於管理篩選引擎的<a href="fwp-mgmt-functions.md">函數</a>。 這些函式是用來執行下列工作：<br /><ul><li>設定和查詢篩選、提供者和標注。</li><li>取出 IPsec 統計資料。</li><li>設定 Windows 篩選平台。</li></ul> | <dl> fwpmu。h<br />fwpmk。h<br /></dl> | 
| 共用 API (.FWP)  | 跨 Windows 篩選平台共用的基本<a href="fwp-enums.md">列舉類型</a>和<a href="fwp-structs.md">結構</a>。 | <dl> fwptypes。h<br />fwptypes .idl<br /></dl> | 




 

資料型別名稱全都是大寫和底線分隔。 名稱的開頭一律是識別其元件群組的前置詞，例如 [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0)。

函式名稱為混合大小寫和以大小寫分隔。 名稱的開頭一律是識別其元件群組的前置詞，例如 [**FwpmProviderCoNtextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0)。

大部分資料和函式名稱的結尾都是版本號碼。 Fwpvi .h 標頭檔會將與版本無關的資料和函式名稱對應至適用于指定作業系統的版本。 如需詳細資訊，請參閱[WFP Version-Independent 名稱，並以特定版本的 Windows 為目標](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md)。

每個元件都不會獨立。 例如，IKE 主要模式 (MM) 原則會定義在 IKEEXT 元件中，但會儲存在提供者內容中，並與在 FWPM API 元件中找到的篩選準則相關聯。

## <a name="user-mode-and-kernel-mode-public-header-files"></a>User-Mode 和 Kernel-Mode 公用標頭檔

您可以從使用者模式或核心模式呼叫大部分的 WFP 函數。 不過，使用者模式函數會傳回代表 Win32 錯誤碼的 **DWORD** 值，而核心模式函數則會傳回代表 NT 狀態碼的 **NTSTATUS** 值。 因此，使用者模式和核心模式之間的函式名稱和語義都相同，但函式簽章則否。 這需要函式原型的不同使用者模式和核心模式的特定標頭。 使用者模式標頭檔名稱的結尾是 "u"，核心模式標頭檔名稱則以 "k" 結尾。

下表列出定義 WFP 函數的 Win32 標頭檔。

| 標頭檔 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fwpmk。h      | FWPM、IPsec 和 IKEEXT 元件的核心模式函數原型。 僅適用于 DDK。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| fwpmu。h      | FWPM、IPsec 和 IKEEXT 元件的使用者模式函數原型。 僅適用于 Microsoft Windows 軟體開發套件 (SDK) 。                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| fwpsk。h      | FWPS 元件的核心模式函數原型和列舉類型。 僅適用于 DDK。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| fwpsu。h      | FWPS 元件的使用者模式函數原型和列舉類型。 僅適用于 Windows SDK。**注意** 使用者模式 FWPS 列舉類型與核心模式 FWPS 列舉類型相同。 因此，這些類型只記錄在 DDK 中。<br/> **注意**  使用者模式 FWPS 函式原型與核心模式 FWPS 函式原型相同，但傳回碼例外。 使用者模式 FWPS 函式會傳回 **DWORD**，而核心模式的 FWPS 函式會傳回一個 **NTSTATUS**。 因此，這些函式只會記錄在 DDK 中。<br/> |



 

所有使用者模式函數都會從 fwpuclnt.dll 匯出。 所有核心模式函數都會從 fwpkclnt.sys 匯出。

### <a name="management-fwpm-and-callout-fwps-data-types"></a>管理 (FWPM) 和標注 () 資料類型

大部分的 FWPM 資料類型（用於管理工作，例如從應用程式或驅動程式新增篩選或標注）都會有 FWPS 的對應專案。 FWPS 資料類型會在實際的網路流量篩選期間使用，而在分類的標注常式內容中。

例如，為了將篩選加入至特定篩選引擎層，程式設計人員應該使用 FWPM 類型，例如： `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` 。 若要檢查正在呼叫標注的圖層，程式設計人員應使用對應的 FWPS 類型： ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` 。

FWPM 資料類型的某些 FWPS 對應項會擴充原始 FWPM 資料類型。 例如，若要在許多篩選引擎層級加入篩選準則，程式設計人員會指定， `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` 無論篩選引擎層為何。 為了尋找篩選準則值，程式設計人員會指定圖層特定的 FWPS 類型，例如： `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` 。

FWPS 資料類型通常小於其 FWPM 對應專案。 例如， [**FWPM 篩選層識別碼**](management-filtering-layer-identifiers-.md) 是 (16 個位元組的 **GUID**) ，而 [FWPS 篩選層識別碼](/windows-hardware/drivers/network/management-filtering-layer-identifiers) 則為 **UINT16** (16 位) 。 FWPS 資料類型的較小大小可改善系統效能，因為整數比較超過了即時流量的 **GUID** 比較。 此外，核心記憶體會有效率地使用，因為 FWPS 類型全都在核心中用來管理篩選，而 FWPM 類型則以使用者模式儲存以管理不同的層級。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WFP API 物件模型](object-model.md)
</dt> <dt>

[WFP API 物件管理](object-management.md)
</dt> </dl>

