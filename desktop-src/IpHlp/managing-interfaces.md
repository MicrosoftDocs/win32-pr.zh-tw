---
description: IP 協助程式可延伸您管理網路介面的能力。 指定電腦上的介面和介面卡之間有一對一的對應關係。 介面是一個 IP 層級的抽象概念，而介面卡是一個交叉連結層級的抽象概念。
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: 管理介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb46ecba6f1c5780960f6d8e363db9ec04d0cc3611da1caf023ec95bf5a99a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146691"
---
# <a name="managing-interfaces"></a>管理介面

IP 協助程式可延伸您管理網路介面的能力。 指定電腦上的介面和介面卡之間有一對一的對應關係。 介面是一個 IP 層級的抽象概念，而介面卡是一個交叉連結層級的抽象概念。

使用下列段落中所述的功能來管理本機電腦上的介面。

[**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)函數會傳回本機電腦上的介面數目。

[**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)函數會傳回一個資料表，其中包含本機電腦上介面的名稱和對應的索引。 如需涉及 **GetInterfaceInfo** 的程式碼範例，請參閱 [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)。

[**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)函式會接受介面索引，並傳回回溯相容的介面索引，也就是只使用較低24位的介面索引。 這種類型的索引有時稱為「易記」介面索引。

[**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry)函數會傳回 [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow)結構，其中包含本機電腦上特定介面的相關資訊。 此函式需要呼叫端提供介面的索引。

[**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable)函式會傳回 [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow)專案的資料表，也就是電腦上的每個介面各一個。

您可以使用 [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) 函數來修改特定介面的設定。

 

 
