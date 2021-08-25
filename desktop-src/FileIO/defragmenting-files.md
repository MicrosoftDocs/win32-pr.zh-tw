---
description: 磁碟重組是指將檔案的部分移到磁片上以重組檔案的程式，也就是在磁片上移動檔案叢集以使其成為連續的進程。
ms.assetid: 27ccaab7-ec89-489b-80dc-df9beb7969bc
title: 磁碟重組檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f04c0a3c961854b7e3ecab50d67db608178393113ca259b916db9623058e2f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696288"
---
# <a name="defragmenting-files"></a>磁碟重組檔案

當檔案寫入磁片時，有時檔案無法寫入連續的叢集中。 非連續的叢集會減緩讀取和寫入檔案的程式。 這是不連續叢集的磁片上的進一步的，這是因為移動硬碟的讀取/寫入標頭所需的時間，所以問題越糟。 具有非連續叢集的檔案會 *分散*。 為了將檔案優化以進行快速存取，磁片區可進行磁碟重組。

*磁碟重組* 是指將檔案的部分移到磁片上以重組檔案的程式，也就是在磁片上移動檔案叢集以使其成為連續的進程。 如需詳細資訊，請參閱下列各節：

-   [磁碟重組檔案](#defragmenting-a-file)
-   [將磁碟重組與陰影複製之間的互動降至最低](#minimizing-interactions-between-defragmentation-and-shadow-copies)
-   [支援磁碟重組的檔案、資料流程和資料流程類型](#files-streams-and-stream-types-supported-for-defragmentation)

## <a name="defragmenting-a-file"></a>磁碟重組檔案

在簡單的單一工作作業系統中，重組軟體是唯一的工作，而且沒有其他進程可讀取或寫入磁片。 不過，在多工作業系統中，某些進程可以讀取和寫入硬碟，而另一個進程則會將該硬碟的磁片磁碟機進行磁碟重組。 秘訣是避免寫入正在進行磁碟重組的檔案，而不需要停止撰寫程式很長的時間。 解決這個問題並不容易，但還是有可能發生。

若要允許重組而不需要詳細瞭解檔案系統磁片結構，則會提供一組三個控制項代碼。 控制碼提供下列功能：

-   讓應用程式找出空的叢集
-   判斷檔案叢集的磁片位置
-   移動磁片上的叢集

控制程式代碼也會以透明的方式處理抑制的問題，並允許其他進程在移動期間讀取和寫入檔案。

您可以執行這些作業，而不需要抑制其他進程執行。 不過，當磁片磁碟機正在進行磁碟重組時，其他進程會有較慢的回應時間。

**重組檔案**

1.  使用 [**FSCTL \_ 取得磁片 \_ 區 \_ 點陣圖**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap) 控制項程式碼，找出磁片區上夠大的位置，以接受整個檔案。
    > [!Note]  
    > 必要時，請將其他檔案移至夠大的位置。 在理想的情況下，在檔案的第一個範圍之後，您可以將後續範圍移到第一個範圍之後的空間中，有足夠的未配置叢集。

     

2.  使用 [**FSCTL \_ get 抓取 \_ \_ 指標**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) 控制項程式碼，取得磁片上檔案目前配置的對應。
3.  逐步解說 [**FSCTL \_ GET 抓取 \_ \_ 指標**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers)所傳回的抓取 [**\_ 指標 \_ 緩衝區**](/windows/desktop/api/WinIoCtl/ns-winioctl-retrieval_pointers_buffer)結構。
4.  當您逐步執行結構時，請使用 [**FSCTL \_ move \_ FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) control 程式碼來移動每個叢集。
    > [!Note]  
    > 當其他進程寫入磁片時，您可能需要在不同的時間更新點陣圖或抓取結構。

     

重組程式中使用的兩個作業需要磁片區的控制碼。 只有系統管理員可以取得磁片區的控制碼，因此只有系統管理員可以重組磁片區。 應用程式應該檢查嘗試執行磁碟重組軟體之使用者的許可權，如果使用者沒有適當的許可權，就不應該允許使用者重組磁片區。

當您在 FAT 或 FAT32 檔案系統磁片區的磁碟重組期間使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 來開啟目錄時，請指定 **一般 \_ 讀取** 存取遮罩值。 請勿指定 **\_ 允許** 的存取遮罩值上限。 如果已完成，就會拒絕存取目錄。

請勿嘗試在 NTFS 檔案系統中移動延伸超過叢集舍入檔案大小的已配置叢集，因為結果會是錯誤。

您可以針對 NTFS 檔案系統磁片區中的重新剖析點、點陣圖和屬性清單進行磁碟重組、開啟以供讀取和同步處理，以及使用 *file*：*name*：*type* 語法來命名。例如， *dirname*： $i 30： $INDEX \_ 配置、 *mrp*：： $DATA、 *mrp*：： $REPARSE \_ 點和 *mrp*：： $ATTRIBUTE \_ 清單。

對 NTFS 檔案系統磁片區進行磁碟重組時，允許重組超過檔案配置大小的虛擬叢集。

## <a name="minimizing-interactions-between-defragmentation-and-shadow-copies"></a>將磁碟重組與陰影複製之間的互動降至最低

可能的話，請以 16 kb 的 (KB) 遞增方式，在彼此相對的區塊中移動資料。 這可在啟用陰影複製時減少複製時的額外負荷，因為陰影複製空間會增加，而且當發生下列狀況時，效能會降低：

-   移動要求區塊大小小於或等於 16 KB。
-   移動差異不是以 16 KB 為單位遞增。

移動 delta 是來源區塊開始與目標區塊開頭之間的位元組數目。 換句話說，如果 X 減 Y 的絕對值是 16 KB 的倍數，則從位移 X 開始 (磁片) 的區塊可以移至起始位移 Y。 因此，假設有 4 KB 的叢集，從叢集3移至叢集27的動作將會優化，但從叢集18移至叢集24則不會。 請注意，mod (3，4) = 3 = mod (27，4) 。 因為 4 KB 的四個叢集都相當於 16 KB，所以選擇了 Mod 4。 因此，格式化為 16 KB 叢集大小的磁片區會導致所有的移動檔案都經過優化。

如需陰影複製的詳細資訊，請參閱 [磁碟區陰影複製服務](/windows/desktop/VSS/about-the-volume-shadow-copy-service)。

## <a name="files-streams-and-stream-types-supported-for-defragmentation"></a>支援磁碟重組的檔案、資料流程和資料流程類型

雖然大部分的檔案都可以使用 [**FSCTL \_ 移動 \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) 檔案控制程式代碼來移動，但並非全部都可以移動。 以下是檔案、資料流程和資料流程類型的清單 (也稱為「屬性類型代碼」（ **FSCTL \_ MOVE \_ FILE**）支援) 。 **FSCTL \_ 移動 \_** 檔案不支援其他檔案、資料流程和資料流程類型。

支援任何檔案或目錄的資料流程類型。

-   ：： $DATA
-   ：： $ATTRIBUTE \_ 清單
-   ：： $REPARSE \_ 點
-   ：： $EA
-   ：： $LOGGED \_ 公用程式 \_ 資料流程

* * Windows 7、Windows Server 2008 R2、Windows server 2008、Windows Vista、Windows Server 2003 和 Windows XP： * *：： $EA 和：： $LOGGED \_ 公用程式 \_ 串流在 Windows 8 和 Windows Server 2012 之前都不受支援

支援任何目錄的資料流程類型。

-   ：： $BITMAP
-   ：： $INDEX \_ 配置

以下是 [**FSCTL \_ MOVE \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) 檔案在 "*filename*：*streamname*： $*typename*" 格式中所支援的系統檔案、資料流程和資料流程類型。

-   $MFT：： $DATA
-   $MFT：： $ATTRIBUTE \_ 清單
-   $MFT：： $BITMAP
-   $AttrDef：： $DATA
-   $AttrDef：： $ATTRIBUTE \_ 清單
-   $Secure： $SDS： $DATA
-   $Secure：： $ATTRIBUTE \_ 清單
-   $Secure： $SDH： $INDEX \_ 配置
-   $Secure： $SDH： $BITMAP
-   $Secure： $SII： $INDEX \_ 配置
-   $Secure： $SII： $BITMAP
-   $UpCase：： $DATA
-   $UpCase：： $ATTRIBUTE \_ 清單
-   $Extend： $I 30： $INDEX \_ 配置
-   $Extend：： $ATTRIBUTE \_ 清單
-   $Extend： $I 30： $BITMAP
-   $Extend \\ $UsnJrnl： $J： $DATA
-   $Extend \\ $UsnJrnl：： $ATTRIBUTE \_ 清單
-   $Extend \\ $UsnJrnl： $Max： $DATA
-   $Extend \\ $Quota： $Q： $INDEX \_ 配置
-   $Extend \\ $Quota：： $ATTRIBUTE \_ 清單
-   $Extend \\ $Quota： $Q： $BITMAP
-   $Extend \\ $Quota： $O： $INDEX \_ 配置
-   $Extend \\ $Quota： $O： $BITMAP
-   $Extend \\ $ObjId： $O： $INDEX \_ 配置
-   $Extend \\ $ObjId：： $ATTRIBUTE \_ 清單
-   $Extend \\ $ObjId： $O： $BITMAP
-   $Extend \\ $Reparse： $R： $INDEX \_ 配置
-   $Extend \\ $Reparse：： $ATTRIBUTE \_ 清單
-   $Extend \\ $Reparse： $R： $BITMAP
-   $Extend \\ $RmMetadata： $I 30： $INDEX \_ 配置
-   $Extend \\ $RmMetadata： $I 30： $BITMAP
-   $Extend \\ $RmMetadata：： $ATTRIBUTE \_ 清單
-   $Extend \\ $RmMetadata \\ $Repair：： $DATA
-   $Extend \\ $RmMetadata \\ $Repair：： $ATTRIBUTE \_ 清單
-   $Extend \\ $RmMetadata \\ $Repair： $Config： $DATA
-   $Extend \\ $RmMetadata \\ $Txf： $I 30： $INDEX \_ 配置
-   $Extend \\ $RmMetadata \\ $Txf：： $ATTRIBUTE \_ 清單
-   $Extend \\ $RmMetadata \\ $Txf： $I 30： $BITMAP
-   $Extend \\ $RmMetadata \\ $Txf： $TXF \_ 資料： $LOGGED \_ 公用程式 \_ 資料流程
-   $Extend \\ $RmMetadata \\ $TxfLog： $I 30： $INDEX \_ 配置
-   $Extend \\ $RmMetadata \\ $TxfLog：： $ATTRIBUTE \_ 清單
-   $Extend \\ $RmMetadata \\ $TxfLog： $I 30： $BITMAP
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $Tops：： $DATA
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $Tops：： $ATTRIBUTE \_ 清單
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $Tops： $T： $DATA
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $TxfLog. blf：： $DATA
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $TxfLog. blf：： $ATTRIBUTE \_ 清單

 

 
