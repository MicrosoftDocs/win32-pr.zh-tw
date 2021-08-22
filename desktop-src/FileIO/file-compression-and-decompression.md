---
description: NTFS 檔案系統使用 Lempel-Ziv 壓縮，也就是不失真的壓縮演算法。
ms.assetid: 35a9fb47-5a73-479c-8fe0-5a2b07705536
title: 檔案壓縮和解壓縮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61c19449d1bfb31dfdd6e55e8c5ffa204bda36af597c43204693c55b13254e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927798"
---
# <a name="file-compression-and-decompression"></a>檔案壓縮和解壓縮

NTFS 檔案系統磁片區支援以個別檔案為基礎來壓縮檔案。 NTFS 檔案系統所使用的檔案壓縮演算法 Lempel-Ziv 壓縮。 這是不失真的壓縮演算法，這 *表示壓縮和* 解壓縮檔案時，不會遺失任何資料，而是在每次發生資料壓縮和解壓縮時遺失資料的 *失真壓縮演算法*（例如 JPEG）。

資料壓縮會將多餘的資料降到最低，以縮減檔案的大小。 在文字檔中，重複的資料可能是經常發生的字元，例如空白字元或一般母音，例如字母 e 和 a;它也可以是經常發生的字元字串。 資料壓縮會藉由將此多餘資料降到最低，來建立檔案的壓縮版本。

每種類型的資料壓縮演算法會以獨特的方式將多餘的資料降到最低。 例如， *Huffman 編碼演算法* 會根據這些字元的出現頻率，將程式碼指派給檔案中的字元。 另一個壓縮演算法（稱為「 *執行長度編碼*」）會針對重複字元產生兩個部分的值：第一個部分會指定重複字元的次數，而第二個部分則會識別該字元。 另一個壓縮演算法（也稱為 *Lempel-ziv lempel-ziv 演算法*）會將可變長度的字串轉換成固定長度的程式碼，此程式碼耗用的空間比原始字串少。

## <a name="the-ntfs-file-system-file-compression"></a>NTFS 檔案系統檔案壓縮

在 NTFS 檔案系統上，壓縮會以透明的方式執行。 這表示可以使用它，而不需要變更現有的應用程式。 應用程式無法存取檔案的壓縮位元組;他們只會看到未壓縮的資料。 因此，開啟壓縮檔案的應用程式可以像是未壓縮的一樣運作。 不過，這些檔案無法複製到另一個檔案系統。

如果您壓縮超過 30 gb 的檔案，壓縮可能不會成功。

下列主題會識別 NTFS 檔案系統檔案壓縮：

-   [壓縮屬性](compression-attribute.md)
-   [壓縮狀態](compression-state.md)
-   [取得壓縮檔案的大小](obtaining-the-size-of-a-compressed-file.md)

## <a name="file-compression-and-decompression-libraries"></a>檔案壓縮和解壓縮程式庫

檔案壓縮和解壓縮程式庫會取得現有的檔案或檔案，並產生原始檔案的壓縮版本檔案。 壓縮也不會失真，但應用程式不會察覺壓縮。 應用程式只能使用檔案壓縮程式庫的協助來操作這類檔案。 此外，您可以在這類檔案上執行的唯一作業是從原始的檔案建立壓縮檔案，並從解壓縮的版本復原原始資料。 通常不支援編輯，如果完全支援，則搜尋會受到限制。

一般而言，應用程式會呼叫 Lz32.dll 中的函式，以解壓縮使用 Compress.exe 壓縮的資料。 函式也可以處理檔案，而不會嘗試將它們解壓縮。

您可以使用 Lz32.dll 中的函數，將單一或多個檔案解壓縮。 您也可以使用它們，一次將壓縮檔案解壓縮到一個部分。

下列主題會識別 Lz32.dll 中的函式所提供的檔案解壓縮功能：

-   [解壓縮單一檔案](decompressing-a-single-file.md)
-   [解壓縮多個檔案](decompressing-multiple-files.md)
-   [從壓縮檔案讀取](reading-from-compressed-files.md)

## <a name="cabinets"></a>櫃

Cab 是由支援磁片跨越和多檔案壓縮等功能的壓縮程式庫所建立。 如需其他資訊，請參閱「封包軟體發展工具組：」 [https://msdn.microsoft.com/library/dncabsdk/html/cabdl.asp](/previous-versions/ms974336(v=msdn.10)) 。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                             | 描述                                                                                                                              |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [壓縮屬性](compression-attribute.md)<br/>                                     | 在 NTFS 檔案系統磁片區上，每個檔案和目錄都有一個 *壓縮屬性*。<br/>                                         |
| [壓縮狀態](compression-state.md)<br/>                                             | 磁片區上的每個檔案和目錄都支援個別檔案和目錄的壓縮，都有 *壓縮狀態*。<br/> |
| [取得壓縮檔案的大小](obtaining-the-size-of-a-compressed-file.md)<br/> | 若要取得壓縮的檔案大小，請使用 GetCompressedFileSize 函數。<br/>                                               |
| [解壓縮單一檔案](decompressing-a-single-file.md)<br/>                         | 應用程式可以使用 LZOpenFile、LZCopy 和 LZClose 函式來解壓縮單一壓縮檔案。<br/>                |
| [解壓縮多個檔案](decompressing-multiple-files.md)<br/>                       | 應用程式可以使用 LZOpenFile、LZCopy 和 LZClose 函式，將多個檔案解壓縮。<br/>                          |
| [從壓縮檔案讀取](reading-from-compressed-files.md)<br/>                     | 應用程式可以使用 LZSeek 和 LZRead 函數，一次將壓縮檔案解壓縮。<br/>                 |



 

 

