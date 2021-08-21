---
description: IP Helper 提供管理網路介面卡的功能。 指定電腦上的介面和介面卡之間有一對一的對應關係。 介面是一個 IP 層級的抽象概念，而介面卡是一個交叉連結層級的抽象概念。
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: 管理網路介面卡
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e1fd02426b27e3c07d4634edbe0215efa1c5c25c7a9c3abde32e991f766daf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078258"
---
# <a name="managing-network-adapters"></a>管理網路介面卡

IP Helper 提供管理網路介面卡的功能。 指定電腦上的介面和介面卡之間有一對一的對應關係。 介面是一個 IP 層級的抽象概念，而介面卡是一個交叉連結層級的抽象概念。

您可以使用下列段落中所述的函式，來取得本機電腦上網路介面卡的相關資訊。

[**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)函式會傳回 [**IP \_ 介面卡 \_ 資訊**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info)結構的陣列，本機電腦中的每個介面卡都有一個陣列。 [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)函數會傳回特定介面卡的其他相關資訊。 **GetPerAdapterInfo** 函式需要呼叫者指定介面卡的索引。 若要從介面卡名稱取得介面卡索引，請使用 [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) 函數。

有些應用程式會使用接收資料包的介面卡，但無法傳輸。 若要取得這些介面卡的相關資訊，請使用 [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) 函數。

[**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)函數可讓您取得與特定介面卡相關聯的 IP 位址。 此函式支援 IPv4 和 IPv6 定址。

-   如需涉及 [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) 的程式碼範例，請參閱 [使用 GetAdaptersInfo 管理網路介面卡](managing-network-adapters-using-getadaptersinfo.md)。

 

 



