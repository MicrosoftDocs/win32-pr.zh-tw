---
title: 生物特徵辨識架構總覽
description: 生物識別單元的原生支援會併入 Windows 中。
ms.assetid: 616ba95a-27a3-4eac-b802-5217954ed04e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f524437ba60f0ad5c1518225f91ff23c789a917
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463444"
---
# <a name="biometric-framework-overview"></a>生物特徵辨識架構總覽

每個人都有唯一的特性可用於識別。 這些特性通常是實體的，而且包含指紋等特性，但也可以包含行為特性，例如 gait 和輸入節奏。 生物特徵辨識詞彙包含這兩種意義。 生物特徵辨識資訊逐漸取代密碼以識別和驗證使用者。 這對使用者和系統管理員來說更安全，而且通常更方便。

感應器可用來捕捉生物特徵辨識資訊。 感應器會將此資訊視為生物特徵辨識範例。 單一範例包含的資料代表一個個人的單一生物特徵辨識特性。 建立生物特徵辨識範本的平均是多個範例，且範本會安全地儲存。 之後，來自未知使用者的範例會與已儲存的範本進行比較，以建立及驗證使用者身分識別。 Windows 生物識別服務（屬於 Windows 生物特徵辨識架構 (WBF) 的一部分）提供下列功能。 您可以使用 Windows 生物特徵辨識架構 API 來利用此功能。

-   擷取生物識別樣本並用來建立範本。
-   安全地儲存和取出生物特徵辨識範本。
-   將每個範本對應至唯一識別碼，例如 GUID 或 SID。

您也可以使用此 API 來延伸架構，以及建立生物特徵辨識感應器介面卡、相符引擎和儲存體元件。 如需建立感應器介面卡、相符引擎和儲存元件的詳細資訊，請參閱 [建立介面卡外掛程式](creating-adapter-plug-ins.md)。

## <a name="core-platform-components"></a>核心平臺元件

### <a name="windows-biometric-driver-interface-wbdi"></a>Windows 生物識別驅動程式介面 (WBDI)

WBDI 是一種程式設計介面，可供生物特徵辨識驅動程式用來透過 Windows 生物特徵辨識服務 (WBS) 公開生物特徵辨識裝置。 您可以使用任何支援的驅動程式技術來執行 WBDI 驅動程式，包括下列各項。 不過，我們建議您盡可能使用 UMDF 來改善驅動程式品質和系統穩定性。

-   使用者模式驅動程式架構 (的 UMDF) 
-   核心模式驅動程式架構 (KMDF) 
-   Windows Driver Model (WDM) 

WBDI 生物特徵辨識驅動程式也必須支援 WBDI 驅動程式介面 GUID 和所有必要的 i/o 控制項， (IOCTLs) 。 驅動程式開發人員應該複習 Windows 驅動程式套件 (WDK) 的檔和範例程式碼。

### <a name="windows-biometric-service-wbs"></a>Windows 生物特徵辨識服務 (WBS) 

Windows 生物特徵辨識服務會管理已安裝的生物特徵辨識驅動程式，並支援 Windows 生物特徵辨識架構 API 來提供用戶端應用程式的裝置存取權。 WBS 會執行下列功能：

-   它會將用戶端應用程式與生物特徵辨識資料分開，以保護使用者的機密性。
-   它會要求應用程式使用唯一識別碼來取得資料的存取權，以保護來自無許可權用戶端應用程式的生物特徵辨識資料。
-   它會使用稱為 [生物識別單位](/previous-versions//dd401512(v=vs.85)) 的軟體元件，透過標準化介面公開特定生物特徵辨識裝置的功能。
-   它會藉由將生物識別單位組成系統、私人或未指派的 [感應器](sensor-pools.md)集區來管理它們。
-   它支援針對缺乏上架處理或儲存功能的實體裝置使用生物識別單位 [介面卡](/previous-versions//dd401508(v=vs.85)) 。

### <a name="windows-biometric-framework-api"></a>Windows 生物特徵辨識架構 API

Windows 生物特徵辨識架構 API 可讓您建立可與 Windows 生物特徵辨識服務互動的用戶端應用程式，以執行下列動作：

-   識別並驗證使用者。
-   找出生物特徵辨識裝置並查詢其功能。
-   管理會話和監視事件。

## <a name="user-experience-components"></a>使用者體驗元件

### <a name="discovery-points"></a>探索點

終端使用者可以透過下列任何方式找出生物識別單元：

-   在 [開始搜尋] 文字方塊中輸入生物特徵辨識、指紋、臉部或其他相關片語，以啟動 [生物特徵辨識裝置] 控制台。 生物特徵辨識的結果清單可包含 Windows 10 映射上的下列專案。
    -   安裝指紋登入
    -   設定臉部登入

### <a name="supported-scenarios"></a>支援的案例

以下是支援的案例：

-   使用者可以使用指紋辨識器或焦點在臉部上的 IR 攝影機登入本機電腦、工作組或網域。
-   具有系統管理許可權的使用者可以使用指紋或臉部 (UAC) 來提升應用程式的使用者帳戶控制。

## <a name="management-components"></a>管理元件

您可以使用群組原則或行動裝置管理 (MDM) 來管理生物識別系統。

### <a name="biometric-system-management"></a>生物識別系統管理

您可以使用群組原則或 MDM 來管理生物特徵辨識功能。 群組原則可以進一步用來執行下列動作：

-   指定快速切換使用者的超時期間（如果是由 ISV 所執行的話）。
-   防止生物識別單元安裝。
-   強制移除生物特徵辨識裝置的驅動程式。
-   停用生物識別服務。

 

 