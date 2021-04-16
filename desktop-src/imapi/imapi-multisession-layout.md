---
title: IMAPI.EXE 多會話配置
description: IMAPI.EXE 讓應用程式開發人員能夠建立 ISO 9660 和 UDF 檔案系統映射，並將它們燒錄到 CD、DVD 和 Blu-Ray \ 8482;光學媒體。
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2581672fac78d23a0d2f4e2bc36ee4227adbca1d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104566163"
---
# <a name="imapi-multisession-layout"></a>IMAPI.EXE 多會話配置

IMAPI.EXE 讓應用程式開發人員能夠建立 ISO 9660 和 UDF 檔案系統映射，並將它們燒錄到 CD、DVD 和藍光™光學媒體上。 在 Windows 7 中，IMAPI.EXE 提供對 DVD 和藍光™可讀寫媒體上的多會話燒錄的額外支援。

下列檔詳細說明 IMAPI.EXE 利用來執行多會話的光碟版面配置。 這項資訊應該用來確保 IMAPI.EXE 與其他燒錄軟體之間的互通性，以及允許此軟體的開發人員建立與 IMAPI.EXE 相容的多會話光碟映射。

> [!Note]  
> 如需詳細說明如何建立多個多會話光碟的範例，請參閱 [建立多會話光碟](creating-a-multisession-disc.md)。

 

## <a name="multisession-on-sequential-media"></a>連續媒體上的多會話

連續媒體上的多會話的 IMAPI.EXE 執行支援與 CD-R、CD-RW、DVD-R、DVD + R 和藍光™媒體搭配使用。 IMAPI.EXE 會使用一次會話記錄模式進行 CD-RW，因此在此案例中，格式會視為連續的媒體類型。

在使用 UDF 的連續媒體的多重會話案例中，IMAPI.EXE 會寫出錨點結構 (UDF 錨點磁片區描述元指標-AVDP) 、磁片區結構 (UDF 磁片區描述項順序-VDS) ，以及檔案系統元資料結構 (UDF 檔案集描述項-FSD) 在每個新會話開始時，如下圖所述：

![顯示具有「匯入/F S 掛接點」的檔案系統元資料結構的圖表，其在實體會話2的「錨點」以紅色箭號表示。](images/multises1.png)

> [!Note]  
> 此圖說明使用 UDF 2.50 搭配重複中繼資料時的 IMAPI.EXE 光碟版面配置。

 

依序錄製的媒體上儲存的資料是由一些實體會話所組成。 每個會話都包含一個完整的檔案系統，將使用者資料表示為一組以目錄組織的檔案。 檔案系統中繼資料包含許多階層式組織的資料結構。 階層的頂端會有錨點結構 (AVDP) 位於預先定義的邏輯區塊位址 (LBAs) 。 錨點結構會指定沒有預先定義之位址的下一個層級結構的位置。 錨點結構之後的下一個階層層級包含磁片區結構 (VDS) 描述磁片區的屬性，並參考檔案系統元資料結構 (FSD) ，進而描述個別的檔案和目錄。

## <a name="multisession-on-rewritable-media"></a>可讀寫媒體上的多會話

上一節所述之順序媒體的方法與可讀寫 (非順序) 媒體不相容。 這些媒體格式包括 DVD-ROM、DVD + RW、DVD RAM、藍光™可讀寫，以及其他隨機寫入媒體，例如 Iomega REV 磁片。 可讀寫媒體不支援對應至邏輯會話的實體會話概念，也就是由主控應用程式所認可的個別增量。 只會公開單一實體會話，這是從光碟開頭開始的區域，代表可能包含多個邏輯會話的整個可定址區域。

> [!Note]  
> 雖然 CD-RW 是在連續模式下支援實體會話的概念，但 IMAPI.EXE 目前並不支援這項功能。

 

為了因應可讀寫格式的實體和邏輯會話之間缺乏一對一的對應，IMAPI.EXE 選擇性地更新 *第一個* 邏輯會話中的錨定結構 (AVDP) ，以指向 *最後一個* 邏輯會話的新磁片區結構 (VDS) 和檔案系統元資料結構 (FSD) ，如下圖所述：

![此圖顯示具有「匯入/F S 掛接點」的檔案系統元資料結構，並在邏輯會話1的「錨點」處以紅色箭號表示。](images/multises2.png)

> [!Note]  
> 此圖說明使用 UDF 2.50 搭配重複中繼資料時的 IMAPI.EXE 光碟版面配置。

 

將新的邏輯會話新增到可讀寫光碟時，IMAPI.EXE 會先分析磁片區中繼資料 (VDS) ，判斷最後一個邏輯會話的結尾。 然後，IMAPI.EXE 會新增邏輯會話、完成新的錨點 (AVDP) 、磁片區 (VDS) 以及檔案系統元資料結構 (FSD) ，與先前錄製的邏輯會話實際上是連續的。 最後一個步驟需要更新第一個邏輯會話開頭的錨定結構 (AVDP) ，以指向 *新* 邏輯會話中 (VDS) 的磁片區結構。 操作結果與順序媒體相同。

## <a name="additional-recommendations"></a>其他建議

-   **分割區版面配置**

    為了達成 IMAPI.EXE 的相容性，建議協力廠商的燒錄軟體發展人員使用本檔中所述的光碟版面配置。 開發人員應避免配置檔案系統分割區佔用整個光碟，因為這需要記錄應用程式，以便在需要將資料附加到光碟時，找出現有磁碟分割內的可用空間。記錄應用程式通常會利用光碟上的專屬標記來完成這項作業，以指出使用者資料實際佔用多少空間。 這類光碟版面配置與 IMAPI.EXE 不相容，因為無法在建立專屬標記的應用程式之外辨識這些標記。

-   **UDF 磁碟分割類型**

    IMAPI.EXE 會在可寫入的媒體上，使用 **唯讀** UDF 磁碟分割類型來執行多會話。 協力廠商燒錄軟體的開發人員應該使用 **唯讀** UDF 磁碟分割類型，透過 Imapi.exe 達成 Windows 主要燒錄的相容性。 如果使用另一個 UDF 分割類型，例如可重 **寫** ，則 imapi.exe 無法提供主控支援。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立多會話光碟](creating-a-multisession-disc.md)
</dt> <dt>

[**IMultisessionRandomWrite**](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




