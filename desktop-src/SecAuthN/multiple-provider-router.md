---
description: 多個提供者路由器 (MPR) 處理 Windows 作業系統和已安裝網路提供者之間的通訊。 它可讓 Windows 向使用者呈現整合的網路。
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: 多個提供者路由器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788a6b5dc7ec2db1f75d4bdf7d04df4127e90670b7f798682423dac4567a6fe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786576"
---
# <a name="multiple-provider-router"></a>多個提供者路由器

[*多個提供者路由器*](../secgloss/m-gly.md) (MPR) 處理 Windows 作業系統和已安裝網路提供者之間的通訊。 它可讓 Windows 向使用者呈現整合的網路。

當 MPR 啟動時，它會檢查登錄，以判斷安裝在系統上的網路提供者，以及應迴圈的順序。 它會載入所有已註冊的網路提供者 Dll，並使用它們來處理使用者介面或其他應用程式所進行的後續 WNet 呼叫。

如需 WNet 函式的詳細資訊，請參閱[Windows 網路](../wnet/windows-networking-wnet-.md)功能。

 

 
