---
title: 取得服務和使用者 SDOs
description: 若要取得 NPS (IAS) 或特定使用者的 SDOs，請呼叫 ISdoMachine GetServiceSDO 或 ISdoMachine GetUserSDO 方法。
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c7562c3b7c6aa1150ba3ce6581441064eb386f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315712"
---
# <a name="obtaining-service-and-user-sdos"></a><span data-ttu-id="8bac2-103">取得服務和使用者 SDOs</span><span class="sxs-lookup"><span data-stu-id="8bac2-103">Obtaining Service and User SDOs</span></span>

> [!Note]  
> <span data-ttu-id="8bac2-104">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="8bac2-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="8bac2-105">若要取得 NPS (IAS) 或特定使用者的 SDOs，請呼叫 [**ISdoMachine：： GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) 或 [**ISdoMachine：： GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) 方法。</span><span class="sxs-lookup"><span data-stu-id="8bac2-105">To obtain SDOs for NPS (IAS) or a particular user, call the [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) methods.</span></span> <span data-ttu-id="8bac2-106">這些方法會傳回這些物件的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="8bac2-106">These methods return pointers to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interfaces for these objects.</span></span> <span data-ttu-id="8bac2-107">若為使用者 SDO，請使用 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法來取得物件的 [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) 介面。</span><span class="sxs-lookup"><span data-stu-id="8bac2-107">For the user SDO, use the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object.</span></span> <span data-ttu-id="8bac2-108">針對服務 SDO，請使用 **IUnknown：： QueryInterface** 來取得 [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) 介面或 [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="8bac2-108">For the service SDO, use **IUnknown::QueryInterface** to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface or [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) interface.</span></span>

<span data-ttu-id="8bac2-109">在呼叫 [**ISdoMachine：： GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) 或 [**ISdoMachine：： GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)之前，請先呼叫 [**ISdoMachine：： Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) ，以將電腦物件與本機電腦產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8bac2-109">Before calling either [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), call [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) to associate the machine object with the local computer.</span></span>

<span data-ttu-id="8bac2-110">如需示範如何取得這些 SDOs 的範例程式碼，請參閱 [取出服務 sdo](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) 和取得 [使用者 SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) 。</span><span class="sxs-lookup"><span data-stu-id="8bac2-110">See [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) and [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) for sample code that demonstrates how to obtain these SDOs.</span></span>

 

 