---
description: NLA 能夠為其用戶端提供網路位置變更的通知。 用來要求變更事件通知的機制是 WSALookupServiceBegin、WSANSPIoctl 和 WSALookupServiceNext 函數的組合。
ms.assetid: fed5a90d-0bc5-46e7-b3d3-edc4b303d305
title: 來自 NLA 的通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8e7309fe6845d822702ffd81448999e2472ebdd37a6949812f622110ee9d42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822663"
---
# <a name="notification-from-nla"></a>來自 NLA 的通知

NLA 能夠為其用戶端提供網路位置變更的通知。 用來要求變更事件通知的機制是 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)、 [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)和 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 函數的組合。

為了接收來自 NLA 的變更通知，用戶端必須先呼叫 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) 來取得有效的 NLA SP 查閱控制碼。 接下來，用戶端可以依任何順序呼叫 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)或 [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) ;若要註冊通知，請呼叫 **WSANSPIoctl** 函式，並 \_ \_ 在 DWCONTROLCODE 參數中以 SIO 的 NSP 通知 \_ 變更控制程式碼集。 

[**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)函式會 \_ 將 WSA E \_ NO 其他傳回 \_ 為 set 分隔符號。 當用戶端已使用 [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) 函式註冊通知，而 **WSALookupServiceNext** 傳回 \_ 不超過的 WSA E 時 \_ \_ ，再次呼叫 **WSALookupServiceNext** 會顯示是否發生變更：

-   如果自先前的 WSA e 起未發生任何變更 \_ \_ \_ ，則不 \_ 會再傳回 WSA e \_ \_ 。
-   如果發生變更，或是發生了變更並進行輪詢呼叫， [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 函式呼叫會將網路傳回為 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構，並在其 **dwOutputFlags** 成員中設定下列其中一個旗標：

    <dl> \_已 \_ 新增結果  
    結果 \_ 已 \_ 變更  
    結果 \_ 已 \_ 刪除  
    </dl>

針對已變更的任何欄位，會提供變更通知，因為使用 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) 函式呼叫取得 NLA 查閱控制碼，或自最後一個列舉產生 WSA \_ E \_ 沒有 \_ 其他錯誤。 提供所有已變更的網路位置資訊時， \_ 不 \_ 會再傳回 WSA E \_ 。 用戶端可以在任何時間（一次一個）重新發出相同查詢控制碼上的 [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) 函式呼叫，並 \_ 設定 SIO 的 NSP \_ 通知 \_ 變更旗標。 這項功能可讓用戶端持續回收查詢控制碼，藉此讓用戶端不需要自行維護變更狀態資訊。 一旦用戶端不再需要變更通知，就應該使用 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) 函式來關閉查詢控制碼。

 

 



