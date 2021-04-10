---
title: 開發與網路中的部署
description: 大部分的開發人員都是在快速可靠的 LAN 上撰寫和測試軟體。
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021324"
---
# <a name="development-vs-deployment-in-the-network"></a>開發與網路中的部署

大部分的開發人員都是在快速可靠的 LAN 上撰寫和測試軟體。 他們的用戶端和伺服器通常位於相同的網路區段。 在這種情況下，網路幾乎沒有回應，而且連線很少會遺失。 不過，當部署在客戶環境中時，用戶端和伺服器通常位於不同的網路區段，可能位於遠端，而且伺服器會與其他用戶端高度載入。 換句話說：無法假設網路回應性。

本文說明如何在本質上不可靠的網路和可能無法使用的伺服器所引進的不確定性情況下，建立穩固的用戶端/伺服器架構。

 

 




