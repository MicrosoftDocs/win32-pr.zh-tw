---
description: 資源配置器資源配置進程
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: 資源配置器資源配置進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e91802b001bdb8a1af3a933d458c4e9b86b6e3bcd2eb40646e9b64a2e2e14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953818"
---
# <a name="resource-dispenser-resource-allocation-process"></a>資源配置器資源配置進程

每次資源配置器從其持有者配置資源時，就會發生下列情況：

1.  資源配置器會宣告 (**RESTYPID**) 的資源類型識別碼，描述所需的資源類型。

2.  資源配置器會呼叫持有者的 [**IHolder：： AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) 方法，並傳遞此 **RESTYPID**。

3.  持有者會從可用的資源產生候選清單。 候選項目是指未在交易中登記，或已在呼叫物件的交易中登記的資源。

4.  這些候選項目會個別傳遞至 [**IDispenserDriver：： RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) 方法，在此方法中，會根據候選資源與所需的 **RESTYPID** 有多好，以0到) 100 的級別 (。

5.  持有者會選擇資源配置者費率最高的資源。

6.  資源配置器可以提早終止評等迴圈，方法是將候選資源分級為 100 (完美符合) 。 通常會針對已正確登記的候選資源保留100的評等，除非資源配置程式最後會將登記視為便宜的作業。 如果所有的候選資源 (如果有任何) 分級為 0 (無法使用) ，則會藉由呼叫 [**IDispenserDriver：： CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource)來建立新的資源。

7.  如果先前選擇的資源尚未登記在呼叫物件的交易中，則會呼叫資源配置程式的 [**IDispenserDriver：： EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) 方法。

8.  [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource)方法呼叫會傳回具有已登錄資源的資源配置器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 資源配置器概念](com--resource-dispenser-concepts.md)
</dt> <dt>

[在交易中登記資源](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[追蹤未配置的資源](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



