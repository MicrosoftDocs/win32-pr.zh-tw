---
description: CMSPCallMultiGraph 成員
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: CMSPCallMultiGraph 成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987559"
---
# <a name="cmspcallmultigraph-members"></a>CMSPCallMultiGraph 成員

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

等候區塊會儲存註冊到執行緒集區的等候相關資訊。 它包含 [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) 呼叫所傳回的等候控制碼，以及內容結構的指標。 陣列中的每個區塊都是針對其中一個資料流程物件中的圖形。 此陣列中的區塊位移與擁有圖形的資料流程位移相同。

 

 
