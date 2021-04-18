---
title: 正在載入預設字元
description: 正在載入預設字元
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 387715b5078c4ec875c9abce47039898e4998cf7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964968"
---
# <a name="loading-the-default-character"></a><span data-ttu-id="fa37c-103">正在載入預設字元</span><span class="sxs-lookup"><span data-stu-id="fa37c-103">Loading the Default Character</span></span>

<span data-ttu-id="fa37c-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="fa37c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="fa37c-105">您可以載入 *預設字元*，而不是直接載入特定字元，而不是直接載入指定的字元。</span><span class="sxs-lookup"><span data-stu-id="fa37c-105">Instead of loading only a specific character directly by specifying its filename, you can load the *default character*.</span></span> <span data-ttu-id="fa37c-106">預設字元是一種服務，其目的是要提供使用者選擇的共用、中央 Windows 輔助程式。</span><span class="sxs-lookup"><span data-stu-id="fa37c-106">The default character is a service intended to provide a shared, central Windows assistant that the user chooses.</span></span> <span data-ttu-id="fa37c-107">Microsoft Agent 將屬性工作表包含為預設字元服務的一部分，也就是字元屬性視窗，可讓使用者變更選取的預設字元。</span><span class="sxs-lookup"><span data-stu-id="fa37c-107">Microsoft Agent includes a property sheet as part of the default character service, known as the Character Properties window, which enables the user to change their selection of the default character.</span></span>

<span data-ttu-id="fa37c-108">預設字元的選取範圍僅限於支援標準動畫集的字元，以確保跨字元的基本一致性層級。</span><span class="sxs-lookup"><span data-stu-id="fa37c-108">Selection of the default character is limited to a character that supports the standard animation set, ensuring a basic level of consistency across characters.</span></span> <span data-ttu-id="fa37c-109">這不會排除包含其他動畫的字元。</span><span class="sxs-lookup"><span data-stu-id="fa37c-109">This does not exclude a character from having additional animations.</span></span>

<span data-ttu-id="fa37c-110">不過，因為預設字元是用於一般用途，而且可能會同時由其他應用程式共用，所以當您想要讓應用程式專用的字元時，請避免載入預設字元。</span><span class="sxs-lookup"><span data-stu-id="fa37c-110">However, because the default character is intended for general-purpose use and may be shared by other applications at the same time, avoid loading the default character when you want a character exclusively for your application.</span></span>

<span data-ttu-id="fa37c-111">若要載入預設字元，請呼叫 [**load**](load-method.md) 方法，而不指定檔案名或路徑。</span><span class="sxs-lookup"><span data-stu-id="fa37c-111">To load the default character, call the [**Load**](load-method.md) method without specifying a filename or path.</span></span> <span data-ttu-id="fa37c-112">Microsoft Agent 會自動將目前的字元集載入為預設字元。</span><span class="sxs-lookup"><span data-stu-id="fa37c-112">Microsoft Agent automatically loads the current character set as the default character.</span></span> <span data-ttu-id="fa37c-113">如果使用者尚未選取預設字元，則代理程式會選取支援標準動畫集的第一個字元。</span><span class="sxs-lookup"><span data-stu-id="fa37c-113">If the user has not yet selected a default character, Agent will select the first character that supports the standard animation set.</span></span> <span data-ttu-id="fa37c-114">如果沒有可用的，方法將會失敗，並回報原因。</span><span class="sxs-lookup"><span data-stu-id="fa37c-114">If none is available, the method will fail and report back the cause.</span></span>

<span data-ttu-id="fa37c-115">雖然用戶端應用程式可以查詢字元的身分識別，但是只有使用者可以變更其設定。</span><span class="sxs-lookup"><span data-stu-id="fa37c-115">Although a client application can inquire as to the identity of the character, only a user can change its settings.</span></span> <span data-ttu-id="fa37c-116">您可以使用 [**ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) 來顯示屬性視窗字元。</span><span class="sxs-lookup"><span data-stu-id="fa37c-116">You can use the [**ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) to display the Character Properties window.</span></span>

<span data-ttu-id="fa37c-117">當使用者變更選取的字元時，伺服器會通知已載入預設字元的用戶端，並傳遞新字元的 GUID。</span><span class="sxs-lookup"><span data-stu-id="fa37c-117">The server will notify clients that have loaded the default character when a user changes a character selection, and pass the GUID of the new character.</span></span> <span data-ttu-id="fa37c-118">伺服器會自動卸載先前的字元，並重載新的字元。</span><span class="sxs-lookup"><span data-stu-id="fa37c-118">The server automatically unloads the former character and reloads the new character.</span></span> <span data-ttu-id="fa37c-119">已載入預設字元之任何用戶端的佇列都會暫停和清除。</span><span class="sxs-lookup"><span data-stu-id="fa37c-119">The queues of any clients that have loaded the default character are halted and flushed.</span></span> <span data-ttu-id="fa37c-120">不過，使用字元的檔案名明確載入字元的用戶端佇列不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="fa37c-120">However, the queues of clients that have loaded the character explicitly using the character's filename are not affected.</span></span> <span data-ttu-id="fa37c-121">如有必要，伺服器也會處理新字元的文字轉換語音 (TTS) 引擎的自動重設。</span><span class="sxs-lookup"><span data-stu-id="fa37c-121">If necessary, the server also handles automatically resetting the text-to-speech (TTS) engine for the new character.</span></span>

 

 




