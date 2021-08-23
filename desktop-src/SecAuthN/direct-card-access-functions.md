---
description: 您可以使用智慧卡子系統，與可能不符合 ISO 7816 規格的卡片進行通訊。
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: 直接存取卡的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72b606cd766ea9a8930599bd2a44e117dea0bffdef6474c038b39294c08acf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008456"
---
# <a name="direct-card-access-functions"></a>直接存取卡的功能

您可以使用 [*智慧卡*](/windows/desktop/SecGloss/s-gly) 子系統，與可能不符合 ISO 7816 規格的卡片進行通訊。 若要這樣做，下列函式可讓您藉由提供 [*讀取器*](/windows/desktop/SecGloss/r-gly)的直接、低層級操作，來控制應用程式與卡片之間通訊的屬性。

若要使用這些函式，您必須提供有問題的屬性識別碼。 如需有效的屬性識別碼和值，請參閱表格3-1 中 *PC-Connected 介面裝置的需求*。



| 主題                                    | 描述                           |
|------------------------------------------|---------------------------------------|
| [**SCardControl**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | 提供讀取器的直接控制權。 |
| [**SCardGetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | 取得讀取器屬性。                |
| [**SCardSetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | 設定讀取器屬性。                 |



 

 

 
