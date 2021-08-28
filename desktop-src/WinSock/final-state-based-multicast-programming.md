---
description: 本節說明使用 IOCTLs 而不是通訊端選項的最終狀態式多播程式設計。 如需最終狀態式多播程式設計與以變更為基礎的多播程式設計有何不同的總覽，請參閱多播程式設計。
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: 以最終狀態為基礎的多播程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad31f0c840228e1fea729582f5e259ec92c4a04381752ed9ee50db2586b3b29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132511"
---
# <a name="final-state-based-multicast-programming"></a>以最終狀態為基礎的多播程式設計

本節說明使用 IOCTLs 而不是通訊端選項的最終狀態式多播程式設計。 如需最終狀態式多播程式設計與以變更為基礎的多播程式設計有何不同的總覽，請參閱 [多播程式設計](multicast-programming.md)。

下表描述用於 Windows 的多播程式設計 Windows 通訊端 IOCTLs。 

| IOCTL                       | 引數類型                                   |
|-----------------------------|-------------------------------------------------|
| SIOCSMSFILTER               | [**群組 \_篩選**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) 結構 |
| SIOCGMSFILTER               | [**群組 \_篩選**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) 結構 |
| SIO \_ 取得 \_ 多播 \_ 篩選 | [**ip \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) 結構   |
| SIO \_ 設定 \_ 多播 \_ 篩選器 | [**ip \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) 結構   |



 

請注意， **SIOCSMSFILTER** 和 **SIOCGMSFILTER** IOCTLS 可在 Windows Vista 和更新版本上取得。

使用這些 IOCTLs 進行多播程式設計時，在使用大型來源清單時有其效能優勢。 如需有關使用 SIO \_ 取得 \_ 多播 \_ 篩選器或 SIO 設定多播篩選器之參數和設定的詳細資訊 \_ \_ ，請 \_ 參閱 [**群組 \_ 篩選**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) 參考頁面。 如需有關使用 SIO \_ 取得 \_ 多播 \_ 篩選器或 SIO 設定多播篩選器之參數和設定的詳細資訊 \_ \_ ，請 \_ 參閱 [**ip \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) 參考頁面。

 

 



