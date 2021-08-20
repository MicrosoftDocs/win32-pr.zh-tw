---
description: 有幾個通訊端屬性可透過 WSPSocket 中的旗標參數來表示。
ms.assetid: 5fd4321b-a5cc-4921-bec5-bdf625261ea2
title: 通訊端屬性旗標和模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2943116c58c77d53cefa4e8d238f9c5542ea71840b31f979ffbe6eb7f1c2550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927330"
---
# <a name="socket-attribute-flags-and-modes"></a>通訊端屬性旗標和模式

有幾個通訊端屬性可透過 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)中的 *旗標* 參數來表示。 WSA 旗標重迭 \_ \_ 旗標表示將會使用通訊端來進行重迭的 i/o 作業。 所有服務提供者都必須支援此屬性。 如需詳細資訊，請參閱重迭的 [i/o](overlapped-i-o-2.md) 。 請注意，若要建立具有重迭屬性的通訊端，就不會影響通訊端目前處於封鎖或非封鎖模式。 使用重迭屬性建立的通訊端可以用來執行重迭的 i/o，而這樣做並不會變更通訊端的封鎖模式。 由於重迭的 i/o 作業不會封鎖，因此通訊端的封鎖模式與這些作業無關。

建立要用於 multipoint 和/或多播作業的通訊端時，會使用四個額外的屬性旗標，而這些屬性的支援是選擇性的。 支援 multipoint 屬性的提供者會 \_ \_ 在其各自的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構中透過 XP1 支援 multipoint bit 來指出這一點。 如需這些旗標的定義和使用方式，請參閱 API 中的 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) 和 [通訊協定獨立多播和 Multipoint](protocol-independent-multicast-and-multipoint-in-the-spi-2.md) 。 只有使用 multipoint 相關屬性建立的通訊端可以用在 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) 函式中，以建立 multipoint 會話。

通訊端處於兩種模式的其中一種，也就是封鎖和非封鎖的。 通訊端預設會在封鎖模式下建立，而且可以藉由呼叫 [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))、 [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))或 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))來變更為非封鎖模式。 如果沒有作用中的 **WSPAsyncSelect** 或 **WSPEventSelect** ，則可以使用 **WSPIoctl** ，將通訊端切換回封鎖模式。 通訊端的模式只會影響可能封鎖的函式，而不會影響重迭的 i/o 作業。 如需詳細資訊，請參閱 [封鎖作業](blocking-operations-2.md) 。

 

 
