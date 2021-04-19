---
description: CAudioRenderTerminal 終端機衍生自 CSingleFilterTerminal，並使用 DirectShow waveout 篩選器來為 wave 裝置實行靜態音訊轉譯終端機。 大部分的 Msp 都不需要覆寫此終端機的執行。
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: CAudioRenderTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9915ef03a210f4ca440cb7a7b66448228b41df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984595"
---
# <a name="caudiorenderterminal"></a><span data-ttu-id="028e5-104">CAudioRenderTerminal</span><span class="sxs-lookup"><span data-stu-id="028e5-104">CAudioRenderTerminal</span></span>

<span data-ttu-id="028e5-105">**CAudioRenderTerminal** 終端機衍生自 [CSingleFilterTerminal](csinglefilterterminal.md) ，並使用 DirectShow waveout 篩選器來為 wave 裝置實行靜態音訊轉譯終端機。</span><span class="sxs-lookup"><span data-stu-id="028e5-105">The **CAudioRenderTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio render terminal for wave devices using the DirectShow waveout filter.</span></span> <span data-ttu-id="028e5-106">大部分的 Msp 都不需要覆寫此終端機的執行。</span><span class="sxs-lookup"><span data-stu-id="028e5-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="028e5-107">定義于 MSPtrmar 中。</span><span class="sxs-lookup"><span data-stu-id="028e5-107">Defined in MSPtrmar.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="028e5-108">備註</span><span class="sxs-lookup"><span data-stu-id="028e5-108">Remarks</span></span>

<span data-ttu-id="028e5-109">**CAudioRenderTerminal** 的 [**put \_ 餘額**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance)和 [**取得 \_ 餘額**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance)方法不會實作為，並會傳回電子 \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="028e5-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioRenderTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



