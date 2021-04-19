---
description: 下列定義提供一組可能對衍生類別有用的資料流程狀態，雖然不需要使用它們。 衍生類別只要定義其他值，就可以輕易地延伸一組可用的狀態。
ms.assetid: 2c719828-904f-4469-ab3b-a331f009b9c3
title: CMSPStream 型別定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5395227b2c95bddb6b4b7ef7df391b610bf20bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979829"
---
# <a name="cmspstream-type-definitions"></a><span data-ttu-id="5acc5-104">CMSPStream 型別定義</span><span class="sxs-lookup"><span data-stu-id="5acc5-104">CMSPStream Type Definitions</span></span>

<span data-ttu-id="5acc5-105">下列定義提供一組可能對衍生類別有用的資料流程狀態，雖然不需要使用它們。</span><span class="sxs-lookup"><span data-stu-id="5acc5-105">The following definitions provide a set of stream states that may be useful to the derived class, although their use is not required.</span></span> <span data-ttu-id="5acc5-106">衍生類別只要定義其他值，就可以輕易地延伸一組可用的狀態。</span><span class="sxs-lookup"><span data-stu-id="5acc5-106">Derived classes can conveniently extend the set of available states simply by defining additional values.</span></span>

``` syntax
#define STRM_INITIAL            0x00000000
#define STRM_TERMINALSELECTED   0x00000001
#define STRM_CONFIGURED         0x00000002
#define STRM_RUNNING            0x00000004
#define STRM_PAUSED             0x00000008
#define STRM_STOPPED            0x00000010
```

## <a name="related-topics"></a><span data-ttu-id="5acc5-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="5acc5-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5acc5-108">**CMSPStream**</span><span class="sxs-lookup"><span data-stu-id="5acc5-108">**CMSPStream**</span></span>](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



