---
description: 區塊複製作業會指示檔案系統代表應用程式複製某範圍的檔案位元組。
ms.assetid: E18E8D79-3985-40B8-A4C5-A73A21E5C527
title: 封鎖複製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33aa1c1eee693b6ed4b502aedc6da6176ece3e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514000"
---
# <a name="block-cloning"></a>封鎖複製

*區塊複製* 作業會指示檔案系統代表應用程式複製某範圍的檔案位元組。 目的地檔案可能與來源檔案相同或不同。

檔案系統會管理叢集 [和延伸區](clusters-and-extents.md)的對應，而且可以藉由將虛擬叢集編號 (VCN) 變更為邏輯叢集號碼， (LCN) 對應作為低成本的中繼資料作業，而不是讀取和寫入基礎檔案資料，來執行複製。 這可讓複本以較快的速度完成，並產生較少的 i/o 給基礎儲存體。 此外，多個檔案現在可能會在區塊複製後共用邏輯叢集，而不會在磁片上多次儲存相同的叢集來節省容量。

區塊複製作業不會中斷檔案之間提供的隔離。 在區塊複製完成之後，寫入來源檔案的作業不會出現在目的地中，反之亦然。

區塊複製僅適用于從 Windows Server 2016 開始的 [ReFS 檔案系統](/windows/desktop/w8cookbook/resilient-file-system--refs-) 類型。

## <a name="block-cloning-on-refs"></a>在 ReFS 上進行區塊複製

Windows Server 2016 上的 ReFS 會藉由將邏輯叢集 (也就是磁片區上的實體位置) 從來源區域到目的地區域，來實行區塊複製。 然後，它會使用以配置為依據的寫入機制，以確保這些區域之間的隔離。 來源和目的地區域可以位於相同或不同的檔案中。

此執行需要將開始和結束檔案位移對齊叢集界限。 在 Windows Server 2016 的 ReFS 中，叢集預設的大小為 4 KB，但可以選擇性地設定為64KB。 叢集大小是以格式時間設定的全磁片區參數。

## <a name="restrictions-and-remarks"></a>限制和備註

-   來源和目的地區域必須在叢集界限的開頭和結尾。
-   複製的區域長度必須小於 4GB。
-   目的地區域不得延伸超過檔案結尾。 如果應用程式想要使用複製的資料來擴充目的地，它必須先呼叫 [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)。
-   若來源與目的地區域位於相同檔案，其不得重疊。  (應用程式可以將區塊複製作業分割成多個不再重迭的區塊複製，以繼續進行。 ) 
-   來源與目的檔案必須位於相同的 ReFS 磁碟區。
-   來源和目的地檔案必須有相同的 [**完整性資料流程**](file-attribute-constants.md) 設定 (也就是說，必須在這兩個檔案中啟用完整性資料流程，或是在兩個檔案) 中都停用。
-   若來源檔案為疏鬆，目的檔案也必須為疏鬆。
-   區塊複製作業會中斷共用的隨機鎖定 (也稱為 [層級 2](types-of-opportunistic-locks.md) 的隨機鎖定) 。
-   ReFS 磁片區必須已格式化為 Windows Server 2016，如果 Windows 容錯移轉叢集正在使用中，則叢集功能等級必須是 Windows Server 2016 或更新版本（格式時間）。

## <a name="example"></a>範例

假設我們有兩個檔案 X 和 Y，其中每個檔案都是由三個不同的區域所組成。 每個檔案區域都儲存在磁片區的不同區域。 檔案系統會儲存每一個檔案區域中所參考的每個磁片區區域的知識：

![複製前](images/before-clone.png)

現在假設應用程式會從檔案 X （在檔案區域 A 和 B）對檔案 Y 發出區塊複製作業，該作業是在 E 目前為的位移處的檔案 Y。 將會產生下列檔案系統狀態：

![複製後](images/after-clone.png)

區域 A 和 B 中的資料實際上是從檔案 X 複製到檔案 Y （藉由將 VCN 變更為 ReFS 磁片區內的 LCN 對應）。 磁片區支援區域 A 和 B 未讀取，也不是支援在作業期間覆寫舊區域 E 和 F 的磁片區。

檔案 X 和 Y 現在會在磁片上共用邏輯群集。 這會反映在資料表所顯示的參考計數中。 共用會導致磁片區容量耗用量較低，因為基礎磁片區上的區域 A 和 B 已複製。

現在，假設應用程式會覆寫檔案 X 中的區域 A。 ReFS 會產生重複的複本，現在我們將會呼叫 g.，然後將 G 對應到檔案 X，並套用修改。 如此可確保維持檔案間的隔離。 參考計數會適當地更新：

![修改寫入之後](images/after-modifying-write.png)

修改寫入之後，區域 B 仍會在磁片上共用。 注意，若區域 A 大於叢集，便僅會複製修改的叢集，且剩餘的部分會維持為共用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**重複的 \_ 延伸區 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-duplicate_extents_data)
</dt> <dt>

[**\_將重複 \_ 的範圍 FSCTL \_ 至 \_ 檔案**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)
</dt> </dl>

 

 
