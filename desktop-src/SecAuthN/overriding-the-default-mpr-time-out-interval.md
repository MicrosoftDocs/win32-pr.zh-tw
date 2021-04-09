---
description: 多個提供者路由器 (MPR) 會呼叫 NPGetCaps，以找出網路提供者何時將開始 (nIndex 設定為 WNNC \_ 啟動) 。
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: 覆寫預設 MPR 逾時間隔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4308d94f4b16a7f67786c8a0856f23922e6f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944830"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a>覆寫預設 MPR 逾時間隔

[*多個提供者路由器*](../secgloss/m-gly.md) (MPR) 會呼叫 [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) ，以找出網路提供者何時將開始 (*nIndex* 設定為 WNNC \_ 啟動) 。 然後，MPR 會等待所有網路提供者所指定的最長超時時間，再向使用者呈現匯總的網路。 如果其中一個網路提供者不知道何時會開始，MPR 會使用該提供者的預設超時時間（60秒）。

如果有需要，系統管理員可以藉由建立下列登錄 **\_ DWORD** 登錄超時（其中 *n* 是逾時間隔，以毫秒為單位）來覆寫預設超時時間：

**HKEY \_LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **>restoretimeout**  =  *n*

下列虛擬程式碼會顯示 MPR 的完成時間處理的完整邏輯流程。


```C++
If there is a RegistryTimeout,
Then MaxTimeout = RegistryTimeout.
Otherwise,
MaxTimeout = 0.
For each provider,
if the provider does not supply a time-out and
if there is a RegistryTimeout,
ProviderTimeout is set to RegistryTimeout.
Otherwise,
ProviderTimeout is set to DefaultTimeout.
Otherwise,
If the ProviderTimeout is longer than MaxTimeout,
MaxTimeout = ProviderTimeout.
```



 

 
