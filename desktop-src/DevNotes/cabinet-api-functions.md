---
description: 深入瞭解：封包 API 函式
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: 封包 API 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b08234a47c84a604c78275632d88be2bcdeef68e47fd092bbf50e4d97dcf925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668352"
---
# <a name="cabinet-api-functions"></a>封包 API 函式

本節說明下列封包 API 函式：

## <a name="fci-functions"></a>FCI 函式

FCI (檔案壓縮介面) 程式庫提供建立封包 (也稱為「CAB 檔案」 ) 的功能。 此外，程式庫還提供壓縮來減少儲存在封包中的檔案資料大小。



| 函式                                   | 描述                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | 將檔案新增至目前正在效果的封包。<br/>                                           |
| [**FCICreate**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | 建立 FCI 內容。<br/>                                                                          |
| [**FCIDestroy**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | 刪除開啟的 FCI 內容，釋放與內容相關聯的任何記憶體和暫存檔案。<br/> |
| [**FCIFlushCabinet**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | 完成目前的封包。<br/>                                                                   |
| [**FCIFlushFolder**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | 強制立即完成結構下目前的資料夾。<br/>                        |



 

## <a name="fdi-functions"></a>FDI 函式

FDI (檔案解壓縮介面) 程式庫提供從封包解壓縮檔案的功能。



| 函式                                         | 描述                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**FDICopy**](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | 從封包解壓縮檔案。<br/>                                                          |
| [**FDICreate**](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | 建立 FDI 內容。<br/>                                                                |
| [**FDIDestroy**](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | 刪除開啟的 FDI 內容。<br/>                                                           |
| [**FDIIsCabinet**](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | 判斷檔案是否為封包，如果是，則會傳回描述性資訊。<br/> |
| [**FDITruncateCabinet**](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | 從指定的資料夾編號開始截斷封包檔。<br/>                      |



 

## <a name="deprecated-functions"></a>已淘汰函式

-   [**DeleteExtractedFiles**](deleteextractedfiles.md)
-   [**DllGetVersion**](dllgetversion.md)
-   [**擷取**](extract.md)
-   [**GetDllVersion**](getdllversion.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[封包 API 參考](cabinet-api-reference.md)
</dt> <dt>

[使用封包 API](using-the-cabinet-api.md)
</dt> </dl>

 

 




