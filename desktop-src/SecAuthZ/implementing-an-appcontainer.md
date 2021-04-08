---
description: AppContainer 的執行方式是將新的資訊新增至處理常式權杖、變更 SeAccessCheck () ，讓所有舊版、未修改的存取控制清單 (ACL) 物件預設會封鎖來自 AppContainer 進程的存取要求，以及可供 AppContainers 使用的重新 ACL 物件。
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: 執行 AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851695"
---
# <a name="implementing-an-appcontainer"></a>執行 AppContainer

AppContainer 的執行方式是將新的資訊新增至處理常式權杖、變更 [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) ，讓所有舊版、未修改的存取控制清單 (ACL) 物件預設會封鎖來自 AppContainer 進程的存取要求，以及可供 AppContainers 使用的重新 ACL 物件。

## <a name="the-process"></a>程序

首先，新增處理常式權杖的新資訊。 然後變更 **SeAccessCheck ()** ，如此一來，所有舊版、未修改的 acl 預設將會封鎖來自 AppContainer 進程的存取要求。 最後，應可供 AppContainers 的重新 ACL 資源

AppContainer SID 是 appcontainer 的持續性唯一識別碼。 功能 Sid 會將資源群組的存取權授與 AppContainers 群組。 AppContainerNumber 是用來區別 AppContainers 的暫時性 **DWORD** 。 不過，它不應該用來作為 AppContainer 的身分識別。

若要允許單一 AppContainer 存取資源，請將其 AppContainerSID 新增至該資源的 ACL。

若要允許數個特定 AppContainers 存取資源，請將其所有 AppContainerSIDs 新增至該資源的 ACL。

若要管理許可權群組，請建立 (GUID) 的功能 SID，並將該功能 SID 放在要授與的所有資源上。 然後將功能 SID 新增至您的進程權杖。

若要允許所有 AppContainers 存取資源，請將 **所有應用程式封裝** SID 新增至該資源的 ACL。 這相當於萬用字元。

AppContainerSID 和 CapabilitySID 都支援存取控制專案 (ACE) 的存取遮罩。 適當設定。

 

 
