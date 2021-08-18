---
title: 使用 DVC 通道寫入資料
description: 使用動態虛擬通道來寫入通道資料 (DVC) 是遠端桌面工作階段主機 (RD 工作階段主機) 伺服器和用戶端的對稱。
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e3f73b8e7a3d7db8ac109e84c9c638845af441b58568156782710fdac0968a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058239"
---
# <a name="writing-data-by-using-a-dvc-channel"></a>使用 DVC 通道寫入資料

使用動態虛擬通道來寫入通道資料 (DVC) 是遠端桌面工作階段主機 (RD 工作階段主機) 伺服器和用戶端的對稱。 通道資料的寫入是由 [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)介面的 [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write)方法所執行。

下圖顯示 DVC 用戶端與伺服器 (DVC 外掛程式) 之間的資料封包傳送和接收。

![傳送和接收 dvc 用戶端與伺服器之間的資料封包](images/writedvcchannel.png)

 

 




