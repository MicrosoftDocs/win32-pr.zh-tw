---
description: 說明必須設定哪個登錄機碼，以防止自動播放。
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: 如何防止元件的自動播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebe03473ce7c5eb441ec428cbe4d060dc62f042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973137"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a><span data-ttu-id="8af0f-103">如何防止元件的自動播放</span><span class="sxs-lookup"><span data-stu-id="8af0f-103">How to Prevent AutoPlay for a Component</span></span>

<span data-ttu-id="8af0f-104">說明必須設定哪個登錄機碼，以防止自動播放。</span><span class="sxs-lookup"><span data-stu-id="8af0f-104">Illustrates which registry key must be set to prevent AutoPlay.</span></span>

## <a name="instructions"></a><span data-ttu-id="8af0f-105">指示</span><span class="sxs-lookup"><span data-stu-id="8af0f-105">Instructions</span></span>


<span data-ttu-id="8af0f-106">若要避免在回應事件時啟動自動播放，請新增下列 **REG \_ SZ** 值（如本範例所示）。</span><span class="sxs-lookup"><span data-stu-id="8af0f-106">To prevent AutoPlay from launching in response to an event, add the following **REG\_SZ** value, as shown in this example.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="8af0f-107">值是)  (CLSID 的類別識別碼，可在執行中的物件資料表 (的 ROT) 得知產生事件的元件。</span><span class="sxs-lookup"><span data-stu-id="8af0f-107">The value is the class identifier (CLSID) that the component that is generating the event is known by in the running object table (ROT).</span></span> <span data-ttu-id="8af0f-108">值沒有任何資料。</span><span class="sxs-lookup"><span data-stu-id="8af0f-108">The value has no data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8af0f-109">在此機碼下，Clsid 不會以大括弧括住 ( {} ) 。</span><span class="sxs-lookup"><span data-stu-id="8af0f-109">Under this key, the CLSIDs are not enclosed in braces ( {} ).</span></span>

 

 

 



