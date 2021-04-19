---
description: Ws2 \_32.dll (和分層式通訊協定) 會針對 WSPStartup 的每個調用呼叫 WSPCleanup 一次。
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: 清除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc294183f964d00ae9ebb1d74b90b346c2ce8fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997488"
---
# <a name="cleanup"></a>清除

Ws2 \_32.dll (和分層式通訊協定) 會針對 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)的每個調用呼叫 [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))一次。 在每次叫用時， **WSPCleanup** 應該遞減每個進程的參考計數器，而當計數器到達零時，服務提供者必須準備要從記憶體卸載。 第一個商務順序是在設定為正常關閉的通訊端上完成傳送任何未傳送的資料。 之後，提供者所持有的任何和所有資源都將被釋放。 服務提供者必須停留在可透過呼叫 **WSPStartup** 立即重新初始化的狀態。

 

 
