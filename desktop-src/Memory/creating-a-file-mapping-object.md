---
description: 對應檔案的第一個步驟是呼叫 CreateFile 函數來開啟檔案。
ms.assetid: e00d8742-b717-419c-902c-9a286d75d8aa
title: 建立檔案對應物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550609cf9d8a052e324c585fc046472278bb428c
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524352"
---
# <a name="creating-a-file-mapping-object"></a>建立檔案對應物件

對應檔案的第一個步驟是呼叫 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數來開啟檔案。 若要確保其他進程無法寫入至對應之檔案的部分，您應該開啟具有獨佔存取權的檔案。 此外，檔案控制代碼應該保持開啟，直到進程不再需要檔案對應物件為止。 取得獨佔存取權的簡單方法是在 **CreateFile** 的 *fdwShareMode* 參數中指定零。 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函數會使用 **CreateFile** 傳回的控制碼來建立檔案對應物件。

[**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函式會傳回檔案對應物件的控制碼。 這個控制碼將在 [建立檔案視圖](creating-a-file-view.md) 時使用，以便您可以存取共用記憶體。 當您呼叫 **CreateFileMapping** 時，會指定物件名稱、要從檔案對應的位元組數目，以及對應記憶體的讀取/寫入權限。 呼叫 **CreateFileMapping** 的第一個進程會建立檔案對應物件。 針對現有物件呼叫 **CreateFileMapping** 的程式會接收現有物件的控制碼。 您可以藉由呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式來判斷是否成功呼叫 **CreateFileMapping** 建立或開啟檔案對應物件。 **GetLastError** 不會在建立處理常式中傳回 **任何 \_ 錯誤** ，而且後續進程中 **\_ 已 \_ 有錯誤** 。

如果存取旗標與 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)函式開啟檔案時所指定的 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函式發生衝突，則此函數會失敗。 例如，若要讀取和寫入檔案：

-   在 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)的 *fdwAccess* 參數中，指定 **泛型 \_ 讀取** 和 **一般 \_ 寫入** 值。
-   在 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)的 *fdwProtect* 參數中指定 **PAGE \_ READWRITE** 值。

建立檔案對應物件不會認可實體記憶體，只會保留它。

## <a name="file-mapping-size"></a>檔案對應大小

檔案對應物件的大小與所對應之檔案的大小無關。 但是，如果檔案對應物件大於檔案，則系統會在 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) 傳回之前展開檔案。 如果檔案對應物件小於檔案，則系統只會對應檔案中指定的位元組數目。

[**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)的 *dwMaximumSizeHigh* 和 *dwMaximumSizeLow* 參數可讓您指定要從檔案對應的位元組數目：

-   當您不想要變更檔案的大小時 (例如，將唯讀檔案對應) 時，請呼叫 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) 並為 *dwMaximumSizeHigh* 和 *dwMaximumSizeLow* 指定零。 這樣做會建立與檔案大小完全相同的檔案對應物件。 否則，您必須計算或預估已完成檔案的大小，因為檔案對應物件的大小為靜態;一旦建立之後，就無法增加或減少其大小。 以這種方式對應長度為零的檔案會失敗，並出現錯誤檔案 **\_ \_ 無效** 的錯誤代碼。 程式應測試長度為零的檔案，並拒絕這類檔案。

-   受命名檔案支援的檔案對應物件大小受限於磁碟空間。 檔案視圖的大小受限於未保留虛擬記憶體的最大可用連續區塊。 最多 2 GB 減去處理程式已保留的虛擬記憶體。

您所選取的檔案對應物件大小，可控制您可以使用記憶體對應來「查看」檔案的距離。 如果您建立大小為 500 Kb 的檔案對應物件，則不論檔案的大小為何，您都只能存取檔案的第一個 500 Kb。 由於不會產生任何系統資源的成本來建立較大的檔案對應物件，因此請建立檔案大小的檔案對應物件， (將 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)的 *dwMaximumSizeHigh* 和 *dwMaximumSizeLow* 參數設定為零) ，即使您不想要查看整個檔案也一樣。 系統資源中的成本是建立視圖並加以存取。

您可以在檔案開頭處，查看不是從檔案開頭開始的部分檔案。 如需詳細資訊，請參閱 [在檔案中建立視圖](creating-a-view-within-a-file.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>
  
[建立檔案視圖](creating-a-file-view.md)
</dt> <dt>

[在檔案中建立視圖](creating-a-view-within-a-file.md)
</dt> </dl>


 
