---
description: IP 協助程式提供資訊抓取功能，對於本機電腦的網路管理很有用。
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: 在網際網路通訊協定和網際網路控制訊息通訊協定上抓取資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936589"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a>在網際網路通訊協定和網際網路控制訊息通訊協定上抓取資訊

IP 協助程式提供資訊抓取功能，對於本機電腦的網路管理很有用。 下列函式會取得網際網路通訊協定 (IP) 的統計資料，以及 (ICMP) 的網際網路控制訊息通訊協定。 您也可以使用這些函數來設定 IP 的特定設定參數。

[**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics)函式會取得本機電腦目前的 IP 統計資料。 如需涉及 **GetIpStatistics** 的程式碼範例，請參閱 [使用 GetIpStatistics 抓取資訊](retrieving-information-using-getipstatistics.md)。

[**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics)函式會捕獲目前的 ICMP 統計資料。

使用 [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) 函數來啟用或停用 IP 轉送。 此功能也可讓您為 IP 資料包設定預設的存留時間 (TTL) 。 或者，您可以使用 [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) 函數來設定 TTL。

 

 



