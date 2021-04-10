---
description: 手機裝置上的燈可能會以各種不同的光源模式亮起。
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: 燈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027278"
---
# <a name="lamps"></a><span data-ttu-id="6ddb9-103">燈</span><span class="sxs-lookup"><span data-stu-id="6ddb9-103">Lamps</span></span>

<span data-ttu-id="6ddb9-104">手機裝置上的燈可能會以各種不同的光源模式亮起。</span><span class="sxs-lookup"><span data-stu-id="6ddb9-104">The lamps on a phone device can be lit in a variety of different lighting modes.</span></span> <span data-ttu-id="6ddb9-105">與響鈴模式不同的是，燈泡模式在不同廠商的不同電話組間是更一致的。</span><span class="sxs-lookup"><span data-stu-id="6ddb9-105">Unlike ringing patterns, lamp modes are more uniform across phone sets of different vendors.</span></span> <span data-ttu-id="6ddb9-106">API 會定義一組常見的燈泡模式。</span><span class="sxs-lookup"><span data-stu-id="6ddb9-106">A common set of lamp modes is defined by the API.</span></span> <span data-ttu-id="6ddb9-107">以燈泡按鈕識別碼識別的燈泡，可在指定的燈泡模式中亮起。</span><span class="sxs-lookup"><span data-stu-id="6ddb9-107">A lamp identified by its lamp-button identifier can be lit in a given lamp mode.</span></span> <span data-ttu-id="6ddb9-108">燈泡也可以查詢其目前的燈泡模式。</span><span class="sxs-lookup"><span data-stu-id="6ddb9-108">A lamp can also be queried for its current lamp mode.</span></span>

<span data-ttu-id="6ddb9-109">用於燈的 TAPI 函式是 [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp)，它會在指定的燈光源模式中，以指定的開啟電話裝置燈燈燈，而 [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp)則會傳回指定燈的目前燈泡模式。</span><span class="sxs-lookup"><span data-stu-id="6ddb9-109">The TAPI functions used for lamps are [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), which lights a lamp on a specified open phone device in a given lamp lighting mode, and [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), which returns the current lamp mode of the specified lamp.</span></span>

<span data-ttu-id="6ddb9-110">當手機裝置的燈泡變更時，會將 [**電話 \_ 狀態**](phone-state.md) 消息傳送至應用程式，以通知應用程式狀態變更。</span><span class="sxs-lookup"><span data-stu-id="6ddb9-110">When a lamp of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="6ddb9-111">此訊息的參數提供了變更的指示。</span><span class="sxs-lookup"><span data-stu-id="6ddb9-111">Parameters to this message provide an indication of the change.</span></span>

 

 



