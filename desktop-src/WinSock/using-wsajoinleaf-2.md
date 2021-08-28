---
description: 如先前所述，函式 WSAJoinLeaf 是用來將分葉節點聯結至 multipoint 會話中。
ms.assetid: eaa1593a-36eb-4d92-a3d9-91566fc0216b
title: 使用 WSAJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13b6d82960f74135fa519a1284a1274b878e18c32f59d9c2b8c46ebd592c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121018"
---
# <a name="using-wsajoinleaf"></a>使用 WSAJoinLeaf

如先前所述，函式 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 是用來將分葉節點聯結至 multipoint 會話中。 **WSAJoinLeaf** 與 [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) 具有相同的參數和語義，不同之處在于它會傳回通訊端描述項 (如 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)) 中所示，而且它還有一個額外的 *dwFlags* 參數。

*DwFlags* 參數是用來指出通訊端是否只做為傳送者，只做為收件者，或兩者。 只有 multipoint 通訊端可以用於此函式中的輸入參數 *s* 。 如果 multipoint 通訊端處於非封鎖模式，則在收到對應的 FD 連接指示之前，無法使用傳回的通訊端描述項 \_ 。 Multipoint 會話中的根應用程式可能會呼叫 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 一次或多次，以便加入多個分葉節點，但一次最多隻能有一個 multipoint 連接要求。

[**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)傳回的通訊端描述項會根據輸入通訊端描述項是c \_ 根或 c 分葉而有所不同 \_ 。 搭配 c \_ 根通訊端使用時， *name* 參數會指定要加入的特定分葉節點，而傳回的通訊端描述項是 \_ 對應至新加入之分葉節點的 c 分葉通訊端。 它並不適合用來交換 multipoint 資料，而是用來接收 FD XXX 指標 (例如，針對 \_ \_ 存在於特定 c 分葉的連接關閉) \_ 。 某些 multipoint 執行也可能會允許此通訊端用於根和個別分葉節點之間的並存聊天。 \_如果對應的分葉節點呼叫 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)來捨棄 multipoint 會話，則會收到此通訊端的 FD 關閉指示。 對稱地， 在 \_ 從 **WSAJoinLeaf** 傳回的 c 分葉通訊端上叫用導致 closesocket，會導致對應的分葉節點中的通訊端取得 FD \_ 關閉通知。

使用 c 分葉通訊端叫用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 時 \_ ， *name* 參數會包含根應用程式的位址 (用於根控制項配置) 或現有 multipoint 會話 (nonrooted 控制項配置) ，而傳回的通訊端描述項與輸入通訊端描述項相同。 在根控制項配置中，根應用程式會藉由呼叫接聽，將其 c \_ 根[](/windows/desktop/api/Winsock2/nf-winsock2-listen)通訊端置於接聽模式。 \_當分葉節點要求將本身聯結至 multipoint 會話時，會傳遞標準 FD 接受通知。 根應用程式會使用一般的 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) / [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)函式來承認新的分葉節點。 從 **accept** 或 **WSAAccept** 傳回的值也是 c 分 \_ 葉通訊端描述項，就像從 **WSAJoinLeaf** 傳回的值一樣。 若要容納可同時允許根起始和分葉起始聯結的 multipoint 配置，可接受 \_ 已在接聽模式中的 c 根通訊端作為 **WSAJoinLeaf** 的輸入。

Multipoint 根應用程式通常負責 multipoint 會話的有條理 dismantling。 這類應用程式可能會在 c 根通訊端上使用 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) 或 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) \_ ，使所有相關聯的 c 分 \_ 葉通訊端（包括從 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 傳回的通訊端，以及遠端分葉節點中對應的 c 分 \_ 葉通訊端）取得 FD \_ 關閉通知。

 

 



