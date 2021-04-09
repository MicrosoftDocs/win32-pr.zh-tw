---
description: 您可以使用下列函數來處理 Visual Basic 中的效能資料。
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Visual Basic 的效能計數器函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849283"
---
# <a name="performance-counters-functions-for-visual-basic"></a>Visual Basic 的效能計數器函數

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

您可以使用下列函數來處理 Visual Basic 中的效能資料。

- [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**PdhVbAddCounter**](pdhvbaddcounter.md)
- [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
- [**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
- [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
- [**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
- [**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
- [**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
- [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md)
- [**PdhVbOpenLog**](pdhvbopenlog.md)
- [**PdhVbOpenQuery**](pdhvbopenquery.md)
- [**PdhVbUpdateLog**](pdhvbupdatelog.md)

> [!NOTE]
> 這些函 `PdhVb***` 式適用于每個進程的會話，而且不是安全線程。 這些函式只能從簡單的單一執行緒應用程式使用。
