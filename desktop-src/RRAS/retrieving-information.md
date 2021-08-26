---
title: 擷取資訊
description: RTMv2 可讓用戶端使用 RtmGetEntityInfo、RtmGetDestInfo、RtmGetRouteInfo 和 RtmGetNextHopInfo 函式，來取得指定控制碼所參考的資訊。
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51958fccc8a07e8846705945d9210f4259dfd89b1e3cefccd65d57dd0f033757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028018"
---
# <a name="retrieving-information"></a>擷取資訊

RTMv2 可讓用戶端使用 [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo)、 [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo)、 [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)和 [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) 函式，來取得指定控制碼所參考的資訊。

這些函式呼叫具有對應的函數 ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)、 [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)、 [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo)、 [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) 來釋出與路由表管理員所傳回之資訊結構相關聯的控制碼。

> [!Note]  
> 用戶端的資訊僅適用于目前的實例和位址系列。

 

如需示範如何使用這些函式的範例程式碼，請參閱 [搜尋最佳路由](search-for-the-best-route.md)。

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a>使用 RtmGetExactMatchRoute 和 RtmGetExactMatchDestination

用戶端會使用 [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) 和 [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) 函數來尋找特定的路由或目的地。 這些函式會藉由執行用戶端的比較工作來節省時間。

例如，當 RIP 更新路由時，RIP 必須保留舊的度量資訊。 RIP 會搜尋路由及其資訊。 然後，RIP 可以複製資訊並更新路由。

## <a name="using-rtmgetmostspecificdestination"></a>使用 RtmGetMostSpecificDestination

[**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)函式可用來尋找最符合指定之網路首碼的目的地。

例如，多播群組管理員會使用此函數來執行反向路徑轉送 (RPF) 檢查單一位址。 函數也可以用來尋找指定遠端下一個躍點的本機下一個躍點。

如需示範如何使用這些函式的範例程式碼，請參閱 [使用前置詞樹狀目錄搜尋路由](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) ，並 [搜尋最佳路由](search-for-the-best-route.md)。

## <a name="using-rtmgetlessspecificdestination"></a>使用 RtmGetLessSpecificDestination

[**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination)函式是用來找出下一個最符合指定網路首碼的目的地。 您可以重複呼叫這個函式，以傳回下一次較不相符的相符項，直到沒有其他目的地相符為止。

呼叫 [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)之後，會呼叫這個函式。

如需說明如何使用這些函式的範例程式碼，請參閱 [使用前置詞樹狀目錄搜尋路由](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md)。

## <a name="using-rtmisbestroute"></a>使用 RtmIsBestRoute

[**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute)函式可讓用戶端快速找出特定路由是否為目的地的最佳路由。 例如，如果用戶端是最適合的路由，則可能需要儲存特定的路由。 因此，用戶端可以呼叫這個函式，而不是列舉所有路由並進行比較。

 

 




