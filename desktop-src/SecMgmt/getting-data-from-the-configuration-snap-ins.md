---
description: 附件嵌入式管理單元延伸模組無法直接查詢安全性資料庫以取得資訊。 相反地，它必須使用 ISceSvcAttachmentData：：的安全性設定嵌入式管理單元來查詢這項資訊。
ms.assetid: 1171beed-5b28-4f31-b33f-533e3c631b0d
title: 從設定嵌入式管理單元取得資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eda9bd6beb32ec762979bbfe804e15edea9bccd5160872dbd06ab0eb404a5e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969369"
---
# <a name="getting-data-from-the-configuration-snap-ins"></a>從設定嵌入式管理單元取得資料

附件嵌入式管理單元延伸模組無法直接查詢安全性資料庫以取得資訊。 相反地，它必須使用 [**ISceSvcAttachmentData：：**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata)的安全性設定嵌入式管理單元來查詢這項資訊。

附件嵌入式管理單元可以在初始化本身時取出所有資料，或在開啟其節點時取得資訊。

> [!Note]  
> 您必須使用 [**ISceSvcAttachmentData：： FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) 方法來釋出安全性設定嵌入式管理單元方法所配置的緩衝區 [**ISceSvcAttachmentData：：**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata)。

 

 

 



