---
description: " (Api) 使用 StylusInput 應用程式設計介面時的錯誤處理總覽。"
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: StylusInput API 的錯誤處理考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fa582a8dbf531588f6d3d0c142c4ec7b40a058
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943476"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a>StylusInput API 的錯誤處理考慮

由 [**RealTimeStylus**](realtimestylus-class.md) 物件攔截外掛程式擲回的未處理例外狀況。 當外掛程式擲回例外狀況時，就會中斷正常的資料流程。 **RealTimeStylus** 物件：

1.  在 managed 程式碼) 中建立 [ErrorData](/previous-versions/ms575221(v=vs.100)) 物件 (。
2.  在 managed 程式碼中呼叫 (的 [**錯誤**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) 方法，可能是擲回例外狀況之外掛程式的 [StylusInput. IStylusSyncPlugin](/previous-versions/ms824754(v=msdn.10)) 或 [StylusInput. IStylusAsyncPlugin](/previous-versions/ms824771(v=msdn.10)) 方法) 。
3.  呼叫該集合中其餘外掛程式的 [**錯誤**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) 方法。
4.  如果擲回例外狀況的外掛程式是同步外掛程式，則會將 managed 程式碼) 中 (的 [ErrorData](/previous-versions/ms575221(v=vs.100)) 物件新增至輸出佇列。
5.  [**RealTimeStylus**](realtimestylus-class.md)物件會繼續正常處理原始資料。

如果外掛程式從其 [**錯誤**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) 方法擲回例外狀況，則 [**RealTimeStylus**](realtimestylus-class.md) 物件會捕捉例外狀況，但不會產生新的 [ErrorData](/previous-versions/ms575221(v=vs.100)) 物件。 如需如何將 ErrorData 排入佇列的詳細資訊，請參閱 [外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)。

當其中一個外掛程式擲回例外狀況時， [**RealTimeStylus**](realtimestylus-class.md) 物件不會停止處理 tablet 畫筆資料流程中的資料。 視您的設計而定，某些外掛程式可能需要訂閱 [ErrorData](/previous-versions/ms575221(v=vs.100)) 通知，並在發生例外狀況時修改其行為。

 

 
