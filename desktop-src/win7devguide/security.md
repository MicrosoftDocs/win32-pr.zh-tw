---
title: Windows 7 開發人員指南) 安全性 (
description: Windows 7 包含全新和改進的安全性功能，可讓開發人員更輕鬆地改善、使用和管理其應用程式的安全性。
ms.assetid: c3f19338-8ada-4ded-82a9-ca0869ad469d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a3b317f2fe0c7d42559245108bae6a5dbf0e6f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106968127"
---
# <a name="security-windows-7-developer-guide"></a>Windows 7 開發人員指南) 安全性 (

Windows 7 包含全新和改進的安全性功能，可讓開發人員更輕鬆地改善、使用和管理其應用程式的安全性。 它提供了各種新的安全性功能，不僅有助於抵禦威脅，也可限制攻擊者在取得電腦的存取權時所能做的損害。

Windows 篩選平台的增強功能可讓開發人員建立應用程式，以與作業系統網路堆疊中的封包處理進行互動。 您可以篩選網路資料，也可以在到達目的地之前加以修改。

此外，由於 Windows 許可權模型的變更，開發人員和使用者可以更容易管理系統安全性。 新的增強功能可讓您輕鬆地識別重要提示，以確保使用者可以存取所需的應用程式和功能，而不會危害其系統。  (參閱 [MSDN 安全性開發人員中心](https://msdn.microsoft.com/security/default.aspx)。 ) 

## <a name="windows-filtering-platform"></a>Windows 篩選平台

在 Windows 7 中，已增強 Windows 篩選平台，讓開發人員能夠更充分掌控防火牆功能。 篩選層級已增加，且 *isv* 現在可以在較低層級插入自訂保護和偵測。 此外，防火牆開發人員可以選擇性地開啟或關閉 Windows 防火牆的元件。

開發人員可以使用 Windows 篩選平台，在其應用程式中建立防火牆、入侵偵測系統、防毒程式、網路監視工具和家長監護。 Windows 篩選平台會與整合，並提供各種防火牆功能的支援，包括根據應用程式使用通訊端 API (以應用程式為基礎的原則) 的驗證通訊和動態防火牆設定。 Windows 篩選平台也提供原則管理、變更通知、網路診斷和具狀態篩選的基礎結構。

Windows Vista 中的 Windows 篩選平台的初始架構提供以 IP 為基礎的流量功能。 其他非 IP 通訊協定（例如位址解析通訊協定） (ARP) 和媒體存取控制 (*MAC*) 層通訊協定來進行網路管理和驗證，也需要篩選、檢查或記錄。 在 Windows 7 中，已提供支援 *MAC* 和 *ETHERNET* 篩選的 *NDIS* 檢查層，以滿足這項需求。  (參閱 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。 ) 

## <a name="user-account-control"></a>使用者帳戶控制

 (UAC) 的使用者帳戶控制是 Windows 7 中的安全性元件，可讓開發人員建立應用程式，讓使用者以非系統管理員身分執行一般工作。 開發人員可以使用標準使用者權杖來執行應用程式，以降低安全性風險，進而降低錯誤或攻擊的風險。

屬於本機 *Administrators* 群組成員的使用者帳戶將以標準使用者的身分執行大部分的應用程式。 UAC 藉由分隔使用者和系統管理員功能，同時提高生產力，讓開發人員能夠更充分掌控使用者對應用程式受保護區域的存取層級。 UAC 會在 *安全桌面* 模式下要求認證，其中整個螢幕都會受到保護，以防止使用者介面或滑鼠詐騙。  (參閱 [ [使用者帳戶控制] 對話方塊更新](../win7appqual/user-interface---user-account-control-dialog-updates.md) 和 [ [使用者帳戶控制] 和 [WMI](../wmisdk/user-account-control-and-wmi.md)]。 ) 

 

 
