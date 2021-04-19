---
description: 安裝函數會在內部處理封包。 若要從封包明確地列舉和解壓縮檔案，您可以呼叫 SetupIterateCabinet 函式。
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: 使用封包檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03467f6591b4503cb13935cca550f8c1ba1dff81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980611"
---
# <a name="using-cabinet-files"></a>使用封包檔

安裝函數會在內部處理封包。 若要從封包明確地列舉和解壓縮檔案，您可以呼叫 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 函式。

下列主題描述安裝函式內部的封包處理，以及如何使用 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)。 此外，也會討論 **SetupIterateCabinet** 所傳送的通知，以及封包回呼常式的必要格式來處理這些通知。

-   [從封包解壓縮檔案](extracting-files-from-cabinets.md)
-   [建立封包回呼常式](creating-a-cabinet-callback-routine.md)

 

 



