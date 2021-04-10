---
description: 若要將檔案中的資料對應至進程的虛擬記憶體，您必須建立檔案的視圖。
ms.assetid: b1ebd9a4-cde4-4c0c-80d2-5ccb655cd3a4
title: 建立檔案視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498f7ba132efd9ecf82f9ec087492c9622824b51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944165"
---
# <a name="creating-a-file-view"></a>建立檔案視圖

若要將檔案中的資料對應至進程的虛擬記憶體，您必須建立檔案的視圖。 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile)和 [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex)函式會使用 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)所傳回的檔案對應物件控制碼，在進程的虛擬位址空間中建立檔案的視圖或部分檔案。 如果存取旗標與 **CreateFileMapping** 建立檔案對應物件時所指定的旗標發生衝突，則這些函式會失敗。

[**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile)函式會傳回檔案視圖的指標。 藉由在 **MapViewOfFile** 中指定的位址範圍內取值指標，應用程式可以從檔案讀取資料，並將資料寫入檔案。 寫入檔案視圖會導致檔案對應物件的變更。 實際寫入磁片上的檔案是由系統處理。 資料在寫入檔案對應物件時，不會實際傳送。 相反地，大部分的檔案輸入和輸出 (i/o) 都會進行快取，以改善一般系統效能。 應用程式可以藉由呼叫 [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) 函式來強制系統立即執行磁片交易，藉以覆寫此行為。

[**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex)函式的運作方式與 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile)函式完全相同，不同之處在于它可讓進程在 *lpvBase* 參數中，于進程的虛擬位址空間中，指定檔案視圖的基底位址。 如果指定的位址沒有足夠的空間，則呼叫會失敗。 因此，如果您必須將檔案對應到多個進程中的相同位址，則處理常式應協商適當的位址： *lpvBase* 參數必須是系統記憶體配置細微性的整數倍數，否則呼叫會失敗。 若要取得系統的記憶體配置細微性，請使用 [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) 函數，它會填入 [**系統 \_ 資訊**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) 結構的成員。

應用程式可以從相同的檔案對應物件建立多個檔案視圖。 檔案視圖的大小可以不同于從其中衍生的檔案對應物件，但它必須小於檔案對應物件。 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile)的 *dwOffsetHigh* 和 *dwOffsetLow* 參數所指定的位移必須是系統組態細微性的倍數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在檔案中建立視圖](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
