---
title: 輸入格式列舉
description: 輸入格式列舉
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows Media Format SDK，輸入格式列舉
- Windows Media Format SDK，列舉輸入格式
- Advanced Systems Format (ASF) 、輸入格式列舉
- ASF (Advanced 系統格式) 、輸入格式列舉
- Advanced Systems Format (ASF) ，列舉輸入格式
- ASF (Advanced 系統格式) ，列舉輸入格式
- 輸入格式列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e853aeeac5ca470f1b33b611b287cba8fa025dc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462433"
---
# <a name="input-format-enumeration"></a><span data-ttu-id="d2a24-110">輸入格式列舉</span><span class="sxs-lookup"><span data-stu-id="d2a24-110">Input Format Enumeration</span></span>

<span data-ttu-id="d2a24-111">寫入器物件會從您提供的設定檔取得串流格式資訊。</span><span class="sxs-lookup"><span data-stu-id="d2a24-111">The writer object gets stream format information from the profile you give it.</span></span> <span data-ttu-id="d2a24-112">設定檔中的串流設定資訊可為寫入器提供在檔案中寫入資料所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="d2a24-112">Stream configuration information in a profile gives the writer all of the information it needs about how the data is to be written in the file.</span></span> <span data-ttu-id="d2a24-113">設定檔不會提供有關您的應用程式所提供之輸入範例格式的任何資訊給寫入器。</span><span class="sxs-lookup"><span data-stu-id="d2a24-113">The profile does not provide the writer with any information about the format of the input samples that your application delivers.</span></span> <span data-ttu-id="d2a24-114">只有使用其中一種 Windows Media 編解碼器壓縮的資料流程才會知道輸入格式：您可以根據設定檔中的資訊來預測任意資料流程類型的輸入。</span><span class="sxs-lookup"><span data-stu-id="d2a24-114">Input formats will be unknown only for streams compressed with one of the Windows Media codecs; inputs for arbitrary stream types are predictable based on the information in the profile.</span></span>

<span data-ttu-id="d2a24-115">寫入器物件可以與資料流程的編解碼器進行通訊，以判斷可以使用的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="d2a24-115">The writer object can communicate with the codec for a stream to determine the input types that can be used.</span></span> <span data-ttu-id="d2a24-116">提供方法來列舉可能的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="d2a24-116">Methods are provided to enumerate the possible input types.</span></span> <span data-ttu-id="d2a24-117">您應該一律尋找符合輸入媒體的輸入類型，方法是列舉支援的類型，而不是手動設定輸入媒體屬性。</span><span class="sxs-lookup"><span data-stu-id="d2a24-117">You should always find the input type that matches your input media by enumerating the supported types rather than setting the input media properties manually.</span></span> <span data-ttu-id="d2a24-118">如需詳細資訊，請參閱 [來列舉輸入格式](to-enumerate-input-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="d2a24-118">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2a24-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2a24-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2a24-120">**檔案寫入功能**</span><span class="sxs-lookup"><span data-stu-id="d2a24-120">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="d2a24-121">**使用輸入**</span><span class="sxs-lookup"><span data-stu-id="d2a24-121">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




