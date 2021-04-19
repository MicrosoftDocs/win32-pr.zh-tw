---
title: attribute_onchange
description: 當外觀屬性變更值時，就會發生事件處理常式可以處理的事件。 事件處理常式的名稱是屬性的名稱，後面接著底線和 \ 0034; onchange \ 0034;，例如 \ 0034; value \_ onchange \ 0034;。
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange Windows Media Player
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000426"
---
# <a name="attribute_onchange"></a><span data-ttu-id="6a339-105">屬性 \_ onchange</span><span class="sxs-lookup"><span data-stu-id="6a339-105">attribute\_onchange</span></span>

<span data-ttu-id="6a339-106">當外觀屬性變更值時，就會發生事件處理常式可以處理的事件。</span><span class="sxs-lookup"><span data-stu-id="6a339-106">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="6a339-107">事件處理常式的名稱是屬性的名稱，後面接著底線和 "onchange"，例如「值 \_ onchange」。</span><span class="sxs-lookup"><span data-stu-id="6a339-107">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span>

``` syntax
        attribute_onchange
```

## <a name="examples"></a><span data-ttu-id="6a339-108">範例</span><span class="sxs-lookup"><span data-stu-id="6a339-108">Examples</span></span>


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a><span data-ttu-id="6a339-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a339-109">Requirements</span></span>



| <span data-ttu-id="6a339-110">需求</span><span class="sxs-lookup"><span data-stu-id="6a339-110">Requirement</span></span> | <span data-ttu-id="6a339-111">值</span><span class="sxs-lookup"><span data-stu-id="6a339-111">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="6a339-112">版本</span><span class="sxs-lookup"><span data-stu-id="6a339-112">Version</span></span><br/> | <span data-ttu-id="6a339-113">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="6a339-113">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a339-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a339-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a339-115">**環境事件處理常式**</span><span class="sxs-lookup"><span data-stu-id="6a339-115">**Ambient Event Handlers**</span></span>](ambient-event-handlers.md)
</dt> </dl>

 

 





