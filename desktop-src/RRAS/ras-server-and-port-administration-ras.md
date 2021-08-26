---
title: RAS 伺服器和埠管理
description: RAS 伺服器管理功能可讓您取得指定的 RAS 伺服器與其埠的相關資訊。 這些功能也可讓您在指定的 RAS 伺服器埠上終止連接。
ms.assetid: 783b0ded-7c0e-49eb-8040-563d5dd675f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d09d683bf0850b5f51a5d9c1ac1aa21b25f2968ddedbed2d383d28dad7785f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028798"
---
# <a name="ras-server-and-port-administration"></a>RAS 伺服器和埠管理

RAS 伺服器管理功能可讓您取得指定的 RAS 伺服器與其埠的相關資訊。 這些功能也可讓您在指定的 RAS 伺服器埠上終止連接。

[**RasAdminServerGetInfo**](rasadminservergetinfo.md)函式會傳回 [**ras \_ 伺服器 \_ 0**](ras-server-0-str.md)結構，其中包含 ras 伺服器設定的相關資訊。 傳回的資訊包括目前可用的埠數目、目前使用中的埠數目，以及伺服器版本號碼。

[**RasAdminPortEnum**](rasadminportenum.md)函式會抓取 [**ras \_ 埠 \_ 0**](ras-port-0-str.md)結構的陣列，其中包含 ras 伺服器上所設定之每個埠的資訊。 每個埠的資訊包括：

-   埠的名稱
-   連接到埠之裝置的相關資訊
-   與埠相關聯的 RAS 伺服器是否為 Windows NT/Windows 2000 伺服器
-   埠是否正在使用中，如果是，則連接的相關資訊

您可以呼叫 [**RasAdminPortGetInfo**](rasadminportgetinfo.md) 函數，以取得有關 RAS 伺服器上指定埠的其他資訊。 此函式會傳回包含 [**ras \_ 埠 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0)結構的 [**ras \_ 埠 \_ 1**](ras-port-1-str.md)結構，以及埠目前狀態的其他相關資訊。 **RasAdminPortGetInfo** 函式也會傳回 [**RAS \_ 參數**](ras-parameters-str.md)結構的陣列，以描述與埠相關聯之任何媒體特定金鑰的值。 **Ras \_ 參數** 結構會使用 [**ras \_ PARAMS \_ 格式**](ras-params-format-str.md)列舉的值，來指出每個媒體特定索引鍵的值格式。

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)函式也會傳回 [**RAS \_ 埠 \_ 統計**](ras-port-statistics-str.md)結構，其中包含埠上目前連接（如果有的話）的各種統計資料計數器。 針對屬於多重連結連線的通訊埠， **RasAdminPortGetInfo** 會傳回與連接相關之所有埠的個別埠和累計統計資料的統計資料。 您可以使用 [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) 函數來重設埠的統計資料計數器。 [**RasAdminPortDisconnect**](rasadminportdisconnect.md)函式會中斷使用中的埠。

您可以使用 [**RasAdminFreeBuffer**](rasadminfreebuffer.md) 函式來釋放 [**RasAdminPortEnum**](rasadminportenum.md) 和 [**RasAdminPortGetInfo**](rasadminportgetinfo.md) 函式所配置的記憶體。 您可以使用 [**RasAdminGetErrorString**](rasadmingeterrorstring.md) 函式來取得字串，此字串描述其中一個 ras 伺服器管理 (RasAdmin) 函式所傳回的 ras 錯誤碼。

 

 




