---
title: 非 WHQL 簽署驅動程式的核心檢查
description: 若為清理安裝 Windows 10 的裝置，以及安全開機 (請注意，這在 Windows 8.0) 發行之後的所有新裝置都是標準的，而且所有新的驅動程式都必須經過 WHQL/Sysdev 簽署，而不只是使用交叉簽署的憑證。
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372473"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a>非 WHQL 簽署驅動程式的核心檢查

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

若為清理安裝 Windows 10 的裝置，以及安全開機 (請注意，這在 Windows 8.0) 發行之後的所有新裝置都是標準的，而且所有新的驅動程式都必須經過 WHQL/Sysdev 簽署，而不只是使用交叉簽署的憑證。 在此原則生效之前，已升級的裝置以及驅動程式已透過交叉憑證簽署的案例，會從此原則中排除，以確保回溯相容性。 此原則已于2015年4月宣佈，不過將會在2016年8月發行的 Windows 周年版中強制執行。

如果未正確簽署驅動程式，則會將它列為 PCA 通知，指出驅動程式 (s) 在未通過簽章需求的情況下遭到封鎖。 這可防止在幕後以透明方式封鎖的驅動程式離線使用者體驗。

如需詳細資訊，請參閱 [這篇 blog 文章](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/)，這篇文章宣佈驅動程式簽章變更。

 

 




