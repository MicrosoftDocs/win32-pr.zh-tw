---
description: WSARecv、WSARecvFrom、WSARecvMsg、WSASend、WSASendMsg 和 WSASendTo 函數全都採用應用程式緩衝區的陣列作為輸入參數，並可用於散佈/收集 (或向量) i/o。
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: 散佈/收集 i/o
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4dc580065655c2d69485a49cd41919345c566c32ec2ff9cd1055383853c7438
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794678"
---
# <a name="scattergather-io"></a>散佈/收集 i/o

[**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)、 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)、 [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)、 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)、 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)和 [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto)函數全都採用應用程式緩衝區的陣列作為輸入參數，並可用於散佈/收集 (或向量) i/o。 這在傳送的每個訊息的部分包含一或多個固定長度的標頭元件（除了訊息內文以外）時，這可能非常有用。 在傳送之前，應用程式不需要將這類標頭元件串連成單一連續緩衝區。 同樣地，在接收時，標頭元件可以自動分割成不同的緩衝區，並將訊息主體視為本身。

當接收到多個緩衝區時，不論是否使用所有提供的緩衝區，都會在從網路抵達資料時完成。

 

 
