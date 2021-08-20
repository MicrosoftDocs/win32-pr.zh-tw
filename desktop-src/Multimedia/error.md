---
title: 錯誤
description: 錯誤
ms.assetid: d3a087e4-7b57-4070-aa82-3673bc18a54f
keywords:
- AVICap 回呼函式，錯誤通知訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d257ee6fc85709fdb5935e01025338753c5af60926234aa458e773a84f690e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988485"
---
# <a name="error"></a>錯誤

「捕獲視窗」會使用錯誤通知訊息，通知您應用程式的 AVICap 錯誤，例如磁碟空間不足、嘗試寫入唯讀檔案、無法存取硬體或卸載過多的畫面格。 錯誤通知的內容包含可供顯示的訊息識別碼和格式化的文字字串。 您的應用程式可以使用訊息識別碼來篩選通知，以及限制要向使用者顯示的訊息。 訊息識別碼為零表示正在啟動新的作業，而且回呼函式應清除任何顯示的錯誤訊息。

 

 




