---
title: 變更目前的位置
description: 變更目前的位置
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK 命令訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235dc2639d7d9fc01f94aff700ae9e0ebf1dcbe2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375336"
---
# <a name="changing-the-current-position"></a>變更目前的位置

若要變更裝置元素中的目前位置，請使用 [**mci \_ 搜尋**](mci-seek.md) 命令訊息以及 mci \_ 來旗標和 [**mci \_ 搜尋 \_ PARMS**](mci-seek-parms.md) 結構。 如果您使用 **dwTo** 成員指定使用 MCI 搜尋的搜尋位置 \_ ，您應該查詢時間格式並設定它（如有必要）。

除了指定具有 **dwTo** 成員的位置之外，您還可以指定 \_ 要啟動的 mci 搜尋， \_ \_ 或針對 mciSendCommand 函式的 dwParam1 參數指定「mci」 \_ \_ 以 \_ 結束旗標，以尋找設備元素的開始和結束位置。  [](/previous-versions//dd757160(v=vs.85)) 如果您使用其中一個旗標，請不要指定要旗標的 MCI \_ 。

 

 