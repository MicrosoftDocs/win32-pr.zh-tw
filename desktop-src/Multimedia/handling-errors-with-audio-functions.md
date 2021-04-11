---
title: 使用音訊函數處理錯誤
description: 使用音訊函數處理錯誤
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- 多媒體音訊、波形音訊錯誤
- 音訊、波形音訊錯誤
- 多媒體音訊、輔助音訊錯誤
- 音訊、輔助音訊錯誤
- 波形音訊、錯誤
- 輔助音訊，錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314785"
---
# <a name="handling-errors-with-audio-functions"></a><span data-ttu-id="724cb-109">使用音訊函數處理錯誤</span><span class="sxs-lookup"><span data-stu-id="724cb-109">Handling Errors with Audio Functions</span></span>

<span data-ttu-id="724cb-110">當發生錯誤時，波形-音訊和輔助音訊函數會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="724cb-110">The waveform-audio and auxiliary-audio functions return a nonzero value when an error occurs.</span></span> <span data-ttu-id="724cb-111">Windows 所提供的函式會將這些錯誤值轉換成錯誤的文字描述。</span><span class="sxs-lookup"><span data-stu-id="724cb-111">Windows provides functions that convert these error values into textual descriptions of the errors.</span></span> <span data-ttu-id="724cb-112">應用程式仍然必須檢查錯誤值以判斷如何進行，但錯誤的文字描述可用於描述錯誤給使用者的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="724cb-112">The application must still examine the error values to determine how to proceed, but textual descriptions of errors can be used in dialog boxes that describe errors to users.</span></span>

<span data-ttu-id="724cb-113">您可以使用下列函數來取出音訊錯誤值的文字描述：</span><span class="sxs-lookup"><span data-stu-id="724cb-113">You can use the following functions to retrieve textual descriptions of audio error values:</span></span>



| <span data-ttu-id="724cb-114">函式</span><span class="sxs-lookup"><span data-stu-id="724cb-114">Function</span></span>                                           | <span data-ttu-id="724cb-115">描述</span><span class="sxs-lookup"><span data-stu-id="724cb-115">Description</span></span>                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="724cb-116">**waveInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="724cb-116">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | <span data-ttu-id="724cb-117">抓取指定之波形-音訊輸入錯誤的文字描述。</span><span class="sxs-lookup"><span data-stu-id="724cb-117">Retrieves a textual description of a specified waveform-audio input error.</span></span>  |
| [<span data-ttu-id="724cb-118">**waveOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="724cb-118">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | <span data-ttu-id="724cb-119">抓取指定波形音訊輸出錯誤的文字描述。</span><span class="sxs-lookup"><span data-stu-id="724cb-119">Retrieves a textual description of a specified waveform-audio output error.</span></span> |



 

<span data-ttu-id="724cb-120">唯一不會傳回錯誤值的音訊函式為 [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)、 [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)和 [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)。</span><span class="sxs-lookup"><span data-stu-id="724cb-120">The only audio functions that do not return error values are [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs), and [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span></span> <span data-ttu-id="724cb-121">如果系統中沒有任何裝置或它們遇到任何錯誤，這些函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="724cb-121">These functions return zero if no devices are present in a system or if they encounter any errors.</span></span>

 

 