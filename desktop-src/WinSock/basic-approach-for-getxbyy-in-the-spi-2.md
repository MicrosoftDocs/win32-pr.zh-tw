---
description: 大部分的 GetXbyY 函式都是由 Ws2 \_32.dll 轉譯為 WSALookupServiceBegin、WSALookupServiceNext、WSALookupServiceEnd 序列，其使用一組特殊 guid 作為服務類別。
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: SPI 中的 GetXbyY 基本方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d635230bb1c1205d0f6e1aee16fe7c7ac9eab5b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848025"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a>SPI 中的 GetXbyY 基本方法

大部分的 **GetXbyY** 函式都是由 Ws2 \_32.dll 轉譯為 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)、 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)、 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) 序列，其使用一組特殊 guid 作為服務類別。 這些 Guid 可識別正在模擬的 **GetXbyY** 作業類型。 此查詢受限於支援 AF INET 的 Nsp \_ 。 每當 **GetXbyY** 函式傳回 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) 或 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) 結構時，Ws2 \_32.dll 將會 \_ \_ 在 **LUP** 中指定 WSALookupServiceBegin 傳回 BLOB 旗標，讓 NSP 傳回所需的資訊。 這些結構必須稍微修改，因為在中包含的指標必須取代為相對於 blob 資料開頭的位移。 當然，這些指標成員參考的所有值都必須完全包含在 blob 中，而且所有字串都是 ASCII。

 

 



