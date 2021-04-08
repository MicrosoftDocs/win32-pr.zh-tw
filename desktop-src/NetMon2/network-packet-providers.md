---
description: 網路封包提供者 (NPPs) 是網路監視器系統元件，可從網路收集網路流量 (框架) ，然後將這些流量傳遞至網路監視器 UI，以及 NPP 應用程式。
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: 網路封包提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852708"
---
# <a name="network-packet-providers"></a>網路封包提供者

網路封包提供者 (NPPs) 是網路監視器系統元件，可從網路收集網路流量 (框架) ，然後將這些流量傳遞至網路監視器 UI，以及 [*NPP 應用程式*](n.md)。

下圖顯示兩個 NPPs：網路監視器提供的 NDIS NPP 和自訂 NPP。

![網路監視器和自訂 npp 所提供的 ndis npp](images/npp.png)

網路監視器所提供的 NDIS NPP 是 Ndisnpp.dll。 此 NPP 使用網路監視器系統驅動程式 (Nmnt.sys) 來取得從網路收集的畫面格，以及數個 COM 介面 (稱為 NPP 介面) 將框架傳遞至網路監視器 UI，以及 NPP 應用程式，可在其中顯示和分析這些應用程式。

Ndisnpp.dll 會連接到 [*NDIS*](n.md) 層以取得其網路流量。  (的自訂 NPPs 可以略過 NDIS 層，並直接與網路硬體通訊。 ) 請注意，不論 NPP 是否使用 NDIS，NPPs 都可以連線到任意數目的網路卡，而且所有 NPPs 都必須支援相同的 NPP 介面。

在應用程式開始捕獲資料之前，必須先：

-   選取將 NPP 連接到網路的網路介面卡 (NIC) 。
-   選取將用來捕捉網路框架的 NPP 介面。
-   使用選取的介面連接至 NIC。

如需有關如何列舉和選取網路介面卡的詳細資訊，請參閱 [選取網路介面卡](selecting-a-network-interface-card.md)。

如需 NPPs 所公開的 COM 介面的詳細資訊，請參閱 [選取 NPP 介面](selecting-an-npp-interface.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IDelaydC**](idelaydc.md)
</dt> <dt>

[**IESP**](iesp.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**IStats**](istats.md)
</dt> </dl>

 

 



