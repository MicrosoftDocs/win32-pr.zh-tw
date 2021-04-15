---
description: WSPCloseSocket 會釋出通訊端描述項，如此一來，相同進程的任何執行緒中的任何擱置中作業都將中止，且對它的任何進一步參考將會失敗。
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: 關閉通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d0c877767925f67e07427a77dc8ec8445f30c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511453"
---
# <a name="closing-sockets"></a>關閉通訊端

[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) 會釋出通訊端描述項，如此一來，相同進程的任何執行緒中的任何擱置中作業都將中止，且對它的任何進一步參考將會失敗。 請注意，應該針對共用通訊端使用參考計數，而且只有在這是基礎通訊端的最後一個參考時，如果與此通訊端相關聯的資訊被捨棄，提供的資訊不會受到要求 (也就是，因此 \_ DONTLINGER 不會設定) 。 在設定 DONTLINGER 的情況下 \_ ，會在釋放與通訊端相關聯的資訊之前，傳送任何排入佇列的資料（如果可能的話）。 如需詳細資訊，請參閱 **WSPCloseSocket** 。

針對 nonIFS 服務提供者，必須叫用 [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) ，將通訊端控制碼釋放回 Windows 通訊端 2 DLL。

 

 
