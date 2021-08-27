---
description: IP 協助程式提供本機電腦網路設定的相關資訊。
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: 正在抓取網路設定的相關資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767bdf0ec8c316bc4998e50e06e6f1a88f92742adff88f11745fbbd80c0b26ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050318"
---
# <a name="retrieving-information-about-network-configuration"></a>正在抓取網路設定的相關資訊

IP 協助程式提供本機電腦網路設定的相關資訊。 若要取出一般設定資訊，請使用 [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) 函數。 此函數會傳回特定介面卡或介面特有的資訊。 例如， **GetNetworkParams** 會傳回本機電腦所使用的 DNS 伺服器清單。

-   如需涉及 [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) 的程式碼範例，請參閱 [使用 GetNetworkParams 抓取資訊](retrieving-information-using-getnetworkparams.md)。

 

 



