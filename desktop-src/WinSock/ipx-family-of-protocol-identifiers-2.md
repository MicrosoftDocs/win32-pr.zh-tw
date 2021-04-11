---
description: 通訊端和 WSASocket 中的通訊協定參數是一種識別碼，可建立網路類型，以及用來識別網路上所執行之各種傳輸通訊協定的方法。
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: IPX 通訊協定識別碼系列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113049"
---
# <a name="ipx-family-of-protocol-identifiers"></a>IPX 通訊協定識別碼系列

[**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket)和 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)中的 *通訊協定* 參數是一種識別碼，可建立網路類型，以及用來識別網路上所執行之各種傳輸通訊協定的方法。 不同于 IP，IPX 不會使用單一通訊協定值來選取傳輸堆疊。 由於沒有任何網路需求可針對每個傳輸通訊協定使用特定的值，因此我們可以自由地以 Winsock 應用程式方便的方式指派它們。 我們會避免值0到255，以避免與對應的 PF \_ INET 通訊協定值發生衝突。



| Name         | 值       | 通訊端類型              | Description                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| 保留     | 0-255       |                           | 保留給 PF \_ INET 通訊協定值。              |
| NSPROTO \_ IPX | 1000-1255 | SOCK \_ DGRAM SOCK \_ RAW     | 適用于 IPX 的資料包服務。                           |
| NSPROTO \_ SPX | 1256        | SOCK \_ STREAM SOCK \_ SEQPKT | 使用固定大小的封包進行可靠的封包交換。 |



 

> [!Note]  
> 指定 NSPROTO \_ spx 時，如果兩個端點都能夠執行此動作，則會自動使用 SPX II 通訊協定。

 

 

 



