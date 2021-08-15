---
title: 磁帶初始化
description: 應用程式必須使用 CreateFile 函式來建立磁帶裝置的控制碼。 此控制碼用於裝置中磁帶的後續作業。
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- 磁帶初始化備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aeba729feb9351b5af15d26f6366b455c5ce74a9cc6300c9ab8d25047b4760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835401"
---
# <a name="tape-initialization"></a>磁帶初始化

應用程式必須使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來建立磁帶裝置的控制碼。 此控制碼用於裝置中磁帶的後續作業。

在應用程式寫入磁帶之前，必須根據應用程式的需求以及使用的磁帶機功能來格式化磁帶。 [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition)函式會重新格式化磁帶，在其上建立指定大小的指定磁碟分割數目。

[**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape)函數會準備要存取或移除的磁帶。 此函數可以載入、卸載、鎖定或解除鎖定磁帶。 此函式也可以將磁帶移至磁帶的結尾，再回到開頭，以將磁帶張力。

若要抓取和設定磁帶和磁帶機的相關資訊，應用程式會使用 [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)、 [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)和 [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) 功能。

[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) 會取出描述磁帶或磁帶機的資訊。 磁帶資訊包含磁帶的類型、密度和區塊大小;磁帶上的磁碟分割數目;剩餘的磁帶數量;依此類推。 磁帶機資訊包括磁片磁碟機的預設區塊大小、最大分割區計數，以及支援的功能。

[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) 會設定磁帶區塊大小或設定磁帶機旗標，以指出磁片磁碟機是否支援硬體錯誤修正、資料壓縮、資料填補或三種組合。

[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) 指出磁帶機是否已準備好處理磁帶命令。

 

 