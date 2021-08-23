---
description: 適用于應用程式開發的應用程式安全性評定建議 Windows 安全性軟體和安全軟體發展，包括應用程式安全性測試。
ms.assetid: bb0ddae2-f559-4785-97c7-182fc204fa60
title: 安全性 Api 的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 934bf52d99456d599f91ec23c6e5472bb4e130565cf1acb56763f29f6396c0b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622878"
---
# <a name="best-practices-for-the-security-apis"></a>安全性 Api 的最佳作法

為了協助開發安全的軟體，我們建議您在開發應用程式時使用下列最佳作法。 如需詳細資訊，請參閱 [安全性開發人員中心](https://msdn.microsoft.com/security/default.aspx)。

## <a name="security-development-life-cycle"></a>安全性開發生命週期

 (SDL) 的 [安全性開發生命週期](/previous-versions/ms995349(v=msdn.10)) ，是將一系列以安全性為焦點的活動和交付專案，與軟體發展的每個階段進行協調的流程。 這些活動和交付專案包括：

-   開發威脅模型
-   使用程式碼掃描工具
-   進行程式碼審核和安全性測試

如需 SDL 的詳細資訊，請參閱 [Sdl Blog](https://blogs.msdn.com/sdl/archive/2007/04/26/welcome-to-the-sdl-blog.aspx)。

## <a name="threat-models"></a>威脅模型

進行威脅模型分析可協助您在程式碼中找出潛在的攻擊點。 如需有關威脅模型分析的詳細資訊，請參閱 Howard、Michael 和 LeBlanc、David \[ 2003 \] 、 *撰寫安全* 的程式碼、2d ed、ISBN 0-7356-1722-8、Microsoft 按壓、Redmond、華盛頓州。  (此資源可能無法在某些語言及國家/地區使用。 ) 

## <a name="service-packs-and-security-updates"></a>Service Pack 和安全性更新

組建和測試環境應該鏡像相同的 service pack 層級和目標使用者群的安全性更新。 建議您為任何屬於組建和測試環境的 Microsoft 平臺或應用程式安裝最新的 service pack 和安全性更新，並鼓勵您的使用者針對完成的應用程式環境進行相同的動作。 如需有關 service pack 和安全性更新的詳細資訊，請參閱[microsoft Windows Update](https://www.update.microsoft.com/microsoftupdate/v6/vistadefault.aspx?ln=en-us)和[microsoft 安全性](https://www.microsoft.com/security)。

## <a name="authorization"></a>授權

您應建立需要最低可能許可權的應用程式。 使用最低許可權可能會降低惡意程式碼危害電腦系統的風險。 如需在最低可能許可權層級中執行程式碼的詳細資訊，請參閱 [以特殊許可權](running-with-special-privileges.md)執行。

## <a name="more-information"></a>相關資訊

如需最佳作法的詳細資訊，請參閱下列主題。



| 主題                                                                                                                        | 描述                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [以特殊許可權執行](running-with-special-privileges.md)<br/>                                            | 討論權限的安全性含意。<br/>                                                                                                                                  |
| [避免緩衝區溢位](avoiding-buffer-overruns.md)<br/>                                                          | 提供有關避免緩衝區溢位的資訊。<br/>                                                                                                                            |
| [控制流程防護 (CFG) ](control-flow-guard.md)<br/>                                                                | 討論記憶體損毀弱點。<br/>                                                                                                                                    |
| [建立 DACL](creating-a-dacl.md)<br/>                                                                            | 說明如何使用 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) ，建立任意的存取控制清單 (DACL) 。<br/> |
| [處理密碼](handling-passwords.md)<br/>                                                                      | 討論使用密碼的安全性含意。<br/>                                                                                                                             |
| [如何優化您的 MSDN Library 搜尋](how-to-optimize-your-msdn-library-search.md)<br/>                          | 討論在 MSDN Library 上搜尋安全性 SDK 內容的選項。<br/>                                                                                                           |
| [動態存取控制開發人員擴充性](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)<br/> | 適用于新動態存取控制解決方案的一些開發人員擴充性點的基本導向。<br/>                                                                   |



 

 

