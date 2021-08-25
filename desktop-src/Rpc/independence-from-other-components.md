---
title: 與其他元件的獨立性
description: 即使傳遞的鏈無法辨識擴充的錯誤資料，或無法利用它，擴充的錯誤資料也很有用。 這種情況的建議方法是在本節結尾處提供。
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- 與其他元件的獨立性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8174ffa0469550d3a7b274fb28f2f30dd807314e6bd596b75469f717f5924a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020448"
---
# <a name="independence-from-other-components"></a>與其他元件的獨立性

即使傳遞的鏈無法辨識擴充的錯誤資料，或無法利用它，擴充的錯誤資料也很有用。 這種情況的建議方法是在本節結尾處提供。

當使用 RPC 的應用程式或伺服器利用擴充的錯誤資訊時，擴充的錯誤資料最有用。 在調查 RPC \_ S \_ \* 錯誤碼以及相關的伺服器或應用程式未提供延伸的錯誤資料時，請考慮下列方法：

-   進行探查。

    在取得探查時重現案例。 網路的探查將包含擴充的錯誤資料。

-   從偵錯工具檢查它。

    如果接受問題的探查無法運作，因為呼叫是本機的，或由於錯誤源自本機，請將偵錯工具附加至傳回錯誤的進程，並在 RPC 呼叫產生錯誤之後立即放置中斷點。 RPC 通常會藉由擲回例外狀況來指出錯誤，因此，如果您要尋找錯誤 1825 (RPC \_ S \_ SEC \_ PKG \_ error) ，請啟用例外狀況1825，並在偵錯工具中斷該例外狀況時，檢查執行緒的延伸錯誤資訊。

 

 




