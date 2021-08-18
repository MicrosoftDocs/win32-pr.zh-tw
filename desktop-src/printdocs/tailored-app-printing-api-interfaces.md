---
description: 應用程式會使用下列介面來管理列印檔案套件。
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: 列印檔案套件 API 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc37fa31cbda1be6927cbb24bf4b5707d10d9f2d74ed152ef630a2ad6ed588c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470120"
---
# <a name="print-document-package-api-interfaces"></a>列印檔案套件 API 介面

應用程式會使用下列介面來管理列印檔案套件。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                       | 描述                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDocumentPackageStatusEvent**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | 代表列印工作的進度。<br/>                                                                                                                                                                        |
| [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | 可讓使用者列舉支援的封裝目標型別，並使用指定的類型識別碼建立一個。 **IPrintDocumentPackageTarget** 也支援追蹤封裝列印進度和取消。<br/> |
| [**IPrintDocumentPackageTargetFactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | 與 [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) 搭配使用，以啟動列印工作。<br/>                                                                                                               |



 

 

