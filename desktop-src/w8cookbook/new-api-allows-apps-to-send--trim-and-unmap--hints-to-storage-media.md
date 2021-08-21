---
title: 新的 API 可讓應用程式將「修剪和取消對應」提示傳送至存放裝置媒體
description: 新的 API 可讓應用程式傳送 \ 0034;修剪和取消對應 \ 0034;存放裝置媒體的提示
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d79d47dceb5c8bf2e7575836c9a40ddf0347b7e5c616ab4b7196b547742c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028826"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a>新的 API 可讓應用程式將「修剪和取消對應」提示傳送至存放裝置媒體

## <a name="platforms"></a>平台

**用戶端**– Windows 8  
**伺服器**– Windows Server 2012  


## <a name="description"></a>描述

TRIM 提示會通知磁片磁碟機，應用程式不再需要先前配置的某些磁區，且可以清除。 當應用程式透過檔案進行大量配置，然後自行管理檔案的配置 (例如虛擬硬碟檔案) 時，通常會使用這種方式。

**什麼是 TRIM？**

固態硬碟 (Ssd) 通常是以 flash 記憶體為基礎的區塊清除裝置;這表示當資料寫入 SSD 時，不能就地寫入，必須在其他地方寫入，直到封鎖可進行垃圾收集為止。 由於 SSD 沒有任何內部機制可判斷特定區塊已移除，而且需要其他區塊。 SSD 可將磁區標示為「已變更」的唯一時機是在過度寫入時。 在其他情況下（例如，當檔案被刪除時）會保留這些磁區，因為刪除作業會以主要檔案資料表的形式 () 只變更，而不是對檔案的所有磁區進行作業。 在 Windows 7 中，我們引進了一種標準方式來與 ssd 通訊，而不需要任何其他的磁區。 此命令會在 [T13 規格](https://www.t13.org/Standards/Default.aspx?DocumentType=3) 中定義為 TRIM 命令;NTFS 會傳送一些一般內嵌作業（例如 "deletefile"）的 TRIM 命令。

**儲存體世界中的其他修剪用途**

如同 ssd，存放區域網路 (san) 和新的 Windows 8 功能軟體空間實作為在精簡布建的環境中管理其空間的方式。 San 和軟體空間會以大於磁區或叢集的大小來配置儲存體的區域， (從1MB 到 1GB) 的任何位置。 當它們收到配置大小的 TRIM 提示 (或大於配置大小) 時，SAN/SSD 可以取消配置區域以釋出其他檔案的空間。 它們通常會將所有的 TRIM 提示傳遞給基礎媒體 (SSD 或 HDD) ，讓它們可以適當地使用釋放的空間。 它們通常不會將資料移至取消配置區域，也不會在區域是空的) 時，追蹤取消配置區域 (的修剪區域。

精簡布建的 San 會使用傳遞給它們的修剪提示，以協助降低整體實體儲存體的使用量，進而降低成本。 [T10 SCSI 規格](https://www.t10.org)會定義「取消對應」命令 (類似于 TRIM 命令) ;此命令適用于所有種類的儲存體，包括 Hdd、Ssd 和其他類型。 取消對應命令可協助移除 SAN 配置中的實體區塊。

## <a name="how-to-use-the-new-api"></a>如何使用新的 API


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



如果可能或非同步 (非緩衝) 至裝置 IOCTL DSM 命令修剪，則會透過緩衝區傳遞檔案修剪。 這會對應至適用于 ATA 裝置的 TRIM 命令和 SCSI 裝置的取消對應命令。 檔案修剪程式碼會逐一傳送區域，如同上方的範圍所指定。

檔案修剪不會等待裝置的傳回，因為 TRIM 和取消對應命令會定義為基礎儲存媒體的提示，而且不需要傳回碼。

**端對端工作流程：**

1.  呼叫檔案修剪
    1.  檔案修剪會檢查輸入的錯誤
    2.  檔案修剪將範圍細分為 LCN 區域
    3.  檔案修剪會向上和向下調整傳遞給 TRIM 的錯誤對齊區域
    4.  檔案修剪：清除快取中與修剪區域相關的專案
    5.  檔案修剪會將 IOCTL \_ DSM (TRIM) 每個區域傳遞
2.  檔案修剪傳回或錯誤
    1.  針對輸入有效性進行錯誤檢查
    2.  如果只有部分範圍有效，則會傳回完整 API 呼叫的一個錯誤

**使用案例**

**取用者虛擬硬碟 (VHD) 掛接在 SSD 上：**

VHD 一開始是在「清理」未使用的媒體上掛接。 使用 VHD 時，VHD 會取用檔案的部分儲存媒體等等。當它刪除儲存體媒體中的檔案時，不會從 SSD 移除這些檔案，因為完整的 VHD 會儲存為 SSD 上的一個檔案。 Hyper-v 環境會針對在 VHD 環境中刪除檔案時刪除的所有區域呼叫檔案修剪。 檔案 \_ 修剪會轉譯成 ssd，讓 ssd 效能可以優化。

**在精簡布建的 SAN 上掛接的取用者 VHD：**

VHD 一開始會掛接在精簡布建環境的最小值板上。 當檔案儲存在 VHD 時，VHD 的儲存空間使用量會以 slab 的倍數成長。 移除 VHD 中的檔案時，Hyper-v 會將檔案 \_ 修剪到基礎精簡布建的 SAN。 如果修剪大於樓板的資料細微性，SAN 現在可以移除一個小板，進而減少該 SAN 上的 VHD 使用量。

如果 VHD 位於 Windows 8 基礎的伺服器上，儲存體優化工具也會傳送修剪，以降低 vhd 從掛接的 vhd 內的碳足跡。

## <a name="tests"></a>測試

舊版作業系統版本中沒有任何可比較的 Api。 實際的 API 本身應該不會有任何效能影響，不過如果儲存媒體 (正確地執行，) 可能會顯示更佳的寫入效能。 應謹慎使用 API;因為這些範圍將會從儲存體媒體永久移除，所以只應將不再需要的範圍傳遞給您。

## <a name="resources"></a>資源

-   [T13 規格](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [T10 SCSI 規格](https://www.t10.org/)

 

 




