---
title: EAP 安裝
description: 廠商會在動態連結程式庫中執行 EAPs，也稱為驗證通訊協定， (Dll) 。
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104373987"
---
# <a name="eap-installation"></a>EAP 安裝

廠商會在動態連結程式庫中執行 EAPs，也稱為驗證通訊協定， (Dll) 。 驗證通訊協定的 DLL 必須同時位於用戶端和伺服器電腦上。 為了簡單起見，用戶端和伺服器 Dll 可能完全相同;不過，這不是必要條件。 此外，請注意，相同的 DLL 可能會支援多個驗證通訊協定。

廠商應提供安裝軟體以安裝和移除 DLL。 安裝軟體也應該在系統登錄中為驗證通訊協定建立適當的機碼和值，並在卸載時移除這些金鑰和值。

每個 EAP DLL 的安裝應該會建立下列登錄機碼。

**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Rasman** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**

在上述路徑中， **&lt; eaptypeid &gt;** 是驗證通訊協定的識別碼。 廠商必須從網際網路指派的號碼授權單位取得此識別碼 (IANA) 。

如需此機碼支援值的詳細資訊和描述，請參閱 [驗證通訊協定登錄值](authentication-protocol-registry-values.md)。

 

 




