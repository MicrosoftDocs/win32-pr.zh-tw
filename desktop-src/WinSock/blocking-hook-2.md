---
description: 雖然這項機制足以滿足簡單的應用程式，但它無法支援更高階應用程式的複雜訊息分派需求，例如使用多重文件介面 (MDI) 模型。
ms.assetid: e4558e71-bbec-415a-a7c2-9025a4d6c474
title: 封鎖攔截
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd098692784a662456c990a238bd309db0c321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001336"
---
# <a name="blocking-hook"></a>封鎖攔截

雖然這項機制足以滿足簡單的應用程式，但它無法支援更高階應用程式的複雜訊息分派需求，例如使用多重文件介面 (MDI) 模型。 針對這類應用程式，應用程式可能會安裝執行緒特定的封鎖攔截器。 這會由服務提供者呼叫，而不是先前所述的預設封鎖掛勾。 服務提供者必須藉 \_ 由呼叫 [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback)，從 Ws232.dll 取出每個執行緒的指標。 如果應用程式沒有自行安裝封鎖攔截，則會傳回預設封鎖攔截函式的指標。

Windows 通訊端服務提供者無法假設應用程式提供的封鎖攔截器，可讓訊息處理繼續進行，因為預設封鎖攔截器會執行此操作。 某些應用程式在封鎖作業未完成時，無法容忍可重新進入訊息的可能性。 這類應用程式封鎖攔截函式只會傳回 **FALSE**。 如果服務提供者相依于其內部作業的訊息，它可能會在執行應用程式的封鎖攔截器之前執行 **PeekMessage** (hMyWnd ... ) ，讓它可以取得自己的訊息，而不會影響系統的其餘部分。

Windows 的先占式多執行緒版本未安裝預設封鎖攔截。 這是因為如果單一應用程式正在等待作業完成 (而不是呼叫 **PeekMessage** 或 **GetMessage** ，而導致應用程式在 nonpreemptive Windows) 中產生處理器，則不會封鎖其他進程。 當服務提供者呼叫 [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback) 時，將會傳回 null 指標，表示提供者是使用原生作業系統封鎖函式。 不過，為了維持回溯相容性，應用程式提供的封鎖攔截仍可以在 Windows 中以個別執行緒的形式安裝。

只有在下列所有條件都成立時，Winsock 服務提供者才會呼叫封鎖攔截：常式是定義為可以封鎖的常式、指定的通訊端是封鎖通訊端，而且無法立即完成要求。 如果只使用非封鎖通訊端和 [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) / [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) ，而不是使用 [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) ，則永遠不會呼叫封鎖掛勾。

> [!Note]  
> 如果在 pseudoblocking 期間用來封鎖執行緒，則會收到執行緒的 Windows 訊息，而執行緒會嘗試發出另一個 Winsock 呼叫的風險。 由於安全地管理此狀況的困難，因此 Windows 通訊端1.1 規格不允許這種行為。 不允許指定的執行緒進行多個嵌套的 Winsock 函式呼叫。 特定執行緒只允許一個未處理的函式呼叫。 任何嵌套的 Winsock 函式呼叫都會失敗，並出現錯誤 WSAEINPROGRESS。 請注意，這項限制適用于封鎖和非封鎖作業，但僅適用于 Windows 通訊端1.1 環境。 這項規則有一些例外狀況，包括兩個可讓應用程式判斷 pseudoblocking 作業是否正在進行的函式，以及是否要在需要時取消這類作業。 以下將說明這些情況。

 

 

 
