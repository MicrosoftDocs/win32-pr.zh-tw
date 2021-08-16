---
title: Teredo
description: Teredo
ms.assetid: fc213675-dbdb-42a1-a09f-dda598b95b94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 946932d7a699a4e9b993ed93e8d48faafbd75fbb0ec54e61b260b8a25e634ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354461"
---
# <a name="teredo"></a>Teredo

## <a name="purpose"></a>目的

Teredo 是一種 IPv6 轉換技術，當 IPv6/IPv4 主機位於一或多個 IPv4 網路位址轉譯器 (Nat) 之後，可為單播 IPv6 流量提供位址指派和主機對主機自動通道。 為了流經 IPv4 Nat，IPv6 封包會以 IPv4 使用者資料包協定的形式傳送 (UDP) 訊息。

## <a name="developer-audience"></a>開發人員對象

Teredo 的設計目的是要讓具有 IPv6 網路程式設計經驗的 C/c + + 開發人員使用。

## <a name="run-time-requirements"></a>執行階段需求求

Teredo 介面主要受到 Windows Vista 和 Windows Server 2008 的支援。 Windows XP （含 Service Pack 2） (SP2) 和 Windows Server 2003 所支援的 teredo 介面功能有限，在透過[Teredo 接收請求的流量](receiving-solicited-traffic-over-teredo.md)中有詳細的說明。

## <a name="in-this-section"></a>本節內容



| 主題                                       | 描述                                                                                |
|---------------------------------------------|--------------------------------------------------------------------------------------------|
| [關於 Teredo](about-teredo.md)<br/> | Teredo 介面的相關資訊。<br/>                                         |
| [使用 Teredo](using-teredo.md)<br/> | Teredo 介面之執行和一般使用方式的相關資訊。<br/> |



 

 

 





