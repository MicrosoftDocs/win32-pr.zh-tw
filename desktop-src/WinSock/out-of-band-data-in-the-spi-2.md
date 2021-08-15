---
description: 支援資料流程樣式通訊端之頻外資料 (OOB) 抽象層的服務提供者必須遵守本節中的語法。
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: SPI 中的頻外資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858e2845e9fbe198dc7af7a70edfad8a4ac429f8f1abe84289b87a779f6e478b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741047"
---
# <a name="out-of-band-data-in-the-spi"></a>SPI 中的頻外資料

支援資料流程樣式通訊端之頻外資料 (OOB) 抽象層的服務提供者必須遵守本節中的語法。 我們將以與通訊協定無關的方式來描述 OOB 資料處理。 請參閱 [Winsock 附件](winsock-annexes.md) ，以取得使用 tcp/ip 服務提供者中的緊急資料所執行的 OOB 資料討論。 在下列情況下，使用 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) 也會套用至 [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))。

 

 
