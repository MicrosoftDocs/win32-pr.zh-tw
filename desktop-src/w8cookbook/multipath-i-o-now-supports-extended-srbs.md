---
title: 多重路徑 i/o 現在支援延伸儲存體要求區塊
description: 多重路徑 i/o 現在支援延伸儲存體要求區塊
ms.assetid: 5373D9ED-34AF-4D66-8888-49F1EBF768F4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f558f8088b5066b51447c5f2ea23edd5154d5c10
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "104316657"
---
# <a name="multipath-io-now-supports-extended-storage-request-blocks"></a>多重路徑 i/o 現在支援延伸儲存體要求區塊

## <a name="platforms"></a>平台

**伺服器** – Windows Server 2012 

## <a name="description"></a>Description

在 Windows Server 2012 中， \_ (擴充 SRB 的儲存體要求 \_ 區塊) 會取代 \_ \_ 核心儲存體堆疊中 (舊版 SRB) 的 SCSI 要求區塊。 擴充 SRBs 會複寫舊版 SRBs 的功能，但也可延伸和擴充。

多重路徑 i/o (MPIO) 支援擴充 SRBs，並可讓裝置特定模組 (DSMs) 也可指定外延 SRB 支援。 不過，為了讓多重路徑裝置的儲存體堆疊使用擴充 SRBs， **堆疊中的所有元件都必須支援延伸 SRBs，包括 DSM**。 請注意，Microsoft 內建 DSM （即 MSDSM）支援擴充 SRBs。

SCSI 通過 \_ \_ \_ EX 結構並不是延伸的 MPIO 傳遞結構的一部分，因為擴充的 scsi pass 可以是變數大小，視命令列偵錯工具 (CDB) 而定。 相反地，擴充 MPIO 傳遞會有一個欄位，其描述從擴充 MPIO 通過結構開始到 SCSI 通過 \_ \_ \_ EX 結構的位移。 呼叫端必須確認它們配置了適當大小的緩衝區，並正確地設定 SCSI 通過。 只要呼叫端遵循擴充 SCSI 傳遞解說的規則，則應該不會有任何額外的工作可供他們使用擴充的 MPIO 傳遞。

> [!Note]  
> 如果 DSM 不支援擴充 SRBs，MPIO 將會透過具有 MPIO \_ IOCTL 旗標與 \_ \_ \_ DSM 旗標設定的要求，使擴充 mpio 傳遞失敗。

 

## <a name="manifestation"></a>表現

如果裝置的儲存體堆疊有任何部分（包括 DSM）不支援擴充 SRBs，則儲存體堆疊會還原為使用舊版 SRBs。

## <a name="solution"></a>解決方法

DSM 只有兩個 MPIO 需求可支援儲存體 \_ 要求 \_ 區塊：

-   DSM 必須將其類型報告為 DsmType6
-   DSM 必須提供支援的 DSM \_ 位址 \_ 類型 \_ 函數

如果 DSM 未回報 DsmType6 或回報 DsmType6，但未提供 DSM \_ 網址類別型支援的函式 \_ ，則 \_ MPIO 會假設 DSM 不支援外延 SRBs。

DSM \_ 位址 \_ 類型支援的 \_ 函數接受兩個參數，其中一個是網址類別型。 此網址類別型必須是 srb 中所定義的其中一個儲存體 \_ 位址 \_ 類型 \_ \* 值。 如果 DSM 支援指定的網址類別型，則必須傳回 TRUE，否則為 FALSE。 "Support" 的定義最終會由 DSM 組成。 MPIO 會使用此函式，以確保當 DSM 以 \_ 指定類型的 STOR 位址結構來取得延伸 SRB 時，將不會行為失常。 因此，當列舉多重路徑裝置時，MPIO 通常會呼叫此函式，但是可以隨時呼叫此函式。

如果 DSM 從未觸及擴充 SRB 的 STOR \_ 位址，則可以針對任何有效的儲存體 \_ 網址類別型值傳回 TRUE \_ \_ \* 。 請參閱 WDK 中的範例 DSM。

**其他重要注意事項**

-   支援延伸 SRBs 的 DSMs 必須能夠處理 SCSI \_ 要求 \_ 區塊結構和儲存體 \_ 要求 \_ 區塊結構。 由於 DSM 報告支援擴充 SRBs，並不表示它只會收到延伸的 SRBs。 除了擴充 SRBs，它可能仍會收到任何數目的舊版 SRBs，因此必須能夠同時處理這兩者。
-   我們在名為 srbhelper 的 WDK 中提供標頭檔，其中包含內嵌函式，可協助必須處理擴充和舊版 SRBs 的驅動程式。 我們的範例 DSM 會使用此標頭，讓您可以使用它作為如何使用這些函式的範例。
-   不支援擴充 SRBs 的 DSM 永遠不需要處理延伸的 SRBs。
-   當 DSM 不支援指定的儲存體位址 (類型時，MPIO 可能會導致儲存體堆疊回復舊版 SRBs， \_ \_ \_ \* 否則支援擴充的 SRBs) 。
-   "BTL8" 是 \_ \_ \_ \* 目前為 Windows Server 2012 定義的唯一儲存體網址類別型。

 

 




