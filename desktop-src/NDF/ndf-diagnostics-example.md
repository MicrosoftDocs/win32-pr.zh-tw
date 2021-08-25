---
title: NDF 診斷範例
description: 下列範例顯示如何啟動 NDF 使用者介面，以及診斷網站 HTTP//www.microsoft.com 的連線。
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa1971da12b7d707dc74b34497dff630ee8fdd8f93d5737ae3757bdde129fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802368"
---
# <a name="ndf-diagnostics-example"></a>NDF 診斷範例

下列範例顯示如何啟動 NDF 使用者介面，並診斷網站的連線能力 https://www.microsoft.com 。


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



NDF UI 可以啟動為強制回應視窗。 若要這樣做，請將 [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) 的第二個參數從 **Null** 變更為父視窗 (HWND) 的控制碼。

您可以修改此範例以診斷網路的其他區域。 若要這樣做，請將 [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) 呼叫取代為另一個事件建立功能，例如 [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) 或 [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




