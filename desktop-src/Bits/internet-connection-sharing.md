---
title: 網際網路連線共用
description: 如果連線共用設定為在網路上的電腦存取網際網路時撥號，則 BITS 可以強制使用 Microsoft 網際網路連線共用的家用網路撥號連線。
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8736144b74d12666c4a364ac5b644ead35f8d1ec28aa03926bb7b691c8218f3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588618"
---
# <a name="internet-connection-sharing"></a>網際網路連線共用

如果連線共用設定為在網路上的電腦存取網際網路時撥號，則 BITS 可以強制使用 Microsoft 網際網路連線共用的家用網路撥號連線。 若要防止強制撥號連線，請在共用網際網路連線的連線共用主機電腦上，停 **用 [每當網路上的電腦嘗試存取網際網路時建立撥號連線** ] 選項。

連線到連線共用主機電腦的電腦假設它們具有網路連線，因此 BITS 會嘗試傳輸檔案。 如果主機電腦上的撥號選項已停用，而且主機電腦沒有作用中的連線，則傳輸會失敗併發生暫時性錯誤。 BITS 會定期重試傳輸。

 

 




