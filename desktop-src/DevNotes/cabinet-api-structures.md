---
description: 深入瞭解：封包 API 結構
ms.assetid: b6d636e6-2af0-427c-a529-56c80b349b58
title: 封包 API 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6acae2a62d59353e10eb07e0e3f25e763b69eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025894"
---
# <a name="cabinet-api-structures"></a>封包 API 結構

本節詳細說明下列封包 API 結構：



| 結構                                              | Description                                                                                     |
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

 

 
