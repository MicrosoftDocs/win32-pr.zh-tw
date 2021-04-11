---
description: IP 協助程式提供本機電腦網路設定的相關資訊。
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: 正在抓取網路設定的相關資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945141"
---
# <a name="retrieving-information-about-network-configuration"></a>正在抓取網路設定的相關資訊

IP 協助程式提供本機電腦網路設定的相關資訊。 若要取出一般設定資訊，請使用 [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) 函數。 此函數會傳回特定介面卡或介面特有的資訊。 例如， **GetNetworkParams** 會傳回本機電腦所使用的 DNS 伺服器清單。

-   如需涉及 [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) 的程式碼範例，請參閱 [使用 GetNetworkParams 抓取資訊](retrieving-information-using-getnetworkparams.md)。

 

 



