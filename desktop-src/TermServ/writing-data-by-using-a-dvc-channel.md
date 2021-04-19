---
title: 使用 DVC 通道寫入資料
description: 使用動態虛擬通道來寫入通道資料 (DVC) 是遠端桌面工作階段主機 (RD 工作階段主機) 伺服器和用戶端的對稱。
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd6f26e926958ceba5418a72849b75a66b11d2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996352"
---
# <a name="writing-data-by-using-a-dvc-channel"></a><span data-ttu-id="55913-103">使用 DVC 通道寫入資料</span><span class="sxs-lookup"><span data-stu-id="55913-103">Writing Data by Using a DVC Channel</span></span>

<span data-ttu-id="55913-104">使用動態虛擬通道來寫入通道資料 (DVC) 是遠端桌面工作階段主機 (RD 工作階段主機) 伺服器和用戶端的對稱。</span><span class="sxs-lookup"><span data-stu-id="55913-104">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span> <span data-ttu-id="55913-105">通道資料的寫入是由 [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)介面的 [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write)方法所執行。</span><span class="sxs-lookup"><span data-stu-id="55913-105">The writing of channel data is implemented by the [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) method of the [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) interface.</span></span>

<span data-ttu-id="55913-106">下圖顯示 DVC 用戶端與伺服器 (DVC 外掛程式) 之間的資料封包傳送和接收。</span><span class="sxs-lookup"><span data-stu-id="55913-106">The following illustration shows the sending and receiving of the data packet between the DVC client and server (DVC plug-in).</span></span>

![傳送和接收 dvc 用戶端與伺服器之間的資料封包](images/writedvcchannel.png)

 

 




