---
description: 平臺路徑覆寫
ms.assetid: f430fd9a-f865-4cdb-b0ea-4e6d79913308
title: 平臺路徑覆寫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9a6ae6795b444c44db91d90ecd93efd19ea9dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992590"
---
# <a name="platform-path-override"></a>平臺路徑覆寫

當使用來自不同電腦的 INF 檔案時，會使用 [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) 函數來設定目的電腦的平臺路徑覆寫。 因此，它可以參考不同于目前執行所在的平臺。 針對處理媒體來源，它可以參考不再支援的平臺，例如 Alpha、MIPS 和 PPC。 如果沒有指定，則會移除平臺路徑覆寫。

在平臺路徑覆寫由呼叫 [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea)設定之後，任何佇列檔案複製作業的安裝函式都會檢查來源路徑的最後一個元件。 如果最終元件符合使用者平臺的名稱，則安裝函式會將它取代為 **SetupSetPlatformPathOverride** 所設定的覆寫字串。

例如，在將印表機驅動程式安裝到 MIPS 伺服器上時，您可能會想要為所有支援的平臺安裝驅動程式。 將檔案排入佇列通常會安裝 INF 檔案的 MIPS 相依區段中指定的檔案，以及來源路徑，例如 \\ \\ 根 \\ 來源 \\ MIPS。 若要安裝第二個平臺的檔案，您必須使用覆 *寫* 來呼叫 [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) ，以表示取代平臺。 如果覆 *寫* 所指示的位置包含字串值 "Alpha"，則會將檔案複製作業傳送至來源路徑為根來源 mips 的佇列，而 \\ \\ \\ \\ 其來源路徑會變更為 \\ \\ 根 \\ 來源 \\ Alpha。 您可以針對每個感興趣的平臺重複此程式。

 

 



