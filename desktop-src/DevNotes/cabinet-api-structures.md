---
description: 深入瞭解：封包 API 結構
ms.assetid: b6d636e6-2af0-427c-a529-56c80b349b58
title: 封包 API 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281e131d2a94f58cad15210ace0fa5f189e132bfb274c98b13d374b99baff9da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668276"
---
# <a name="cabinet-api-structures"></a>封包 API 結構

本節詳細說明下列封包 API 結構：



| 結構                                              | 描述                                                                                     |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) | 包含 Cabinet.dll 的版本資訊。<br/>                                    |
| [**CCAB**](/windows/desktop/api/Fci/ns-fci-ccab)                                   | 包含封包資訊。<br/>                                                        |
| [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)                                     | 從 FCI/FDI 傳回錯誤資訊。 呼叫端不應該修改此結構。<br/> |
| [**FDICABINETINFO**](/windows/desktop/api/Fdi/ns-fdi-fdicabinetinfo)               | 包含特定封包檔的詳細資料。<br/>                                    |
| [**FDINOTIFICATION**](/windows/desktop/api/Fdi/ns-fdi-fdinotification)             | 提供資訊給 [**FNFDINOTIFY**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify)。<br/>                           |
| [**會話**](session.md)                             | 包含目前會話的相關資訊。<br/>                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[封包 API 參考](cabinet-api-reference.md)
</dt> <dt>

[使用封包 API](using-the-cabinet-api.md)
</dt> </dl>

 

 
