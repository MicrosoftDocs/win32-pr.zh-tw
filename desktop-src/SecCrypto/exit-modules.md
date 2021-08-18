---
description: 當發生憑證發行之類的作業時，結束模組會接收來自伺服器引擎的通知。
ms.assetid: 5e7ee1f4-7e07-4a08-8e72-89b449804bc2
title: 結束模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38ba8d821900ece1a4ce3eb3fcb2cc805d87274b451a3d5c8948d1e86ebf3547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140751"
---
# <a name="exit-modules"></a>結束模組

當發生憑證發行之類的作業時，結束模組會接收來自伺服器引擎的通知。 Exit 模組會實作為 [*動態連結程式庫*](../secgloss/d-gly.md) ， (DLL) 。 結束模組的一般作業是將已完成的憑證發佈到預設的企業憑證授權單位單位結束模組 (指定的位置，例如，將使用者憑證和 [*憑證撤銷清單*](../secgloss/c-gly.md) (crl) 發佈到 Active Directory) 。 結束模組可以使用 [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) 介面與憑證服務進行通訊。 憑證服務會透過直接 COM 呼叫來與結束模組進行通訊，或者，如果模組不支援透過自動化的直接 COM 呼叫。

結束模組可查看現有的憑證屬性和擴充功能，也可能會查看要求屬性和屬性。 但是，exit 模組無法修改任何屬性。

憑證服務提供預設的結束模組，但您也可以建立自訂的結束模組來符合特殊需求。 不過，在撰寫自訂結束模組之前，請考慮使用預設的結束模組。 此外，對於企業憑證授權單位單位而言，應該一律使用預設的結束模組，即使您可以新增其他自訂的結束模組也是一樣。 如需詳細資訊，請參閱 [撰寫自訂結束模組](writing-custom-exit-modules.md)。

 

 
