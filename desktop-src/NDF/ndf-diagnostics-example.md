---
title: NDF 診斷範例
description: 下列範例顯示如何啟動 NDF 使用者介面，以及診斷網站 HTTP//www.microsoft.com 的連線。
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fca4d54519988c3182b50a7c304f9c76a86392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021308"
---
# <a name="ndf-diagnostics-example"></a><span data-ttu-id="98e27-103">NDF 診斷範例</span><span class="sxs-lookup"><span data-stu-id="98e27-103">NDF Diagnostics Example</span></span>

<span data-ttu-id="98e27-104">下列範例顯示如何啟動 NDF 使用者介面，並診斷網站的連線能力 https://www.microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="98e27-104">The following example shows how to launch the NDF user interface and diagnose connectivity to the website https://www.microsoft.com.</span></span>


```C++
#include "ndfapi.h"

NDFHANDLE hNDF;
HRESULT hr = NdfCreateWebIncident (
                    L"https://www.microsoft.com",
                    &hNDF);

if(SUCCEEDED(hr))
{
    NdfExecuteDiagnosis(hNDF, NULL); // launches the NDF UI
                                     // the UI is not modal to the original window
    NdfCloseIncident(hNDF);
}
```



<span data-ttu-id="98e27-105">NDF UI 可以啟動為強制回應視窗。</span><span class="sxs-lookup"><span data-stu-id="98e27-105">The NDF UI can be launched as a modal window.</span></span> <span data-ttu-id="98e27-106">若要這樣做，請將 [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) 的第二個參數從 **Null** 變更為父視窗 (HWND) 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="98e27-106">To do so, change the second parameter of [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) from **NULL** to the handle (HWND) of the parent window.</span></span>

<span data-ttu-id="98e27-107">您可以修改此範例以診斷網路的其他區域。</span><span class="sxs-lookup"><span data-stu-id="98e27-107">This example can be modified to diagnose other areas of networking.</span></span> <span data-ttu-id="98e27-108">若要這樣做，請將 [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) 呼叫取代為另一個事件建立功能，例如 [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) 或 [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)。</span><span class="sxs-lookup"><span data-stu-id="98e27-108">To do so, replace the [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) call with one of the other incident creation functions, such as [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) or [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).</span></span>

## <a name="related-topics"></a><span data-ttu-id="98e27-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="98e27-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98e27-110">**NdfCloseIncident**</span><span class="sxs-lookup"><span data-stu-id="98e27-110">**NdfCloseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[<span data-ttu-id="98e27-111">**NdfCreateWebIncident**</span><span class="sxs-lookup"><span data-stu-id="98e27-111">**NdfCreateWebIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[<span data-ttu-id="98e27-112">**NdfExecuteDiagnosis**</span><span class="sxs-lookup"><span data-stu-id="98e27-112">**NdfExecuteDiagnosis**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




