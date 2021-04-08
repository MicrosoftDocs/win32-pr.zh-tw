---
title: 管理控制碼
description: 路由表管理員會維護它所維護之所有資訊的參考計數。
ms.assetid: bcd02881-b021-414f-8a40-14baac5baac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24653dd98db9b0427e5a3bee3f2f6613a68ce41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932308"
---
# <a name="managing-handles"></a>管理控制碼

路由表管理員會維護它所維護之所有資訊的參考計數。 這可防止路由表管理員將任何已釋放記憶體的控制碼傳回給用戶端。 每次將控制碼傳回給呼叫端時，會以明確控制碼或資訊結構的一部分（例如 [**RTM \_ DEST \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info)）傳回給呼叫者，對應至控制碼之物件的參考計數會遞增。 釋放控制碼或資訊結構時，會減少適當的參考計數。 如果參考計數變成零，則會釋放物件。

[**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo)、 [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo)、 [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)和 [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)函數會傳回信息結構。 這些函式分別對應至 [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)、 [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)、 [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) 和 [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) 函數。

> [!Note]  
> [**RtmReleaseChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests)函式應該用來釋放呼叫 [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests)所傳回的控制碼。 請勿針對已變更的目的結構使用 [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) 。

 

如果用戶端必須在釋放其餘部分時，將特定的控制碼保留在資訊結構中，則用戶端可以使用該控制碼呼叫 [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) ，然後再釋放資訊結構。 然後，您可以呼叫 [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo)、 [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo)、 [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) 和 [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) 函式來釋放控制碼。

 

 




