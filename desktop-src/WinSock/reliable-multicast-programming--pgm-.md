---
description: 本節說明 Windows 中的實際一般多播 (PGM) 多播通訊協定，通常稱為可靠的多播。 可靠多播是透過 Windows Server 2003 和更新版本中的 Windows 通訊端來實行。
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: '可靠的多播程式設計 (PGM) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c34365bdc8db553d24182fcb193dc03177627ccf9b00a03f309ab4cf7bbe01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559950"
---
# <a name="reliable-multicast-programming-pgm"></a>可靠的多播程式設計 (PGM) 

本節說明 Windows 中的實際一般多播 (PGM) 多播通訊協定，通常稱為可靠的多播。 可靠多播是透過 Windows Server 2003 和更新版本中的 Windows 通訊端來實行。

**Windows XP：** 只有在安裝 Microsoft Message Queuing (MSMQ) 3.0 時，才支援 PGM。

PGM 是可靠且可擴充的多播通訊協定，可讓接收者偵測遺失、要求重新傳輸遺失的資料，或通知應用程式無法復原的遺失。 PGM 是接收者可靠的通訊協定，這表示接收者負責確保收到所有資料，absolving 接收責任的寄件者。

PGM 適用于需要從多個來源將無重複的多播資料傳遞給多個接收者的應用程式。 PGM 不支援認可的傳遞，也無法保證來自多個寄件者的封包順序。

如需有關 PGM 的詳細資訊，請參閱 [www.ietf.org](https://www.ietf.org/)提供的 RFC 3208。

本節說明如何在 Windows 上使用可靠的多播。 下列主題說明使用 Windows 通訊端建立可靠多播應用程式的各個層面：

-   [PGM 寄件者和接收者](pgm-senders-and-receivers.md)
-   [PGM 寄件者選項](pgm-sender-options.md)
-   [傳送和接收 PGM 資料](sending-and-receiving-pgm-data.md)
-   [多宿主和 PGM](multihoming-and-pgm.md)
-   [PGM 通訊端選項](pgm-socket-options.md)

 

 



