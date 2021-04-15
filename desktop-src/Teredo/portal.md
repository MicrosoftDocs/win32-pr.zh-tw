---
title: Teredo
description: .
ms.assetid: fc213675-dbdb-42a1-a09f-dda598b95b94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c1d0f2c03043a7d56a6729d51e1f89c9739ef6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507413"
---
# <a name="teredo"></a>Teredo

## <a name="purpose"></a>目的

Teredo 是一種 IPv6 轉換技術，當 IPv6/IPv4 主機位於一或多個 IPv4 網路位址轉譯器 (Nat) 之後，可為單播 IPv6 流量提供位址指派和主機對主機自動通道。 為了流經 IPv4 Nat，IPv6 封包會以 IPv4 使用者資料包協定的形式傳送 (UDP) 訊息。

## <a name="developer-audience"></a>開發人員對象

Teredo 的設計目的是要讓具有 IPv6 網路程式設計經驗的 C/c + + 開發人員使用。

## <a name="run-time-requirements"></a>執行階段需求求

Teredo 介面主要支援 Windows Vista 和 Windows Server 2008。 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 所支援的 Teredo 介面功能有限，在透過 [Teredo 接收請求的流量](receiving-solicited-traffic-over-teredo.md)中有詳細的說明。

## <a name="in-this-section"></a>本節內容



| 主題                                       | 描述                                                                                |
|---------------------------------------------|--------------------------------------------------------------------------------------------|
| [關於 Teredo](about-teredo.md)<br/> | Teredo 介面的相關資訊。<br/>                                         |
| [使用 Teredo](using-teredo.md)<br/> | Teredo 介面之執行和一般使用方式的相關資訊。<br/> |



 

 

 





