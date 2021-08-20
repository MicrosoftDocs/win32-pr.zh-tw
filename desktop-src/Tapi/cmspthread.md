---
description: CMSPThread 類別會實 Msp 背景工作執行緒。
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992efdc7f46772ee7766ba38ebab4cf3a9adc502e7c4001eb91779d03c677d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946674"
---
# <a name="cmspthread"></a>CMSPThread

**CMSPThread** 類別會執行 MSP 的背景工作執行緒。 基類使用此背景工作執行緒有許多用途。 系統會提供一般和輕量的工作專案機制，讓衍生的 MSP 可將此執行緒用於其本身的同步或非同步工作專案，不論它們可能是什麼。 此執行緒也會提取訊息，並支援處理 Apc (雖然基類) 不會使用 Apc。

當有多個類似的位址存在時 (也就是，當相同 DLL 的相同 MSP 實) 具現化時，執行緒類別會自動針對所有位址使用單一執行緒，以確保可調整性。 執行緒類別的介面，就是 MSP 實可以將 thread 類別視為私用執行緒，而不需要在意可能共用的其他位址。

定義于 MSPthrd 中。

 

 



