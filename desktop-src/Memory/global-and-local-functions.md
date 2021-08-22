---
description: 支援從16位程式碼移植的全域和區域函式，或維持與16位 Windows 的原始程式碼相容性。
ms.assetid: 97707ce7-4c65-4d0e-ba69-47fdaee73a9b
title: 全域和區域函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d7832f90a420e6be87fe6599cc8c9e4722ddf45b789663ed9b39eab4e5449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869690"
---
# <a name="global-and-local-functions"></a>全域和區域函數

支援從16位程式碼移植的全域和區域函式，或維持與16位 Windows 的原始程式碼相容性。 從32位 Windows 開始，全域和區域函式會實作為包裝函式，以使用進程預設堆積的控制碼來呼叫對應的[堆積函數](heap-functions.md)。 因此，全域和區域函數的額外負荷會比其他記憶體管理函數更大。

[堆積](heap-functions.md)函式提供的功能和控制與全域和區域函式不同。 新的應用程式應該使用堆積函式，除非檔特別指出應該使用全域或區域函數。 例如，某些 Windows 函式會配置必須使用 [**>localfree**](/windows/desktop/api/WinBase/nf-winbase-localfree)釋放的記憶體，而全域函式仍會搭配動態資料交換 (DDE) 、剪貼簿函式和 OLE 資料物件使用。 如需全域和區域函數的完整清單，請參閱 [記憶體管理函數](memory-management-functions.md)中的資料表。

Windows 的記憶體管理不提供個別的本機堆積和全域堆積，因為16位 Windows。 因此，全域和區域系列的函式是相等的，而在它們之間選擇則是個人喜好設定。 請注意，從16位分割的記憶體模型到32位虛擬記憶體模型的變更，已使某些相關的全域和區域函數和其選項不需要或無意義。 例如，因為本機和全域配置都會傳回32位虛擬位址，所以不會再有接近或遠的指標。

[**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)和 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)所配置的記憶體物件位於私用、已認可的頁面，其具有無法由其他進程存取的讀取/寫入存取權。 使用 **GlobalAlloc** 搭配 **GMEM \_ DDESHARE** 所配置的記憶體，實際上並不是全域共用的，因為它是在16位 Windows 中。 此值沒有任何作用，而且僅適用于相容性。 針對其他用途需要共用記憶體的應用程式必須使用檔案對應物件。 多個進程可以對應相同檔案對應物件的視圖，以提供命名的共用記憶體。 如需詳細資訊，請參閱檔案 [對應](file-mapping.md)。

記憶體配置只受限於可用的實體記憶體，包括磁片上分頁檔案中的儲存體。 當您配置固定的記憶體時， [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) 和 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) 會傳回呼叫進程可以立即用來存取記憶體的指標。 當您配置可移動記憶體時，傳回值為控制碼。 若要取得可移動記憶體物件的指標，請使用 [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock) 和 [**LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) 函數。

所配置記憶體的實際大小可能會大於所要求的大小。 若要判斷配置的實際位元組數目，請使用 [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize) 或 [**LocalSize**](/windows/desktop/api/WinBase/nf-winbase-localsize) 函數。 如果配置的數量大於所要求的數量，則處理常式可以使用整個數量。

[**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)和 [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc)函式會變更 [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)和 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)所配置之記憶體物件的大小或屬性。 大小可能會增加或減少。

[**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree)和 [**>localfree**](/windows/desktop/api/WinBase/nf-winbase-localfree)函式會釋放由 [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)、 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)、 [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)或 [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc)所配置的記憶體。 若要捨棄指定的記憶體物件而不使控制碼失效，請使用 [**GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) 或 [**LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) 函數。 **GlobalReAlloc** 或 **LocalReAlloc** 稍後可以使用此控制碼來配置與相同控制碼相關聯的新記憶體區塊。

若要傳回指定之記憶體物件的相關資訊，請使用 [**GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags) 或 [**LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) 函數。 此資訊包含物件的鎖定計數，並指出物件是否為 discardable 或已被捨棄。 若要將控制碼傳回至與指定之指標相關聯的記憶體物件，請使用 [**GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle) 或 [**LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[比較記憶體配置方法](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 
