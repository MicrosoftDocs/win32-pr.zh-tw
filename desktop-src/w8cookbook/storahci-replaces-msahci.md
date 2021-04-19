---
title: StorAHCI 取代 MSAHCI
description: StorAHCI 取代 MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "106967292"
---
# <a name="storahci-replaces-msahci"></a>StorAHCI 取代 MSAHCI

## <a name="platforms"></a>平台

**用戶端** – Windows 8  
**伺服器** – Windows Server 2012  


## <a name="description"></a>Description

StorAHCI，Storport 微型功能支援 Windows 中的序列 advanced 技術附件 (SATA) advanced host controller interface (AHCI) 控制器，並取代 MSAHCI （ATAport 的微型埠）。

## <a name="manifestation"></a>表現

功能或效能都不會有任何變更;此驅動程式支援 MSAHCI 支援的所有相同裝置。

這項變更對使用者而言是透明的。

## <a name="mitigation"></a>降低

更新依賴 ATAport 系結的任何公用程式和腳本。 請勿依賴磁片磁碟機名稱。 改為使用標準磁片偵測。

 

 




