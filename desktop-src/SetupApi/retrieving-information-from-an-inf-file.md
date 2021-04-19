---
description: 當您有 INF 檔案的控制碼之後，您可以透過各種方式來抓取它的資訊。 SetupGetInfInformation、SetupQueryInfFileInformation 和 SetupQueryInfVersionInformation 之類的函式會取得 INF 檔案本身的相關資訊。
ms.assetid: e64c9576-ad62-4ebd-8d30-4e4e0da3b8c5
title: 從 INF 檔案中取出資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cfb1a52fd004b1d812e4a01320a5bdd2bbeca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979173"
---
# <a name="retrieving-information-from-an-inf-file"></a>從 INF 檔案中取出資訊

當您有 INF 檔案的控制碼之後，您可以透過各種方式來抓取它的資訊。 [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)、 [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)和 [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)之類的函式會取得 INF 檔案本身的相關資訊。

[**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)和 [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)等其他功能會取得來源檔案和目標目錄的相關資訊。

低層級功能（例如 [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) 和 [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) ）可讓您直接存取儲存在 INF 檔案的行或欄位中的資訊。 這些函式會由較高層級的函式在內部使用，但如果您需要存取行或欄位層級的 INF 資訊，也可以使用這些函式。

 

 



