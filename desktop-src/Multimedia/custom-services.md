---
title: 自訂服務
description: 自訂服務
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- 多媒體檔案 i/o，自訂服務
- 檔案 i/o，自訂服務
- 輸入和輸出 (i/o) ，自訂服務
- I/o (輸入和輸出) ，自訂服務
- 自訂 i/o
- mmioInstallIOProc 函式
- mmioOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023429"
---
# <a name="custom-services"></a>自訂服務

多媒體檔案 i/o 服務使用 i/o 程式來處理與讀取和寫入不同類型的儲存系統（例如檔案保存系統和資料庫儲存系統）相關聯的實體輸入和輸出。 預先定義的 i/o 程式存在於標準檔案系統和記憶體檔案中，但是您可以使用 [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) 函式提供自訂的 i/o 程式來存取唯一的儲存系統。

若要使用自訂的 i/o 程式來開啟檔案，請使用 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 函數。 在檔案名中包含加號 (+) 或 CFSEPCHAR 常數，以將實體檔案名與您想要開啟之檔案的專案名稱分開。 下列範例會從名為 FILENAME 的檔案開啟名為 "element" 的檔案元素。弧：


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



當檔案 i/o 管理員遇到檔案名的加號時，它會檢查副檔名，以決定要與檔案相關聯的 i/o 程式。 在上述範例中，file i/o 管理員會嘗試使用與相關聯的 i/o 程式。ARC 副檔名;這個 i/o 程式會使用 [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)進行安裝。 如果未安裝任何 i/o 程式， [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 會傳回錯誤。

I/o 程式必須回應下列訊息：

-   [**MMIOM \_ 關閉**](mmiom-close.md)
-   [**MMIOM \_ 開啟**](mmiom-open.md)
-   [**MMIOM \_ 讀取**](mmiom-read.md)
-   [**MMIOM \_ 寫入**](mmiom-write.md)
-   [**MMIOM \_ 搜尋**](mmiom-seek.md)
-   [**MMIOM \_ 重新命名**](mmiom-rename.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)

您也可以使用 [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) 函式來建立自訂訊息，並將其傳送至您的 i/o 程式。 如果您定義自己的訊息，請確定其定義于或高於 MMIOM 使用者常數所定義的值 \_ 。

除了處理訊息之外，i/o 程式還必須維護 **mmioOpen** 函式的 *lpmmioinfo* 參數所指向之 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構 (的 **lDiskOffset** 成員) 。 **LDiskOffset** 成員一律必須包含下一個 MMIOM \_ READ 或 MMIOM \_ 寫入訊息將存取之位置的檔案位移。 位移是以位元組為單位來指定，且相對於檔案的開頭。 I/o 程式可以使用 **adwInfo** 成員來維護任何必要的狀態資訊。 I/o 程式不應該修改 **MMIOINFO** 結構中的任何其他成員。

 

 