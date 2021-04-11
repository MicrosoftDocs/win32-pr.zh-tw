---
title: 'Language Bar (TSF 應用程式) '
description: 應用程式無法將專案新增至語言列;只有文字服務可以將專案新增至語言列。
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- 文字服務架構 (TSF) 、language bar
- TSF (文字服務架構) 、language bar
- 啟用 TSF 的應用程式，語言列
- 語言列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef227b29c8b481bfaefc4a218305ba8974fe54e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103843020"
---
# <a name="language-bar-tsf-applications"></a><span data-ttu-id="41a93-107">Language Bar (TSF 應用程式) </span><span class="sxs-lookup"><span data-stu-id="41a93-107">Language Bar (TSF Applications)</span></span>

<span data-ttu-id="41a93-108">應用程式無法將專案新增至語言列;只有文字服務可以將專案新增至語言列。</span><span class="sxs-lookup"><span data-stu-id="41a93-108">An application cannot add items to the language bar; only a text service can add items to the language bar.</span></span> <span data-ttu-id="41a93-109">應用程式可能會影響語言列上特定專案的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="41a93-109">An application can affect how certain items on the language bar appear.</span></span>

<span data-ttu-id="41a93-110">[GUID 區間 \_ \_ 語音 \_ DICTATIONSTAT](predefined-compartments.md)區間用來表示應用程式可接受的語音輸入類型：直接文字輸入 (聽寫) 和/或語音命令。</span><span class="sxs-lookup"><span data-stu-id="41a93-110">The [GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT](predefined-compartments.md) compartment is used to indicate the type of speech input that the application can accept: direct text input (dictation) and/or voice commands.</span></span> <span data-ttu-id="41a93-111">依預設，會啟用聽寫並停用語音命令。</span><span class="sxs-lookup"><span data-stu-id="41a93-111">By default, dictation is enabled and voice command is disabled.</span></span> <span data-ttu-id="41a93-112">如果應用程式可以接受語音命令，則應該在 GUID 區間語音 DICTATIONSTAT 區間中設定 [TF 命令 \_ \_ ENABLED](speech-recognition-constants.md) 值 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="41a93-112">If the application can accept voice commands, it should set the [TF\_COMMANDING\_ENABLED](speech-recognition-constants.md) value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="41a93-113">如果應用程式可以接受聽寫，則應該 \_ \_ 在 GUID 區間語音 DICTATIONSTAT 區間中設定 TF 聽寫啟用的值 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="41a93-113">If the application can accept dictation, it should set the TF\_DICTATION\_ENABLED value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="41a93-114">此區間的值上的 TF \_ 聽寫 \_ ON 或 tf \_ 命令， \_ 會決定 (聽寫或命令) 語音輸入目前在哪個模式。</span><span class="sxs-lookup"><span data-stu-id="41a93-114">The TF\_DICTATION\_ON or TF\_COMMANDING\_ON value of this compartment determines which mode (dictation or command) speech input is currently in.</span></span>

<span data-ttu-id="41a93-115">如果應用程式支援屬性資料的持續性儲存，則應該將 [GUID \_ 區間 \_ PERSISTMENUENABLED](predefined-compartments.md) 區間設定為非零值。</span><span class="sxs-lookup"><span data-stu-id="41a93-115">If the application supports persistent storage of property data, it should set the [GUID\_COMPARTMENT\_PERSISTMENUENABLED](predefined-compartments.md) compartment to a nonzero value.</span></span> <span data-ttu-id="41a93-116">這會導致語音文字服務啟用 [ **儲存語音資料** ] 功能表項目。</span><span class="sxs-lookup"><span data-stu-id="41a93-116">This causes the speech text service to enable the **Save Speech Data** menu item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41a93-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="41a93-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41a93-118">如何設定文字服務架構</span><span class="sxs-lookup"><span data-stu-id="41a93-118">How To Set Up Text Services Framework</span></span>](how-to-set-up-tsf.md)
</dt> <dt>

[<span data-ttu-id="41a93-119">Language Bar (Text Services) </span><span class="sxs-lookup"><span data-stu-id="41a93-119">Language Bar (Text Services)</span></span>](language-bar.md)
</dt> </dl>

 

 




