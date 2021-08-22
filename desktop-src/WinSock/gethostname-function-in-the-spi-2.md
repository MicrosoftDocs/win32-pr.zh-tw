---
description: WSALookupServiceBegin 查詢會使用 SVCID \_ 主機名稱作為服務類別 GUID。
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: SPI 中的 gethostname 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b610016222ab8a06ed874377be9ae447ad1d194ab9605a6e07b3cf829f520093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132261"
---
# <a name="gethostname-function-in-the-spi"></a>SPI 中的 gethostname 函式

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)查詢會使用 SVCID \_ 主機名稱作為服務類別 GUID。 如果 *lpszServiceInstanceName* 為 null 或參考 null 字串 (即為。 "" ) ，將會解析本機主機。 否則，應該會在指定的主機名稱上進行查閱。 基於模擬 [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) 的目的，Ws2 \_32.dll 將會指定 *lpszServiceInstanceName* 的 Null 指標，並指定 LUP \_ \_ 傳回名稱，以便在 *lpszServiceInstanceName* 參數中傳回主機名稱。 如果應用程式使用此查詢並指定 LUP \_ RETURN \_ ADDR，則會在 **CSADDR \_ 資訊** 結構中提供主機位址。 此查詢的 LUP 傳回 \_ \_ BLOB 動作未定義。 除非 *lpszQueryString* 參考的服務（例如 ftp），否則埠資訊會預設為零，在此情況下，將會提供指定服務的完整傳輸位址。

 

 



