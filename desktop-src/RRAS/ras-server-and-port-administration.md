---
title: 關於 RAS 伺服器和埠管理
description: RAS 伺服器管理功能會取得指定的 RAS 伺服器與其埠的相關資訊。 這些函式也可用來在指定的 RAS 伺服器埠上終止連接。
ms.assetid: eedac23e-d716-451e-b08b-594398656bb5
keywords:
- RAS 系統管理 RRAS、伺服器和埠管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb9d3cc520efa6bbb492e8d9e967d423548f96a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104462620"
---
# <a name="about-ras-server-and-port-administration"></a>關於 RAS 伺服器和埠管理

RAS 伺服器管理功能會取得指定的 RAS 伺服器與其埠的相關資訊。 這些函式也可用來在指定的 RAS 伺服器埠上終止連接。

[**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo)函數會傳回 [**MPR \_ 伺服器 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_server_0)結構，其中包含 RAS 伺服器設定的相關資訊。 傳回的資訊包括目前可用的埠數目、目前使用中的埠數目，以及伺服器版本號碼。

[**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)函式會捕獲 [**RAS \_ 埠 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0)結構的陣列。 每個結構都包含 RAS 伺服器上所設定的其中一個埠的資訊。 每個埠的資訊包括：

-   埠的名稱
-   連接到埠之裝置的相關資訊
-   與埠相關聯的 RAS 伺服器是否為 Windows NT/Windows 2000 伺服器
-   埠是否正在使用中，如果是，則連接的相關資訊

若要取得特定連接所使用的通訊埠，請在 *hConnection* 參數中將控制碼傳遞至該連接的 [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) 。 若要取得連接的控制碼，請使用 [**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum) 函數。 或者，如果您已執行 [RAS 管理 DLL](ras-administration-dll.md)， [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) 和 [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) 函數會在建立連線時，收到每個新連線的控制碼。

您可以呼叫 [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) 函數，以取得有關 RAS 伺服器上指定埠的其他資訊。 此函式會傳回包含 [**ras \_ 埠 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0)結構的 [**ras \_ 埠 \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1)結構，以及埠目前狀態的其他相關資訊。 [**RasAdminPortGetInfo**](rasadminportgetinfo.md)函式也會傳回 [**RAS \_ 參數**](ras-parameters-str.md)結構的陣列，以描述與埠相關聯之任何媒體特定金鑰的值。 **Ras \_ 參數** 結構會使用 [**ras \_ PARAMS \_ 格式**](ras-params-format-str.md)列舉的值，來指出每個媒體特定索引鍵的值格式。

[**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)函式也會傳回 [**RAS \_ 埠 \_ 統計**](ras-port-statistics-str.md)結構，其中包含埠上目前連接（如果有的話）的各種統計資料計數器。 針對屬於多重連結連線的通訊埠， **MprAdminPortGetInfo** 會傳回與連接相關之所有埠的個別埠和累計統計資料的統計資料。 您可以使用 [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) 函數來重設埠的統計資料計數器。 [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)函式會中斷使用中的埠。

您可以使用 [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) 函式來釋放 [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) 和 [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) 函式所配置的記憶體。 您可以使用 [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) 函式來取得字串，此字串描述其中一個 ras 伺服器管理 (RasAdmin) 函式所傳回的 ras 錯誤碼。

 

 




