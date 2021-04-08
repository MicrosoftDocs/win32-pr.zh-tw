---
title: NDF 介面
description: 下列介面可以用來擴充識別為可延伸的 Microsoft Helper 類別的功能。
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020721"
---
# <a name="ndf-interfaces"></a>NDF 介面

下列介面可以用來擴充識別為可延伸的 Microsoft Helper 類別的功能。 雖然大部分的應用程式都不需要這項功能，但在某些情況下，它可以提供更具體的診斷和解決方式。

> [!Note]  
> 這些介面及其相關聯的方法適用于執行自己的協力廠商協助程式類別的程式開發人員，以擴充 NDF 功能。

 



| 介面名稱                                                 | 描述                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | 由 NDF 針對診斷期間發生的大部分活動呼叫。                                                     |
| [**INetDiagHelperEx**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | 由 NDF 呼叫來捕捉和提供與網路相關問題之診斷和解決的相關資訊。 |
| [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | 由 NDF 呼叫以驗證它有必要的資訊                                                           |
| [**INetDiagHelperUtilFactory**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | 保留供系統使用。                                                                                                 |



 

 

 




