---
description: WSPConnect 會建立預設的目的地位址，以啟用通訊端搭配後續的傳送 (WSPSend) 並接收 (WSPRecv) 作業。
ms.assetid: efd57cb1-9736-4527-8e20-ab9304e3a8f6
title: 連接至預設對等
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22ca4aff0cdc8560459dd2571d79a71a85fcc71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973461"
---
# <a name="connecting-to-a-default-peer"></a>連接至預設對等

針對系結至無連接通訊協定的通訊端， [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) 所執行的作業只是要建立預設的目的地位址，以便將通訊端用於後續的連接導向傳送和接收作業， ([**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) 和 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))) 。 從指定的目的地位址以外的位址接收的任何資料包都會被捨棄。

 

 
