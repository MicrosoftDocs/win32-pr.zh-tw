---
description: ELS 腳本偵測服務稱為 Microsoft 腳本偵測。
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Microsoft 腳本偵測
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114196"
---
# <a name="microsoft-script-detection"></a><span data-ttu-id="0c58b-103">Microsoft 腳本偵測</span><span class="sxs-lookup"><span data-stu-id="0c58b-103">Microsoft Script Detection</span></span>

<span data-ttu-id="0c58b-104">ELS 腳本偵測服務稱為 Microsoft 腳本偵測。</span><span class="sxs-lookup"><span data-stu-id="0c58b-104">The ELS script detection service is called Microsoft Script Detection.</span></span> <span data-ttu-id="0c58b-105">這項服務可讓應用程式偵測寫入文字的腳本。</span><span class="sxs-lookup"><span data-stu-id="0c58b-105">This service allows applications to detect the scripts in which text is written.</span></span> <span data-ttu-id="0c58b-106"> (NLS) 對應的「腳本偵測」服務的國家語言支援是 [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) 函數。</span><span class="sxs-lookup"><span data-stu-id="0c58b-106">The National Language Support (NLS) counterpart of a script detection service is the [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) function.</span></span> <span data-ttu-id="0c58b-107">不過，ELS 服務會另外抓取屬於每個書寫系統的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="0c58b-107">However, the ELS service additionally retrieves the text ranges that belong to each writing system.</span></span>

## <a name="input-to-microsoft-script-detection"></a><span data-ttu-id="0c58b-108">輸入至 Microsoft 腳本偵測</span><span class="sxs-lookup"><span data-stu-id="0c58b-108">Input to Microsoft Script Detection</span></span>

<span data-ttu-id="0c58b-109">Microsoft 腳本偵測服務的輸入是由服務決定腳本範圍的 UTF-16 文字。</span><span class="sxs-lookup"><span data-stu-id="0c58b-109">The input to the Microsoft Script Detection service is UTF-16 text for which the service determines script ranges.</span></span>

## <a name="output-of-microsoft-script-detection"></a><span data-ttu-id="0c58b-110">Microsoft 腳本偵測的輸出</span><span class="sxs-lookup"><span data-stu-id="0c58b-110">Output of Microsoft Script Detection</span></span>

<span data-ttu-id="0c58b-111">Microsoft 腳本偵測服務的輸出是範圍的陣列，每個都包含以 null 終止的 UTF-16 字串，且具有相關聯書寫系統的 Unicode 指定名稱。</span><span class="sxs-lookup"><span data-stu-id="0c58b-111">The output of the Microsoft Script Detection service is an array of ranges, each containing a null-terminated UTF-16 string with the Unicode-specified name of the associated writing system.</span></span> <span data-ttu-id="0c58b-112">這項服務會報告一般常見的 (Zyyy) ，並將 () 字元繼承為屬於先前的腳本範圍。</span><span class="sxs-lookup"><span data-stu-id="0c58b-112">The service reports regular common (Zyyy) and inherited (Qaai) characters as belonging to the previous script range.</span></span> <span data-ttu-id="0c58b-113">開始通用和繼承的字元會回報為屬於下一個腳本範圍。</span><span class="sxs-lookup"><span data-stu-id="0c58b-113">Beginning common and inherited characters are reported as belonging to the next script range.</span></span> <span data-ttu-id="0c58b-114">如果輸入文字中的所有字元都是通用或繼承的，則服務的輸出會是具有空字串作為其資料的單一範圍。</span><span class="sxs-lookup"><span data-stu-id="0c58b-114">If all the characters in the input text are common or inherited, the output of the service is a single range with the empty string as its data.</span></span>

## <a name="microsoft-script-detection-operation"></a><span data-ttu-id="0c58b-115">Microsoft 腳本偵測操作</span><span class="sxs-lookup"><span data-stu-id="0c58b-115">Microsoft Script Detection Operation</span></span>

<span data-ttu-id="0c58b-116">Microsoft 腳本偵測服務會將屬於通用範圍的程式碼點對應到上述的寫入系統。</span><span class="sxs-lookup"><span data-stu-id="0c58b-116">The Microsoft Script Detection service maps the code points belonging to the common range to the preceding writing system.</span></span> <span data-ttu-id="0c58b-117">或者，如果程式碼點位於輸入字串的開頭，則服務可以將程式碼點對應到下一個寫入系統。</span><span class="sxs-lookup"><span data-stu-id="0c58b-117">Alternatively, the service can map the code points to the next writing system if the code points are at the beginning of the input string.</span></span> <span data-ttu-id="0c58b-118">應用程式完全不需要處理通用範圍。</span><span class="sxs-lookup"><span data-stu-id="0c58b-118">The application does not have to deal with the common range at all.</span></span>

## <a name="microsoft-script-detection-guid"></a><span data-ttu-id="0c58b-119">Microsoft 腳本偵測 GUID</span><span class="sxs-lookup"><span data-stu-id="0c58b-119">Microsoft Script Detection GUID</span></span>

<span data-ttu-id="0c58b-120">Microsoft 語言偵測服務的 GUID 是在 Elssrvc 中宣告，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="0c58b-120">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a><span data-ttu-id="0c58b-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c58b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c58b-122">關於擴充的語言服務</span><span class="sxs-lookup"><span data-stu-id="0c58b-122">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



