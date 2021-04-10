---
title: 擴充錯誤資訊的需求
description: 針對 RPC 問題進行疑難排解的主要難題是將 RPC 錯誤碼對應至根本問題。
ms.assetid: aef3bcd6-ecaa-4639-b765-da90db6ddf82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d82fbbcaf0fac427b2bf64fbacbf1e85aeb4d06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021186"
---
# <a name="the-need-for-extended-error-information"></a>擴充錯誤資訊的需求

針對 RPC 問題進行疑難排解的主要難題是將 RPC 錯誤碼對應至根本問題。 設定錯誤或網路問題可能會導致一或多個工作站接收 RPC \_ \_ \* 的錯誤，但該工作站只能顯示錯誤、釋義，或將它儲存至某些記錄檔。 無論使用哪種方法，針對問題進行疑難排解的人員都必須 deprived 基本資訊：

-   發生錯誤的位置。 可能發生在本機電腦上、由本機電腦呼叫的遠端電腦，或是由另一部遠端電腦呼叫的遠端電腦上。
-   造成問題的原始錯誤碼。 為了符合憑證標準，MS RPC 會將錯誤碼對應至 RPC \_ S \_ \* 代碼。 \_ \_ \* 不過，RPC S 的代碼太過一般，而且提供了一些實用的疑難排解資訊。
-   與發生問題相關的任何內容資訊。 在非 RPC 錯誤中，偵錯工具可以停止進程並檢查發生錯誤的內容。 RPC 錯誤通常是由遠端進程或電腦所產生，會在傳回錯誤之後繼續處理，並覆寫與錯誤有關的任何內容。

 

 




