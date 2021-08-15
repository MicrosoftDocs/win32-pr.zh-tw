---
title: Yield 回呼函數
description: Yield 回呼函數
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- AVICap 回呼函式，yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e87a3c986378bee05078b8cab28a0647827a1102ef1809558a47dcd5123af2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369132"
---
# <a name="yield-callback-functions"></a>Yield 回呼函數

應用程式可以在串流處理期間使用 yield 回呼函數。  (yield 回呼函式通常是由呼叫 [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea)、 [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)和 [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage)的訊息迴圈所組成。 ) 捕捉視窗會針對每個已捕捉的影片框架呼叫 yield 回呼函式至少一次，但確切的速率取決於畫面播放速率和捕獲驅動程式和磁片的額外負荷。

 

 