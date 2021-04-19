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
# <a name="platform-path-override"></a><span data-ttu-id="9c785-103">平臺路徑覆寫</span><span class="sxs-lookup"><span data-stu-id="9c785-103">Platform Path Override</span></span>

<span data-ttu-id="9c785-104">當使用來自不同電腦的 INF 檔案時，會使用 [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) 函數來設定目的電腦的平臺路徑覆寫。</span><span class="sxs-lookup"><span data-stu-id="9c785-104">The [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) function is used to set a platform path override for a target machine when working with INF files from a different machine.</span></span> <span data-ttu-id="9c785-105">因此，它可以參考不同于目前執行所在的平臺。</span><span class="sxs-lookup"><span data-stu-id="9c785-105">As such, it can refer to a different platform than the one it is currently running on.</span></span> <span data-ttu-id="9c785-106">針對處理媒體來源，它可以參考不再支援的平臺，例如 Alpha、MIPS 和 PPC。</span><span class="sxs-lookup"><span data-stu-id="9c785-106">For dealing with media sources, it can refer to platforms that are no longer supported, such as Alpha, MIPS, and PPC.</span></span> <span data-ttu-id="9c785-107">如果沒有指定，則會移除平臺路徑覆寫。</span><span class="sxs-lookup"><span data-stu-id="9c785-107">It removes the platform path override if none is specified.</span></span>

<span data-ttu-id="9c785-108">在平臺路徑覆寫由呼叫 [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea)設定之後，任何佇列檔案複製作業的安裝函式都會檢查來源路徑的最後一個元件。</span><span class="sxs-lookup"><span data-stu-id="9c785-108">After a platform path override is set by a call to [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea), any setup function that queues file copy operations will examine the final component of the source path.</span></span> <span data-ttu-id="9c785-109">如果最終元件符合使用者平臺的名稱，則安裝函式會將它取代為 **SetupSetPlatformPathOverride** 所設定的覆寫字串。</span><span class="sxs-lookup"><span data-stu-id="9c785-109">If the final component matches the name of the user's platform, the setup function will replace it with the override string set by **SetupSetPlatformPathOverride**.</span></span>

<span data-ttu-id="9c785-110">例如，在將印表機驅動程式安裝到 MIPS 伺服器上時，您可能會想要為所有支援的平臺安裝驅動程式。</span><span class="sxs-lookup"><span data-stu-id="9c785-110">For example, when installing printer drivers onto a MIPS server, you might want to install drivers for all supported platforms.</span></span> <span data-ttu-id="9c785-111">將檔案排入佇列通常會安裝 INF 檔案的 MIPS 相依區段中指定的檔案，以及來源路徑，例如 \\ \\ 根 \\ 來源 \\ MIPS。</span><span class="sxs-lookup"><span data-stu-id="9c785-111">Queuing the files normally would install the files specified in the MIPS-dependent sections of the INF file, with source paths such as \\\\root\\source\\mips.</span></span> <span data-ttu-id="9c785-112">若要安裝第二個平臺的檔案，您必須使用覆 *寫* 來呼叫 [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) ，以表示取代平臺。</span><span class="sxs-lookup"><span data-stu-id="9c785-112">To install the files for a second platform, you must call [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) with *Override* indicating the replacement platform.</span></span> <span data-ttu-id="9c785-113">如果覆 *寫* 所指示的位置包含字串值 "Alpha"，則會將檔案複製作業傳送至來源路徑為根來源 mips 的佇列，而 \\ \\ \\ \\ 其來源路徑會變更為 \\ \\ 根 \\ 來源 \\ Alpha。</span><span class="sxs-lookup"><span data-stu-id="9c785-113">If the location indicated by *Override* contains the string value "alpha", file copy operations sent to the queue with a source path of \\\\root\\source\\mips would have their source path changed to \\\\root\\source\\alpha.</span></span> <span data-ttu-id="9c785-114">您可以針對每個感興趣的平臺重複此程式。</span><span class="sxs-lookup"><span data-stu-id="9c785-114">You would repeat this process for each platform of interest.</span></span>

 

 



