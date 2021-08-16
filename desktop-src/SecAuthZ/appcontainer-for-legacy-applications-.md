---
description: AppContainer 環境是一個限制性的進程執行環境，可用於繼承應用程式以提供資源安全性。
ms.assetid: 28498D4E-DCA4-4A85-B474-C3C328BD3022
title: 繼承應用程式的 AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e0cdf21fc4008f1da0d55edb17abaf71978f4a5384843ecff60793b3d5b19a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784731"
---
# <a name="appcontainer-for-legacy-applications"></a>繼承應用程式的 AppContainer

AppContainer 環境是一個限制性的進程執行環境，可用於繼承應用程式以提供資源安全性。 在 AppContainer 中執行的應用程式只能存取專門授與它的資源。 如此一來，在 AppContainer 中執行的應用程式將無法被駭客入侵，以允許在有限指派的資源以外的惡意動作。

## <a name="benefits-of-using-an-appcontainer-environment"></a>使用 AppContainer 環境的優點

AppContainer 環境提供應用程式的安全沙箱處理。 這會隔離應用程式，使其不需特定許可權即可存取硬體、檔案、登錄、其他應用程式、網路連線和網路資源。 個別資源可能會被設為目標，而不會公開其他資源。 此外，使用者身分識別會使用屬於使用者串連的唯一身分識別進行保護，而應用程式則會使用最低許可權模型來授與資源。 這可進一步防止應用程式模擬使用者，以取得其他資源的存取權。

如需針對繼承應用程式使用 AppContainer 的詳細資訊，請參閱下列主題。

## <a name="in-this-section"></a>本節內容



| 主題                                                                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppContainer 隔離](appcontainer-isolation.md)<br/>             | 隔離是 AppContainer 執行環境的主要目標。 藉由將應用程式與不需要的資源和其他應用程式隔離，可將惡意操作的機會降到最低。 根據最低許可權授與存取權，可防止應用程式和使用者存取其權利以外的資源。 控制資源的存取可保護進程、裝置和網路。<br/> |
| [執行 AppContainer](implementing-an-appcontainer.md)<br/> | AppContainer 的執行方式是將新的資訊新增至處理常式權杖、變更 [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) ，讓所有舊版、未修改的存取控制清單 (ACL) 物件預設會封鎖來自 AppContainer 進程的存取要求，以及可供 AppContainers 使用的重新 ACL 物件。<br/>                                                                                        |



 

 

