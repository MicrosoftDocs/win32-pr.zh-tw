---
description: 執行 COM + 資源配置器
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: 執行 COM + 資源配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111433"
---
# <a name="implementing-a-com-resource-dispenser"></a>執行 COM + 資源配置器

下列步驟概述執行 COM + 資源配置器的一般程式：

1.  決定 **RESTYPID** 格式，以分類資源彼此之間的差異。

2.  分別使用 Mtxdm 和 Mtxdm 標頭檔和程式庫。

3.  建立可執行 [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) 介面的 DLL，以及您想要公開給應用程式的 API。

4.  在啟動 ([*DllMain*](/windows/desktop/Dlls/dllmain) 或第一次呼叫分配 API) ，呼叫 [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) 函數。 這會將指標傳回給分配器管理員的 [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) 介面。

5.  呼叫 [**IDispenserManager：： RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser)，並將指標傳遞至您的 [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)執行。 這會導致分配管理員為您的資源配置器建立 (共用管理員) 的持有者，然後將指標傳回 [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) 介面。

6.  儲存這個指標，讓您可以呼叫 [**IHolder：： AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) 和 [**IHolder：： FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)。

7.  您現在可以 (回應對 API 的呼叫，) 呼叫 [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) 和 [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)。 **AllocResource** 一開始會透過回呼至您的 [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) 方法來回應，但後續的 **AllocResource** 呼叫會從不斷成長的資源集區中提供服務。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 資源配置器概念](com--resource-dispenser-concepts.md)
</dt> <dt>

[COM + 資源配置器介面](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
