---
description: 為了讓 Tablet PC 應用程式能夠有效地操作筆墨，該應用程式應該能夠：
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: 重要互通性案例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967091"
---
# <a name="important-interoperability-scenarios"></a><span data-ttu-id="5f60b-103">重要互通性案例</span><span class="sxs-lookup"><span data-stu-id="5f60b-103">Important Interoperability Scenarios</span></span>

<span data-ttu-id="5f60b-104">為了讓 Tablet PC 應用程式能夠有效地操作筆墨，該應用程式應該能夠：</span><span class="sxs-lookup"><span data-stu-id="5f60b-104">For a Tablet PC application to operate with ink effectively, that application should be able to:</span></span>

-   <span data-ttu-id="5f60b-105">將檔儲存為應用程式的原生二進位格式，而不會遺失檔的筆墨。</span><span class="sxs-lookup"><span data-stu-id="5f60b-105">Save a document in the application's native binary format without losing the document's ink.</span></span>
-   <span data-ttu-id="5f60b-106">以任何格式儲存檔，讓應用程式正常支援 (例如 HTML 或 Rtf 格式 (RTF) ) ，而不會遺失檔的筆跡。</span><span class="sxs-lookup"><span data-stu-id="5f60b-106">Save a document in any format the application normally supports (for example, HTML or Rich Text Format (RTF)) without losing the document's ink.</span></span>
-   <span data-ttu-id="5f60b-107">使用剪貼簿，將筆墨從某個應用程式複製到另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="5f60b-107">Copy ink from one application to another by using the Clipboard.</span></span> <span data-ttu-id="5f60b-108">如果另一個應用程式只會辨識特定格式，例如 HTML、RTF 或點陣圖 (BMP) ，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="5f60b-108">This works if the other application only recognizes a specific format, such as HTML, RTF, or bitmap (BMP).</span></span> <span data-ttu-id="5f60b-109">它也適用于目的地應用程式是否辨識筆跡。</span><span class="sxs-lookup"><span data-stu-id="5f60b-109">It also works whether the destination application recognizes ink.</span></span> <span data-ttu-id="5f60b-110">如果它辨識筆墨，目的地應用程式就能夠解讀已複製為筆墨的筆墨，而不只是影像。</span><span class="sxs-lookup"><span data-stu-id="5f60b-110">If it does recognize ink, the destination application is able to interpret the ink that has been copied as ink and not just as an image.</span></span>
-   <span data-ttu-id="5f60b-111">在辨識筆墨的兩個應用程式之間複製筆跡和文字，其中每一個都有一個以上的 [**筆墨**](inkdisp-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="5f60b-111">Copy ink, along with text, between two applications that recognize ink, each of which has more than one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="5f60b-112">這需要 HTML、RTF 或類似的格式。</span><span class="sxs-lookup"><span data-stu-id="5f60b-112">This requires HTML, RTF, or a similar format.</span></span>
-   <span data-ttu-id="5f60b-113">在兩個應用程式之間複製筆跡，每個應用程式都有一個 [**ink**](inkdisp-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="5f60b-113">Copy ink between two applications, each of which has one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="5f60b-114">筆跡序列化格式 (ISF) 即已足夠。</span><span class="sxs-lookup"><span data-stu-id="5f60b-114">Ink Serialized Format (ISF) is sufficient for this.</span></span>
-   <span data-ttu-id="5f60b-115">從具有一個以上 [**筆墨**](inkdisp-class.md) 物件的應用程式，將筆墨複製到只有一個 **筆墨** 物件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5f60b-115">Copy ink from an application that has more than one [**Ink**](inkdisp-class.md) object to an application that has only one **Ink** object.</span></span> <span data-ttu-id="5f60b-116">在此情況下，具有一個以上 **筆墨** 物件的應用程式必須能夠產生筆跡序列化格式 (ISF) 。</span><span class="sxs-lookup"><span data-stu-id="5f60b-116">In this case, the application that has more than one **Ink** object must be able to produce Ink Serialized Format (ISF).</span></span>
-   <span data-ttu-id="5f60b-117">從具有一個 [**筆墨**](inkdisp-class.md) 物件的應用程式，將筆墨複製到具有多個 **筆墨** 物件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5f60b-117">Copy ink from an application that has one [**Ink**](inkdisp-class.md) object to an application that has more than one **Ink** object.</span></span> <span data-ttu-id="5f60b-118">在此情況下，具有一個以上 **筆墨** 物件的應用程式必須能夠辨識 ISF。</span><span class="sxs-lookup"><span data-stu-id="5f60b-118">In this case, the application that has more than one **Ink** object must be able to recognize ISF.</span></span>

 

 



