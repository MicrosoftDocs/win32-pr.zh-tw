---
title: 應用程式相容性層
description: 若要在遠端桌面服務環境中執行繼承應用程式，您可以使用遠端桌面服務應用程式相容性層。
ms.assetid: 6e61ed45-4fcb-4aee-b8cc-638a9b87ce00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e7bbc5867e42951783d3666aa770cdcc45406f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106999802"
---
# <a name="application-compatibility-layer"></a><span data-ttu-id="21cc0-103">應用程式相容性層</span><span class="sxs-lookup"><span data-stu-id="21cc0-103">Application compatibility layer</span></span>

<span data-ttu-id="21cc0-104">若要在遠端桌面服務環境中執行繼承應用程式，您可以使用遠端桌面服務應用程式相容性層。</span><span class="sxs-lookup"><span data-stu-id="21cc0-104">To run legacy applications in a Remote Desktop Services environment you can use the Remote Desktop Services Application Compatibility layer.</span></span> <span data-ttu-id="21cc0-105">當遠端桌面工作階段主機 (RD 工作階段主機) 伺服器載入未遠端桌面服務感知的應用程式時，它也會載入包含相容性程式碼的 DLL。</span><span class="sxs-lookup"><span data-stu-id="21cc0-105">When the Remote Desktop Session Host (RD Session Host) server loads an application that is not Remote Desktop Services aware, it also loads a DLL that contains compatibility code.</span></span> <span data-ttu-id="21cc0-106">若要使用遠端桌面服務應用程式相容性層級，您可以在編譯應用程式時設定 NOT TSAWARE 旗標。</span><span class="sxs-lookup"><span data-stu-id="21cc0-106">To use the Remote Desktop Services Application Compatibility layer, you can set the NOT TSAWARE flag when compiling an application.</span></span>

<span data-ttu-id="21cc0-107">如果您的應用程式遠端桌面服務感知，您可以避免載入此額外 DLL 並執行相容性程式碼的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="21cc0-107">If your application is Remote Desktop Services aware, you can avoid the overhead of loading this extra DLL and running the compatibility code.</span></span>

<span data-ttu-id="21cc0-108">若要指出您的應用程式遠端桌面服務感知，請在選用標頭中設定 **IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL \_ SERVER \_ 感知** 旗標。</span><span class="sxs-lookup"><span data-stu-id="21cc0-108">To indicate that your application is Remote Desktop Services aware, set the **IMAGE\_DLLCHARACTERISTICS\_TERMINAL\_SERVER\_AWARE** flag in the optional header.</span></span> <span data-ttu-id="21cc0-109">如果您使用 Microsoft Visual C++ 隨附的連結器，您可以使用 **TSAWARE** 連結器選項來設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="21cc0-109">If you are using the linker that ships with Microsoft Visual C++, you can use the **TSAWARE** linker option to set this flag.</span></span> <span data-ttu-id="21cc0-110">Microsoft Visual C++ 隨附的 **DUMPBIN** 工具提供 */HEADERS* 選項來判斷 **TSAWARE** 旗標的狀態。</span><span class="sxs-lookup"><span data-stu-id="21cc0-110">The **DUMPBIN** tool that ships with Microsoft Visual C++ provides the */HEADERS* option to determine the state of the **TSAWARE** flag.</span></span> <span data-ttu-id="21cc0-111">如需使用 **DUMPBIN** 工具的詳細資訊，請參閱 [DUMPBIN 參考](/cpp/build/reference/dumpbin-reference?view=vs-2019)。</span><span class="sxs-lookup"><span data-stu-id="21cc0-111">For more information about using the **DUMPBIN** tool, see [DUMPBIN Reference](/cpp/build/reference/dumpbin-reference?view=vs-2019).</span></span>

<span data-ttu-id="21cc0-112">當您使用 **TSAWARE** 旗標時請小心，因為它可讓您的應用程式略過任何遠端桌面服務相容性優化。</span><span class="sxs-lookup"><span data-stu-id="21cc0-112">Be careful when you use the **TSAWARE** flag because it enables your application to bypass any Remote Desktop Services compatibility optimizations.</span></span> <span data-ttu-id="21cc0-113">只有當您確定應用程式是針對遠端桌面服務環境而設計時，才應該使用 **TSAWARE** 旗標。</span><span class="sxs-lookup"><span data-stu-id="21cc0-113">The **TSAWARE** flag should only be used if you are certain that your application is designed for the Remote Desktop Services environment.</span></span> <span data-ttu-id="21cc0-114">如果您的應用程式符合下列準則，您可以安全地使用「 **映射 \_ DLLCHARACTERISTICS \_ 終端機 \_ 伺服器 \_ 感知** 」旗標。</span><span class="sxs-lookup"><span data-stu-id="21cc0-114">If your application meets the following criteria, you can safely use the **IMAGE\_DLLCHARACTERISTICS\_TERMINAL\_SERVER\_AWARE** flag.</span></span>

-   <span data-ttu-id="21cc0-115">應用程式不會使用 .ini 檔案。</span><span class="sxs-lookup"><span data-stu-id="21cc0-115">The application does not use .ini files.</span></span>
-   <span data-ttu-id="21cc0-116">在安裝期間，應用程式不會寫入 **HKEY \_ 目前的 \_ 使用者** 。</span><span class="sxs-lookup"><span data-stu-id="21cc0-116">The application does not write to **HKEY\_CURRENT\_USER** during setup.</span></span> <span data-ttu-id="21cc0-117">如需詳細資訊，請參閱 [儲存 User-Specific 資訊](storing-user-specific-information.md)。</span><span class="sxs-lookup"><span data-stu-id="21cc0-117">For more information, see [Storing User-Specific Information](storing-user-specific-information.md).</span></span>
-   <span data-ttu-id="21cc0-118">應用程式不會以系統服務的形式執行， (也就是 LUID = System) 。</span><span class="sxs-lookup"><span data-stu-id="21cc0-118">The application does not run as a system service (that is, LUID=System).</span></span>
-   <span data-ttu-id="21cc0-119">應用程式不需要獨佔存取 Windows 或其他系統目錄。</span><span class="sxs-lookup"><span data-stu-id="21cc0-119">The application does not expect exclusive access to the Windows or other system directories.</span></span> <span data-ttu-id="21cc0-120">這表示應用程式不會將每個使用者的暫存或設定資料儲存在 Windows 或其他系統目錄中。</span><span class="sxs-lookup"><span data-stu-id="21cc0-120">This means that the application does not store per user temporary or configuration data in the Windows or other system directories.</span></span>
-   <span data-ttu-id="21cc0-121">應用程式不會將使用者特定資料或設定寫入 **HKEY 本機電腦** 登錄 hive。</span><span class="sxs-lookup"><span data-stu-id="21cc0-121">The application does not write to the **HKEY Local Machine** registry hive for user specific data or configuration.</span></span>
-   <span data-ttu-id="21cc0-122">應用程式會遵循本檔中所述的其他遠端桌面服務相容性指導方針。</span><span class="sxs-lookup"><span data-stu-id="21cc0-122">The application follows other Remote Desktop Services compatibility guidelines mentioned in this document.</span></span>

 

 