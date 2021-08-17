---
title: StorAHCI 取代 MSAHCI
description: StorAHCI 取代 MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6affffe41dd00c009ebb7bebf508dac1b63bec673c17783f594d22969822e542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932138"
---
# <a name="storahci-replaces-msahci"></a>StorAHCI 取代 MSAHCI

## <a name="platforms"></a>平台

**用戶端**– Windows 8  
**伺服器**– Windows Server 2012  


## <a name="description"></a>描述

StorAHCI （Storport 微型功能）支援 Windows 中的序列 advanced 技術附件 (SATA) advanced 主機控制器介面 (AHCI) 控制器，並取代 MSAHCI （ATAport 的微型埠）。

## <a name="manifestation"></a>表現

功能或效能都不會有任何變更;此驅動程式支援 MSAHCI 支援的所有相同裝置。

這項變更對使用者而言是透明的。

## <a name="mitigation"></a>降低

更新依賴 ATAport 系結的任何公用程式和腳本。 請勿依賴磁片磁碟機名稱。 改為使用標準磁片偵測。

 

 




