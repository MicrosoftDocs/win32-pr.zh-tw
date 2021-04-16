---
title: 藍牙和 WSASetService
description: 藍牙使用 WSASetService 函式來註冊或移除藍牙命名空間內的服務實例， (NS \_ BTH) 從登錄。
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- 藍牙藍牙
- WSASetService 藍牙
- 藍牙與 WSASetService 藍牙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463209"
---
# <a name="bluetooth-and-wsasetservice"></a>藍牙和 WSASetService

藍牙使用 [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) 函式來註冊或移除藍牙命名空間內的服務實例， (NS \_ BTH) 從登錄。 這項作業所傳回的控制碼只能用來刪除服務。

藍牙有兩種使用 [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) 函式來通告服務的方法：

-   此應用程式可以讓系統通告簡單的藍牙 SDP 服務記錄，並從 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) 結構中的標準成員進行建立。
-   應用程式可以讓系統通告自己的藍牙 SDP 記錄，方法是在 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的 **lpBlob** 成員中傳遞 [**BTH \_ SET \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)結構。 這是更複雜的方法。

> [!Note]  
> [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea)公告的 SDP 記錄不會在發行它們的進程結束後保存。

 

使用 [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) 搭配藍牙有下列需求：

-   *LpqsRegInfo* 參數是要註冊之 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的位址。
-   *EssOperation* 參數是一種列舉，其中包含下表所示的其中一項作業。



| 值                  | 描述                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| RNRSERVICE \_ 註冊   | 使用藍牙 SDP 通訊協定開始通告服務，以進行遠端無線電波查詢。 |
| RNRSERVICE 取消 \_ 註冊 | 無效。 傳回錯誤。                                                               |
| RNRSERVICE \_ 刪除     | 停止通告服務。                                                             |



 

> [!Note]  
> 在 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) 或 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) 呼叫期間探索到的服務控制碼與 RNRSERVICE 刪除作業不相容 \_ 。

 

-   *DwControlFlags* 參數是保留的，而且必須為零。

如需詳細資訊和藍牙通訊端選項的清單，請參閱 [藍牙和通訊端選項](bluetooth-and-socket-options.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 