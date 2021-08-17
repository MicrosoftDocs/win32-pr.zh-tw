---
description: 某些物件一次只支援一個控制碼。
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: 控制碼限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f194ed8464d2731c15e9b88ae62549f9fa090928c14cf7dc66e139944863b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764406"
---
# <a name="handle-limitations"></a>控制碼限制

某些物件一次只支援一個控制碼。 當應用程式建立物件時，系統會提供控制碼，並在應用程式終結物件時使控制碼失效。 其他物件支援單一物件的多個控制碼。 當物件的最後控制碼關閉之後，作業系統會自動從記憶體中移除該物件。

系統中開啟的控制碼總數只受限於可用的記憶體數量。 某些物件類型支援每個會話或每個進程的控制碼數目有限。

 

 



