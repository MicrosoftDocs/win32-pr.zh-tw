---
description: 大部分的 getXbyY 函式都是由 Ws2 \_32.dll 轉譯為 WSALookupServiceBegin、WSALookupServiceNext 和 WSALookupServiceEnd 序列，其使用一組特殊 guid 作為服務類別。
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: API 中的 GetXbyY 基本方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511465"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a>API 中的 GetXbyY 基本方法

大部分的 **getXbyY** 函式都是由 Ws2 \_32.dll 轉譯為 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)、 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)和 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) 序列，其使用一組特殊 guid 作為服務類別。 這些 Guid 可識別正在模擬的 **getXbyY** 作業類型。 此查詢受限於支援 AF INET 的名稱服務提供者 \_ 。 每當 **getXbyY** 函數傳回 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) 或 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) 結構時，Ws2 \_32.dll \_ \_ 會在 **LUP** 中指定 WSALookupServiceBegin 傳回 BLOB 旗標，讓名稱服務提供者傳回所需的資訊。 這些結構必須稍微修改，因為在中包含的指標必須取代為相對於 blob 資料開頭的位移。 當然，這些指標參數所參考的所有值都必須完全包含在 blob 中，而且所有字串都是 ASCII。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[通訊協定獨立名稱解析](protocol-independent-name-resolution-2.md)
</dt> <dt>

[註冊和名稱解析](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



