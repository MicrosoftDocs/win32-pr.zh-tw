---
title: 複合檔案
description: 雖然您可以執行自己的結構化儲存體物件和介面，但 COM 會提供一個稱為複合檔案的標準實作為。
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183120"
---
# <a name="compound-files"></a>複合檔案

雖然您可以執行自己的結構化儲存體物件和介面，但 COM 會提供一個稱為複合檔案的標準實作為。 使用複合檔案可讓您為自己的結構化儲存體執行編寫程式碼，並授數個衍生自訂標準的額外優點。 這些優點包括：

-   **檔案系統和平臺獨立性**。 由於 COM 的複合檔案執行是在現有的一般檔案系統上執行，因此，儲存在 FAT 檔案系統、NTFS 檔案系統或 Macintosh 檔案系統中的複合檔案可以由使用任何其他檔案系統的應用程式來開啟。
-   可 **搜尋。** 由於複合檔案中的個別物件會儲存為標準格式，而且可以使用標準的 COM 介面和 Api 來存取，因此使用這些介面和 Api 的任何瀏覽器公用程式都可以列出檔案中的物件，即使指定物件內的資料可能採用專屬格式也一樣。
-   **存取特定的內部資料**。 由於複合檔案執行提供了撰寫特定資料類型的標準方式（例如摘要資訊），因此應用程式可以使用 COM 介面和 Api 來讀取此資料。

 

 




