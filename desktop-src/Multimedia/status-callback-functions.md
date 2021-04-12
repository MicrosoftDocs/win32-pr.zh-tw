---
title: 狀態回呼函數
description: 狀態回呼函數
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- AVICap 回呼函式，狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b4b4bf4cad5f689f1e146986f9d1b55b00f1aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372190"
---
# <a name="status-callback-functions"></a>狀態回呼函數

捕捉視窗可以將訊息傳送至狀態回呼函式，同時將影片捕獲到磁片或在其他冗長的作業期間，以通知您的應用程式作業進度。 狀態資訊包括可供顯示的訊息識別碼和格式化的文字字串。 您的應用程式可以使用訊息識別碼來篩選通知，以及限制要向使用者顯示的訊息。 在捕獲作業期間，傳送至回呼函式的第一個訊息一律為 ID \_ 端點 \_ 開始，而最後一律為識別碼端點 \_ \_ 。 訊息識別碼為零表示正在啟動新的作業，而且回呼函式應清除目前的狀態。

 

 




