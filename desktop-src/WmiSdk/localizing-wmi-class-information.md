---
description: WMI 所實行的技術，可讓多個當地語系化版本的相同類別儲存在存放庫中。
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: 當地語系化 WMI 類別資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9f1a7e34c3ba230655ebba4c070981a8dab901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320335"
---
# <a name="localizing-wmi-class-information"></a><span data-ttu-id="a4e4e-103">當地語系化 WMI 類別資訊</span><span class="sxs-lookup"><span data-stu-id="a4e4e-103">Localizing WMI Class Information</span></span>

<span data-ttu-id="a4e4e-104">WMI 所實行的技術，可讓多個當地語系化版本的相同類別儲存在存放庫中。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-104">WMI implements a technique that allows multiple localized versions of the same class to be stored in the repository.</span></span>

<span data-ttu-id="a4e4e-105">類別定義會分成下列版本：</span><span class="sxs-lookup"><span data-stu-id="a4e4e-105">The class definition is separated into the following versions:</span></span>

-   <span data-ttu-id="a4e4e-106">僅包含基本類別定義的非語言相關版本。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-106">A language-neutral version that contains only a basic class definition.</span></span>
-   <span data-ttu-id="a4e4e-107">包含當地語系化資訊的特定語言版本，例如地區設定特有的屬性描述。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-107">A language-specific version that contains localized information, such as property descriptions that are specific to a locale.</span></span>

<span data-ttu-id="a4e4e-108">特定語言的類別定義會儲存在包含非語言相關基本類別定義的命名空間底下的子命名空間中。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-108">The language-specific class definitions are stored in a child namespace beneath the namespace that contains a language-neutral basic class definition.</span></span>

<span data-ttu-id="a4e4e-109">當您針對特定地區設定要求當地語系化的類別定義時，WMI 會結合基本類別定義和當地語系化類別資訊來形成完整的當地語系化類別。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-109">When you request a localized class definition for a specific locale, WMI combines the basic class definition and the localized class information to form a complete localized class.</span></span> <span data-ttu-id="a4e4e-110">您可以在連線至 WMI 時指定地區設定，並設定指出您要當地語系化資訊的旗標，以取得 WMI 類別的當地語系化版本。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-110">You can get a localized version of a WMI class by specifying a locale when you connect to WMI and setting a flag that indicates that you want localized information.</span></span> <span data-ttu-id="a4e4e-111">WMI 接著會合並語言中立的資訊，以及類別定義的語言特定版本，以形成當地語系化的類別。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-111">WMI then merges the information from the language-neutral and the language-specific versions of the class definition to form a localized class.</span></span>

<span data-ttu-id="a4e4e-112">包含當地語系化資訊的 WMI 類別會以 **修訂** 辨識符號標示，並稱為修改過的類別;類別支援當地語系化的資訊（如果有此限定詞的話）。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-112">WMI classes that contain localized information are marked with the **Amendment** qualifier and are called amended classes; a class supports localized information if it has this qualifier.</span></span> <span data-ttu-id="a4e4e-113">您可以藉由檢查另一個稱為 [**地區**](swbemobjectpath-locale.md)設定的辨識符號，判斷類別已當地語系化的地區設定。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-113">You can determine which locale the class has been localized for by checking for another qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span> <span data-ttu-id="a4e4e-114">地區設定限定詞包含 (Windows LCID) 的當地語系化識別碼，以識別地區設定。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-114">The locale qualifier contains a localization identifier (Windows LCID) that identifies a locale.</span></span> <span data-ttu-id="a4e4e-115">例如，美式英文的地區設定是0x409。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-115">For example, the locale for American English is 0x409.</span></span> <span data-ttu-id="a4e4e-116">如果修改過的類別中的辨識符號包含當地語系化的資訊，它就會包含 **修改** 過的辨識符號類別。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-116">If a qualifier in an amended class contains localized information, it contains the **amended** qualifier flavor.</span></span>

<span data-ttu-id="a4e4e-117">WMI 當地語系化包含下列工作：</span><span class="sxs-lookup"><span data-stu-id="a4e4e-117">WMI localization includes the following tasks:</span></span>

-   [<span data-ttu-id="a4e4e-118">建立當地語系化的類別定義</span><span class="sxs-lookup"><span data-stu-id="a4e4e-118">Creating localized class definitions</span></span>](creating-localized-class-definitions.md)
-   [<span data-ttu-id="a4e4e-119">編譯當地語系化的 MOF 檔案</span><span class="sxs-lookup"><span data-stu-id="a4e4e-119">Compiling localized MOF files</span></span>](compiling-localized-mof-files.md)
-   [<span data-ttu-id="a4e4e-120">當地語系化屬性值</span><span class="sxs-lookup"><span data-stu-id="a4e4e-120">Localizing property values</span></span>](localizing-property-values.md)
-   [<span data-ttu-id="a4e4e-121">正在抓取修改過的類別</span><span class="sxs-lookup"><span data-stu-id="a4e4e-121">Retrieving amended classes</span></span>](retrieving-amended-classes.md)

<span data-ttu-id="a4e4e-122">如需詳細資訊，請參閱修改過的 [類別考慮](amended-class-considerations.md)。</span><span class="sxs-lookup"><span data-stu-id="a4e4e-122">For more information, see [Amended Class Considerations](amended-class-considerations.md).</span></span>

 

 



