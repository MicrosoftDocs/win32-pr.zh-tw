---
description: Windows 通訊端 (Winsock) 服務提供者介面 (SPI) 。
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974716"
---
# <a name="winsock-spi"></a>Winsock SPI

Winsock 服務提供者介面（或 Winsock SPI）是用來建立提供者的特定 Winsock 專業領域;傳輸提供者（例如 TCP/IP 或 IPX/SPX 通訊協定堆疊）使用 Winsock SPI，如同 (DNS) 的命名空間提供者，例如網際網路的網域命名系統。

傳統的網路程式設計，例如讓應用程式透過網路進行通訊，不需要使用 Winsock SPI 介面;請改用標準 [Winsock](winsock-reference.md) 介面。

 

Winsock SPI 會使用下列函數首碼命名慣例。



| 前置詞 | 意義                          | Description                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Windows 通訊端服務提供者 | 傳輸服務提供者進入點           |
| WPU    | Windows 通訊端提供者 Upcall  | \_服務提供者的 Ws232.dll 進入點    |
| WSC    | Windows 通訊端設定    | WS2 \_ 安裝 applet 的32.dll 進入點 |
| Nsp    | 命名空間提供者               | 命名空間提供者進入點                   |



 

 

 



