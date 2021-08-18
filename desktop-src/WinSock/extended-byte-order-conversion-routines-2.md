---
description: Windows通訊端2不會假設所有通訊協定的網路位元組順序都相同。
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: 擴充 Byte-Order 轉換常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2be1c217e89d19e607a64dfc943449351021506dc88f73ebcd4234a26b2b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132521"
---
# <a name="extended-byte-order-conversion-routines"></a>擴充 Byte-Order 轉換常式

Windows通訊端2不會假設所有通訊協定的網路位元組順序都相同。 提供一組轉換常式，以將16位和32位的數量轉換成網路位元組順序。 這些常式會以具有與其相關聯之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構的通訊端控制碼作為輸入參數。 **WSAPROTOCOL \_ 資訊** 結構的 **NetworkByteOrder** 成員會指定所需的網路位元組順序 (目前是位元組由大到小或由小到大的) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[將通訊端應用程式移植到 Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Winsock 程式設計考慮](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
