---
title: SetInfo 方法
description: IADs SetInfo 方法會將這個 Active Directory 物件之屬性的目前值，從屬性快取儲存到基礎目錄存放區。 這類似于將緩衝區排清到磁片。
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- 使用 SetInfo ADSI
- 屬性 ADSI，儲存屬性的目前值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5965a46e5accd2a00adc006fe37511de13ff0df3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300052"
---
# <a name="the-setinfo-method"></a><span data-ttu-id="05449-106">SetInfo 方法</span><span class="sxs-lookup"><span data-stu-id="05449-106">The SetInfo Method</span></span>

<span data-ttu-id="05449-107">[**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)方法會將這個 Active Directory 物件之屬性的目前值，從屬性快取儲存到基礎目錄存放區。</span><span class="sxs-lookup"><span data-stu-id="05449-107">The [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method saves the current values for the properties for this Active Directory object from the property cache to the underlying directory store.</span></span> <span data-ttu-id="05449-108">這類似于將緩衝區排清到磁片。</span><span class="sxs-lookup"><span data-stu-id="05449-108">This is analogous to flushing a buffer out to disk.</span></span>

<span data-ttu-id="05449-109">[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 會更新目錄中已存在的物件，或為新建立的物件建立新的目錄專案。</span><span class="sxs-lookup"><span data-stu-id="05449-109">[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) updates objects that already exist in the directory, or create a new directory entry for newly created objects.</span></span>

<span data-ttu-id="05449-110">在 [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 呼叫時，如果已使用 [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) 控制項程式碼（例如 ADS 屬性更新或 ads 屬性）來撰寫任何屬性快取值，則 \_ 會將 \_ \_ \_ 適當的要求傳遞至基礎目錄服務。</span><span class="sxs-lookup"><span data-stu-id="05449-110">At the time of the [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) call, if any property cache values have been written with a [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) control code, such as ADS\_PROPERTY\_UPDATE or ADS\_PROPERTY\_CLEAR, then the appropriate requests are passed on to the underlying directory service.</span></span>

 

 




