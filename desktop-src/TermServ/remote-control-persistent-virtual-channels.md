---
title: 遠端控制持續性虛擬通道
description: 遠端控制連接或中斷連接至用戶端的會話時，不會關閉遠端控制持續性虛擬通道。 資料將繼續透過此通道傳送和接收。
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372575"
---
# <a name="remote-control-persistent-virtual-channels"></a>遠端控制持續性虛擬通道

在 Windows XP 上，DLL 可以將一或多個虛擬通道指定為 *遠端控制持續* 性。 遠端控制連接或中斷連接至用戶端的會話時，不會關閉遠端控制持續性虛擬通道。 資料將繼續透過此通道傳送和接收。 在此案例中，DLL 未指定為遠端控制持續性的虛擬通道將會關閉。

遠端控制持續性虛擬通道是在呼叫 **VirtualChannelInit** 期間指定。 如需有關這個的特定資訊，請參閱 [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) 的參考頁面。

 

 




