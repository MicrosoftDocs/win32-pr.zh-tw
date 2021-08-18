---
title: 取得服務和使用者 SDOs
description: 若要取得 NPS (IAS) 或特定使用者的 SDOs，請呼叫 ISdoMachine GetServiceSDO 或 ISdoMachine GetUserSDO 方法。
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebef1e695236bd1449ab886cb998a67f09c2cafc8ded446b0b7e1ad89b01181
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128588"
---
# <a name="obtaining-service-and-user-sdos"></a>取得服務和使用者 SDOs

> [!Note]  
> 網際網路驗證服務 (IAS) 已重新命名網路原則伺服器 (NPS) 從 Windows Server 2008 開始。

 

若要取得 NPS (IAS) 或特定使用者的 SDOs，請呼叫 [**ISdoMachine：： GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) 或 [**ISdoMachine：： GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) 方法。 這些方法會傳回這些物件的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。 若為使用者 SDO，請使用 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法來取得物件的 [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) 介面。 針對服務 SDO，請使用 **IUnknown：： QueryInterface** 來取得 [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) 介面或 [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) 介面。

在呼叫 [**ISdoMachine：： GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) 或 [**ISdoMachine：： GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)之前，請先呼叫 [**ISdoMachine：： Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) ，以將電腦物件與本機電腦產生關聯。

如需示範如何取得這些 SDOs 的範例程式碼，請參閱 [取出服務 sdo](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) 和取得 [使用者 SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) 。

 

 