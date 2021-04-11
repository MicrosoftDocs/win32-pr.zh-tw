---
description: 某些物件一次只支援一個控制碼。
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: 控制碼限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194727"
---
# <a name="handle-limitations"></a>控制碼限制

某些物件一次只支援一個控制碼。 當應用程式建立物件時，系統會提供控制碼，並在應用程式終結物件時使控制碼失效。 其他物件支援單一物件的多個控制碼。 當物件的最後控制碼關閉之後，作業系統會自動從記憶體中移除該物件。

系統中開啟的控制碼總數只受限於可用的記憶體數量。 某些物件類型支援每個會話或每個進程的控制碼數目有限。

 

 



