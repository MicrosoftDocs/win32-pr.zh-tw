---
title: 開發與網路中的部署
description: 大部分的開發人員都是在快速可靠的 LAN 上撰寫和測試軟體。
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ff9da31ecd80b9e0a699d9ec0eb450e885a423b9380b85e2015e9ef7c1af7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930618"
---
# <a name="development-vs-deployment-in-the-network"></a>開發與網路中的部署

大部分的開發人員都是在快速可靠的 LAN 上撰寫和測試軟體。 他們的用戶端和伺服器通常位於相同的網路區段。 在這種情況下，網路幾乎沒有回應，而且連線很少會遺失。 不過，當部署在客戶環境中時，用戶端和伺服器通常位於不同的網路區段，可能位於遠端，而且伺服器會與其他用戶端高度載入。 換句話說：無法假設網路回應性。

本文說明如何在本質上不可靠的網路和可能無法使用的伺服器所引進的不確定性情況下，建立穩固的用戶端/伺服器架構。

 

 




