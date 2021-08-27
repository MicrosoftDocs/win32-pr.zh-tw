---
description: 如先前所述，WSPJoinLeaf 是用來將分葉節點聯結到 multipoint 會話中。
ms.assetid: 03325f5e-4d4a-405b-b644-3d8c03435e17
title: 使用 WSPJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 057be0e2c1f2c3ffec21d64f3e95f6ad0ee584698e66f57cf4489ff6be887dc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121008"
---
# <a name="using-wspjoinleaf"></a>使用 WSPJoinLeaf

如先前所述， [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) 是用來將分葉節點聯結到 multipoint 會話中。 **WSPJoinLeaf** 與 [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) 具有相同的參數和語義，不同之處在于它會傳回通訊端描述項 (如 [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)) 中所示，而且它還有一個額外的 *dwFlags* 參數。 *DwFlags* 參數是用來指出通訊端是否只做為傳送者，只做為收件者，或兩者。 只有 multipoint 通訊端可以用於此函式中的輸入參數 *s* 。 如果 multipoint 通訊端處於非封鎖模式，傳回的通訊端描述項必須等到收到對應的 FD CONNECT 指示之後，才可使用 \_ 。 Multipoint 會話中的根應用程式可能會呼叫 **WSPJoinLeaf** 一次或多次，以便加入多個分葉節點，但一次最多隻能有一個 multipoint 連接要求。

[**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)傳回的通訊端描述項會根據輸入通訊端描述項是 c  \_ 根或 c 分葉而有所不同 \_ 。 搭配 c \_ 根通訊端使用時， *name* 參數會指定要加入的特定分葉節點，而傳回的通訊端描述項是 \_ 對應至新加入之分葉節點的 c 分葉通訊端。 它並不適合用來交換 multipoint 資料，而是用來接收網路事件指標 (例如，針對 \_ 存在於特定 c 分葉的連接，則會關閉) \_ 。 某些 multipoint 執行也可能會允許此通訊端用於根和個別分葉節點之間的並存聊天。 \_如果對應的分葉節點呼叫 [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))來卸載 multipoint 會話，則應該為這個通訊端提供 FD 關閉指示。 對稱地， 在 \_ 從 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)傳回的 c 分葉通訊端上叫用 WSPCloseSocket，會導致對應的分葉節點中的通訊端取得 FD \_ 關閉通知。

使用 c 分葉通訊端叫用 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) 時 \_ ， *name* 參數會包含根應用程式的位址 (用於根控制項配置) 或現有 multipoint 會話 (nonrooted 控制項配置) ，而傳回的通訊端描述項與輸入通訊端描述項相同。 在根控制項配置中，根用戶端會呼叫 WSPListen，將其 c \_ 根通訊端置於接聽[](/previous-versions/windows/hardware/network/ff566297(v=vs.85))模式。 \_當分葉節點要求將本身加入 multipoint 會話時，將會傳遞標準 FD 接受通知。 根用戶端會使用一般 [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) 函式來承認新的分葉節點。 從 **WSPAccept** 傳回的值也是 c 分 \_ 葉通訊端描述項，就像從 **WSPJoinLeaf** 傳回的值一樣。 若要容納可同時允許根起始和分葉起始聯結的 multipoint 配置，可接受 \_ 已在接聽模式中的 c 根通訊端，以做為 **WSPJoinLeaf** 的輸入。

Multipoint 根用戶端通常負責 multipoint 會話的有條理 dismantling。 這類應用程式可能會在 c 根通訊端上使用 [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) 或 [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) ， \_ 以產生所有相關聯的 c 分 \_ 葉通訊端，包括從 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) 傳回的，以及遠端分葉節點中對應的 c 分 \_ 葉通訊端，以取得 FD \_ 關閉通知。

 

 
