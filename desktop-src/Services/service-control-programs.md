---
description: 服務控制程式會啟動並控制服務。
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: 服務控制程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb11e8224a23edcebd0688039502c5bc38da929d47cba470e6f397f4430e444f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889041"
---
# <a name="service-control-programs"></a>服務控制程式

服務控制程式會啟動並控制服務。 其會執行下列動作：

-   啟動服務或驅動程式服務（如果啟動類型是服務 \_ 需求 \_ 開始）。
-   將控制要求傳送至執行中的服務。
-   查詢正在執行之服務的目前狀態。

這些動作需要服務物件的開啟控制碼。 若要取得控制碼，服務控制程式必須：

1.  您可以使用 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) 函式來取得指定電腦上之 SCM 資料庫的控制碼。
2.  使用 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) 或 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函數來取得服務物件的控制碼。

如需詳細資訊，請參閱下列主題：

-   [服務啟動](service-startup.md)
-   [服務控制要求](service-control-requests.md)
-   [使用 SC 控制服務](controlling-a-service-using-sc.md)

 

 



