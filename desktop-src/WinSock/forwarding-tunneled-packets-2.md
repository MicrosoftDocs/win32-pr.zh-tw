---
description: 接收封裝 (通道) 封包，並將它們 demultiplexes 到特定介面的程式碼有一項限制。
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: IPv6 轉送通道封包
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42138c746ea9d0ec8ea61bc3801b84a97a6bdd4c6fb6de0871e6b74447fdf28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132431"
---
# <a name="ipv6-forwarding-tunneled-packets"></a>IPv6 轉送通道封包

接收封裝 (通道) 封包，並將它們 demultiplexes 到特定介面的程式碼有一項限制。 如果您想要轉送透過已設定通道接收的通道封包，則必須在任何6個以上的介面和介面2上啟用轉送 \# 。 只在介面2上啟用轉送 \# 將無法運作。 通常在設定路由器時，您會在回送以外的所有介面上啟用轉送。

 

 



