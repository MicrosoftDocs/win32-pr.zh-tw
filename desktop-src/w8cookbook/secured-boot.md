---
title: 早期啟動反惡意程式碼
description: 早期啟動反惡意程式碼
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1ca8e52f9d2465038e68b6b585bed70b974432566b3b67d080c97bb998103f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852194"
---
# <a name="early-launch-antimalware"></a>早期啟動反惡意程式碼

## <a name="platforms"></a>平台

 **客戶** 端-Windows 8  
**伺服器**-Windows Server 2012  

## <a name="description"></a>描述

由於反惡意程式碼 (AM) 軟體在偵測到執行時間惡意程式碼時變得更好且更好，攻擊者也會在建立可隱藏偵測的 rootkit 時變得更好。 偵測開機週期初期啟動的惡意程式碼，是大部分的廠商都能處理的挑戰。 一般情況下，它們會建立主機作業系統不支援的系統駭客，而且實際上會導致電腦處於不穩定的狀態。 到目前為止，Windows 尚未提供良好的方式來偵測並解決這些早期開機的威脅。

Windows 8 引進稱為「安全開機」的新功能，可保護 Windows 開機設定和元件，並載入早期啟動的反惡意程式碼 (ELAM) 驅動程式。 此驅動程式會在其他開機啟動驅動程式之前啟動，並可讓您評估這些驅動程式，並協助 Windows 核心決定是否應該將它們初始化。

## <a name="manifestation"></a>表現

藉由核心先啟動，ELAM 可確保在任何協力廠商軟體之前啟動，因此能夠偵測開機程式中的惡意程式碼，並防止它初始化。

## <a name="mitigation"></a>降低

開機驅動程式會根據根據初始化原則從 ELAM 驅動程式傳回的分類進行初始化。 依預設，此原則會初始化已知的良好和未知驅動程式，但不會初始化已知的不良驅動程式。 系統管理員可以透過群組原則來指定自訂原則，以防止未知的驅動程式初始化，或可啟用開機程式不可或缺的驅動程式，但已遭篡改、開機以進行初始化。

## <a name="solution"></a>解決方案

ELAM 驅動程式必須註冊核心回呼，以取得每個開機啟動驅動程式初始化時的相關資訊。 然後，ELAM 驅動程式就可以針對每個驅動程式傳回分類。 這些是必要的功能：

-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

ELAM 驅動程式也可以註冊登錄回呼。 這麼做可讓 ELAM 驅動程式檢查每個開機啟動驅動程式所使用的設定資料。 然後，ELAM 驅動程式就可以在開機啟動驅動程式使用之前，先封鎖或修改資料（如有必要）。 這些是必要的功能：

-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

如需 ELAM 驅動程式需求和 API 使用方式的詳細資訊，請參閱 [早期啟動反惡意](/windows-hardware/drivers/install/early-launch-antimalware)代碼。

## <a name="tests"></a>測試

ELAM 驅動程式必須由 Microsoft 特別簽署，以確保在開機程式初期由 Windows 核心啟動。 若要取得簽章，ELAM 驅動程式必須通過一組認證測試，以驗證效能和其他行為。 這些測試都包含在 Windows 硬體認證套件中。

## <a name="resources"></a>資源

-   [早期啟動反惡意程式碼](/windows-hardware/drivers/install/early-launch-antimalware)
-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [使用 Windows 硬體認證套件組建會議簡報來認證硬體](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [下載套件和工具](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
