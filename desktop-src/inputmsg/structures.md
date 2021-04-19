---
title: '結構 (指標輸入訊息和通知) '
description: 本節中的主題提供指標輸入訊息和通知結構的參考規格。
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106996118"
---
# <a name="pointer-input-messages-and-notifications-structures"></a>指標輸入訊息和通知結構

本節中的主題提供 [指標輸入訊息和通知](messages-and-notifications-portal.md) 結構的參考規格。

## <a name="in-this-section"></a>本節內容



| 主題                                                                            | 描述                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INPUT_TRANSFORM**](/previous-versions/windows/desktop/api)<br/>                           | 定義表示訊息取用者之轉換的矩陣。 您可以使用這個矩陣，將指標輸入資料從用戶端座標轉換成螢幕座標，而反向可用來將指標輸入資料從螢幕座標轉換成用戶端座標。 <br/>                                                                 |
| [**POINTER_INFO**](/previous-versions/windows/desktop/api)<br/>                          | 包含所有指標類型通用的基本指標資訊。 應用程式可以使用 [**GetPointerInfo**](/previous-versions/windows/desktop/api)、 [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api)、 [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) 和 [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) 函數來取得此資訊。 <br/> |
| [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)<br/>                 | 定義所有指標類型通用的基本畫筆資訊。 <br/>                                                                                                                                                                                                                                                                                                |
| [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)<br/>             | 定義所有指標類型通用的基本觸控資訊。<br/>                                                                                                                                                                                                                                                                                               |
| [**TOUCHPREDICTIONPARAMETERS**](/previous-versions/windows/desktop/api)<br/> | 包含可用來預測觸控目標的硬體輸入詳細資料，並在處理包含距離和速度資料的觸控和手勢輸入時協助補償硬體延遲。<br/>                                                                                                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[指標輸入訊息參考](wmpointer-reference.md)
</dt> </dl>

 

 





