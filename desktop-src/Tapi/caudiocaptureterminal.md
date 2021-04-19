---
description: CAudioCaptureTerminal 終端機衍生自 CSingleFilterTerminal，並使用 DirectShow wavein 篩選器來為 wave 裝置實行靜態音訊捕獲終端機。 大部分的 Msp 都不需要覆寫此終端機的執行。
ms.assetid: 2860bf22-46ae-484a-a47b-0d7057b900a1
title: CAudioCaptureTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308af17ce7a7cb4d2d4cadebb43b06437ec14abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990329"
---
# <a name="caudiocaptureterminal"></a><span data-ttu-id="dc9b0-104">CAudioCaptureTerminal</span><span class="sxs-lookup"><span data-stu-id="dc9b0-104">CAudioCaptureTerminal</span></span>

<span data-ttu-id="dc9b0-105">**CAudioCaptureTerminal** 終端機衍生自 [CSingleFilterTerminal](csinglefilterterminal.md) ，並使用 DirectShow wavein 篩選器來為 wave 裝置實行靜態音訊捕獲終端機。</span><span class="sxs-lookup"><span data-stu-id="dc9b0-105">The **CAudioCaptureTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio capture terminal for wave devices using the DirectShow wavein filter.</span></span> <span data-ttu-id="dc9b0-106">大部分的 Msp 都不需要覆寫此終端機的執行。</span><span class="sxs-lookup"><span data-stu-id="dc9b0-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="dc9b0-107">定義于 MSPtmac 中。</span><span class="sxs-lookup"><span data-stu-id="dc9b0-107">Defined in MSPtmac.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc9b0-108">備註</span><span class="sxs-lookup"><span data-stu-id="dc9b0-108">Remarks</span></span>

<span data-ttu-id="dc9b0-109">**CAudioCaptureTerminal** 的 [**put \_ 餘額**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance)和 [**取得 \_ 餘額**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance)方法不會實作為，並會傳回電子 \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="dc9b0-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioCaptureTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



