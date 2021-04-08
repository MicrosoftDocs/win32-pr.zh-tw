---
description: MSDV 驅動程式中的 DVINFO 欄位設定
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: MSDV 驅動程式中的 DVINFO 欄位設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688011"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a>MSDV 驅動程式中的 DVINFO 欄位設定

本節說明 MSDV 驅動程式如何填入 [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) 結構。

`DVINFO`結構會定義 MSDV 與其他篩選之間的 pin 連接格式區塊。 根據預設，DV 分隔器篩選器會在從 DV 裝置進行捕捉時使用，而 DV Mux 篩選器則會在傳送至裝置時使用。 不過，應用程式可能會提供自己的自訂篩選，因此瞭解 MSDV 如何填入格式區塊會很有用 `DVINFO` 。

`DVINFO`結構包含下列資訊：

-   針對第一個和第二個音訊區塊，兩個音訊輔助 (AAUX) 來源套件。
-   第一個和第二個音訊區塊的兩個 AAUX 原始檔控制套件。
-   影片輔助 (VAUX) 來源套件。
-   VAUX 原始檔控制套件。

DV 串流中的每個畫面格都包含 AAUX 和 VAUX 套件。 但是， `DVINFO` 格式區塊是靜態的，而且只會用來建立 pin 連接。 當 MSDV 驅動程式連接時，不會檢查資料流程中的任何 AAUX 或 VAUX 元件。 相反地，它會根據 DV 裝置的下列特性，使用一組預設值：

-   裝置是否支援取用者格式 (DVCR) 或專業格式 (DVCPRO) 
-   信號類型
-   格式是否為 NTSC 或 PAL。  (如果裝置未報告此資訊，MSDV 預設為 NTSC 設定) 

串流開始之後，使用者模式篩選器（例如 DV 分隔器）的責任就是檢查每個 DV 框架的實際內容。 因為資訊可以從框架變更為框架，所以篩選可能需要執行動態格式變更。 例如，如果音訊速率變更，則篩選可能需要重新協商音訊類型。

如果您捕捉型別1的 DV 檔案，此 `DVINFO` 結構會以資料流程格式寫入檔案中， ( ' strf ' ) 區塊。 這項資料會直接取自 MSDV 所提供的格式區塊。 如所述，資料流程的實際內容可能會不同。 應用程式必須負責檢查每個畫面中的 AAUX 和 VAUX 套件。

在下列主題中，您可以找到列出 MSDV 所使用之所有欄位的資料表。

-   [AAUX 來源 (作為) 套件](aaux-source--as--pack.md)
-   [AAUX 原始檔控制 (ASC) 套件](aaux-source-control--asc--pack.md)
-   [VAUX 來源 (VS) 套件](vaux-source--vs--pack.md)
-   [VAUX 原始檔控制 (VSC) 套件](vaux-source-control--vsc--pack.md)

閱讀這些資料表時，請參閱下列規格：

-   IEC 61834
-   SMPTE 314M
-   SMPTE 370

在每個資料表中，第一個資料行提供欄位碼，後面接著以括弧括住的 (位數) 。 其餘的資料行則提供域值。 許多 AAUX 和 VAUX 欄位與 pin 連接無關，在這種情況下，MSDV 會設定虛擬值。 整個套件的數值會列在每個資料表的底部。

每個資料表之後的附注會提供有關所選欄位的詳細資訊。 如需完整的說明，請參閱規格。 此外，在 SMPTE 314M/SMPTE 370 中，某些欄位的意義與 IEC 61834 中的意義不同。

> [!Note]  
> DirectShow 目前不支援 DVCPRO 格式。 針對 DVCPRO 格式所列出的值會定義為供日後使用。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 中的數位視訊](digital-video-in-directshow.md)
</dt> <dt>

[AVI 檔案格式的 DV 資料](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[MSDV 驅動程式](msdv-driver.md)
</dt> </dl>

 

 



