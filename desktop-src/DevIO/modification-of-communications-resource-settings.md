---
description: 當 CreateFile 函式開啟序列通訊資源的控制碼時，系統會根據上次開啟資源時所設定的值，初始化和設定資源。
ms.assetid: a39881d8-32af-4846-a2d3-508f1945b666
title: 設定的通訊資源修改
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a4658c58c07dfbd7ffe8ba7977db587211d3422359677999db312d05bd2c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911981"
---
# <a name="modification-of-communications-resource-settings"></a>設定的通訊資源修改

當 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式開啟序列通訊資源的控制碼時，系統會根據上次開啟資源時所設定的值，初始化和設定資源。 保留先前的設定可讓使用者在重新開啟裝置時，保留透過 **模式** 命令指定的設定。 繼承自先前開啟作業的值包含裝置控制區塊的設定， ([**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) 結構) 和 i/o 作業中使用的超時值。 如果裝置從未開啟過，則會使用系統預設值進行設定。

為了判斷序列通訊資源的初始設定，處理常式會呼叫 [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) 函式，此函式會以目前的設定來填滿序列埠 [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) 結構。 若要修改這個設定，進程會在 [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate)函數的呼叫中指定 **DCB** 結構。

[**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb)結構的成員會指定設定設定，例如串列傳輸速率、每個位元組的資料位數，以及每個位元組的停止位數目。 其他 **DCB** 成員會指定特殊字元，並啟用同位檢查和流量控制。 當處理常式只需要修改其中一些設定時，應該先呼叫 [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) ，以使用目前的設定來填入 **DCB** 結構。 然後，此程式可以調整 **DCB** 結構中的重要值，然後藉由呼叫 [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) 並指定修改過的 **DCB** 結構來重新設定裝置。 此程式可確保 **DCB** 結構的未修改成員包含適當的值。 例如，常見的錯誤是使用 **DCB** 結構來設定裝置，其中結構的 **XonChar** 成員等於 **XoffChar** 成員。

[**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba)函式提供另一種修改 [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb)結構的方式。 **BuildCommDCB** 使用的字串格式與 **mode** 命令的命令列引數相同，可指定傳輸速率、同位配置、停止位的數目，以及資料位的數目。 除了適當的成員設定為停用 XON/XOFF 和硬體流量控制之外，此函式不會變更其餘的 [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) 成員。 **BuildCommDCB** 只會修改 **DCB** 結構;它不會重新設定裝置。

處理常式可以使用 [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) 函式來重新設定通訊資源，以從設備磁碟機取得其所支援之設定的相關資訊。 此程式可以使用這項資訊來避免指定不支援的設定。

[**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate)函式會重新配置通訊資源，但不會影響指定驅動程式的內部輸出和輸入緩衝區。 緩衝區不會排清，且暫止的讀取和寫入作業不會提前終止。

進程會使用 [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm) 函式重新初始化通訊資源，此函式會執行下列工作：

-   終止暫止的讀取和寫入作業，即使它們尚未完成。
-   捨棄未讀取的字元，並釋出與指定資源相關聯之驅動程式的內部輸出和輸入緩衝區。
-   重新配置內部輸出和輸入緩衝區。

呼叫 [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm)不需要處理常式。 如果沒有，則資源的驅動程式會在第一次使用通訊資源控制碼時，使用預設設定來初始化裝置。

 

 
