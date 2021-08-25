---
description: 重要的是這個 API 已被取代。
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: 密碼編譯服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7ef58122e47594b195700241b936b8985cd88137c52841976495b195d7e4c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876188"
---
# <a name="cryptographic-service-providers"></a>密碼編譯服務提供者

> [!IMPORTANT]
> 此 API 即將淘汰。 新的和現有的軟體應該開始使用 [新一代密碼編譯 api。](/windows/desktop/SecCNG/cng-portal) Microsoft 可能會在未來的版本中移除此 API。

 

[*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 包含密碼編譯標準和演算法的實施。 CSP 至少包含 [*動態連結程式庫*](../secgloss/d-gly.md) (DLL) ，可在 [*CryptoSPI*](../secgloss/c-gly.md) ([*系統程式介面*](../secgloss/s-gly.md)) 中執行函式。 大部分的 Csp 都包含所有自己的函式的實作為。 不過，某些 csp 會在 Windows 服務控制管理員管理的 Windows 型服務程式中，執行其功能。 其他人會在硬體中執行功能，例如 [*智慧卡*](../secgloss/s-gly.md) 或安全的副處理器。 如果 CSP 未執行自己的函式，則 DLL 會作為傳遞層，以加速作業系統與實際 CSP 實行之間的通訊。

本節包含下列主題。



| 主題                                                                                      | 目錄                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [密碼編譯提供者類型](cryptographic-provider-types.md)                           | 密碼編譯提供者類型是共用資料格式和密碼編譯通訊協定的密碼編譯服務提供者系列。 資料格式包括演算法 [*填補*](../secgloss/p-gly.md) 配置、 [*金鑰長度*](../secgloss/k-gly.md)和預設模式。 |
| [Microsoft 密碼編譯服務提供者](microsoft-cryptographic-service-providers.md) | Microsoft 目前提供之 Csp 的詳細資訊。                                                                                                                                                                                                                                                                                       |



 

 

 
