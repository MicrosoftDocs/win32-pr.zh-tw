---
title: Null 會話
description: 有時抵達 null 會話的呼叫可能會顯示為已驗證的呼叫。
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462416"
---
# <a name="null-sessions"></a>Null 會話

有時抵達 null 會話的呼叫可能會顯示為已驗證的呼叫。 具體而言，呼叫 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) 函數會傳回用於呼叫的驗證層級和安全性提供者。 這種作業不表示呼叫不在 null 會話上。 這兩個問題是直角的。 在 Microsoft Windows 2000 上，遠端程序呼叫可以嘗試模擬呼叫者，並在模擬之後檢查許可權。 在 Microsoft Windows XP 上，呼叫 [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) 函式並檢查 **NullSession** 旗標會更快。

Windows 2000 和 Windows XP 之間存在另一個相關的差異。 如果指定了 [ \_ \_ 僅允許 \_ 安全的] 旗標，則 \_ 會在 Windows 2000 中呼叫 null 會話。 在 Windows XP 中，在預設安全性設定的一般情況下，當指定此旗標時，會拒絕對 null 會話的呼叫，並拒絕存取。 但是，即使是使用 RPC \_ [ \_ \_ 僅允許安全] 旗標 \_ ，rpc 仍無法保證呼叫使用者的許可權等級。 所有 RPC 檢查都是使用者有有效的認證。 呼叫使用者可能會使用 guest 帳戶或其他低許可權帳戶。 \_如果 \_ \_ 使用 [僅允許安全] \_ ，請確定伺服器在 RPC 之後不會採用高許可權。

 

 




