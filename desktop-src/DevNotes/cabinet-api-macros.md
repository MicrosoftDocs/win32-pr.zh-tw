---
description: 深入瞭解：封包 API 宏
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: 封包 API 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510378"
---
# <a name="cabinet-api-macros"></a>封包 API 宏

本節將詳細說明 Cabinet API 所使用的宏：

## <a name="fci-macros"></a>FCI 宏

FCI 會使用下列宏：



| 巨集                                              | Description                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**FNFCIALLOC**](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | 用來在 FCI 內容中配置記憶體。<br/>                                          |
| [**FNFCICLOSE**](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | 用來關閉檔案。<br/>                                                               |
| [**FNFCIDELETE**](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | 用來刪除檔案。<br/>                                                              |
| [**FNFCIFILEPLACED**](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | 用來在檔案放入封包時通知。<br/>                                |
| [**FNFCIFREE**](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | 用來釋放先前在 FCI 內容中配置的記憶體。<br/>                         |
| [**FNFCIGETNEXTCABINET**](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | 用來要求下一個封包的資訊。<br/>                                   |
| [**FNFCIGETOPENINFO**](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | 用來開啟檔案並取出檔案日期、時間和屬性。<br/>                   |
| [**FNFCIGETTEMPFILE**](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | 用來取得暫存檔案名稱。<br/>                                               |
| [**FNFCIOPEN**](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | 用來在 FCI 內容中開啟檔案。<br/>                                              |
| [**FNFCIREAD**](/windows/desktop/api/fci/nf-fci-fnfciread)                     | 用來從檔案讀取資料。<br/>                                                      |
| [**FNFCISEEK**](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | 用來將檔案指標移至指定的位置。<br/>                                |
| [**FNFCISTATUS**](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | 用來更新使用者。<br/>                                                            |
| [**FNFCIWRITE**](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | 用來將資料寫入檔案。<br/>                                                       |
| [**TCOMPfromLZXWindow**](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | 將 windows 大小轉換成 [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)的 LXZ TCOMP 值。<br/> |



 

## <a name="fdi-macros"></a>FDI 宏

FDI 會使用下列宏：



| 巨集                              | Description                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**FNALLOC**](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | 用來在 FDI 內容中配置記憶體。<br/>                               |
| [**FNCLOSE**](/windows/desktop/api/fdi/nf-fdi-fnclose)         | 用來關閉 FDI 內容中的檔案。<br/>                                  |
| [**FNFDINOTIFY**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | 用來更新解碼器狀態的應用程式。<br/>             |
| [**FNFREE**](/windows/desktop/api/fdi/nf-fdi-fnfree)           | 用來釋放先前在 FDI 內容中配置的記憶體。<br/>              |
| [**FNOPEN**](/windows/desktop/api/fdi/nf-fdi-fnopen)           | 用來在 FDI 內容中開啟檔案。<br/>                                   |
| [**FNREAD**](/windows/desktop/api/fdi/nf-fdi-fnread)           | 用來從 FDI 內容中的檔案讀取資料。<br/>                         |
| [**FNSEEK**](/windows/desktop/api/fdi/nf-fdi-fnseek)           | 用來將檔案指標移至 FDI 內容中的指定位置。<br/> |
| [**FNWRITE**](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | 用來將資料寫入 FDI 內容中的檔案。<br/>                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[封包 API 參考](cabinet-api-reference.md)
</dt> <dt>

[使用封包 API](using-the-cabinet-api.md)
</dt> </dl>

 

 




