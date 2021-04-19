---
description: 雖然 \# \# Tablet PC 平臺無法同時在兩個執行緒上存取&160; 辨識器內容&160; 但是 AdviseInkChange 函式可以隨時在任何執行緒上呼叫。
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: 辨識器執行緒考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4297cc28e084bbb7c1c09593deb5babc2319ab43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992071"
---
# <a name="recognizer-threading-considerations"></a><span data-ttu-id="71e05-103">辨識器執行緒考慮</span><span class="sxs-lookup"><span data-stu-id="71e05-103">Recognizer Threading Considerations</span></span>

<span data-ttu-id="71e05-104">雖然 Tablet PC 平臺無法同時存取兩個執行緒上的辨識 [器內容](hrecocontext-handle.md) ，但可以在任何執行緒上隨時呼叫 [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) 函數。</span><span class="sxs-lookup"><span data-stu-id="71e05-104">Although a [recognizer context](hrecocontext-handle.md) cannot be accessed on two threads simultaneously by the Tablet PC platform, the [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) function can be called at any time on any thread.</span></span> <span data-ttu-id="71e05-105">因為 Tablet PC 平臺無法確保一次只有一個辨識器內容，所以個別執行緒中有兩個不同的辨識器內容可能會同時嘗試存取您的辨識 [器](hrecognizer-handle.md)。</span><span class="sxs-lookup"><span data-stu-id="71e05-105">Because the Tablet PC platform does not ensure that there is only one recognizer context at a time, two separate recognizer contexts in separate threads may simultaneously attempt to access your [recognizer](hrecognizer-handle.md).</span></span> <span data-ttu-id="71e05-106">因此，您的辨識引擎中的全域變數必須是安全線程。</span><span class="sxs-lookup"><span data-stu-id="71e05-106">Therefore, global variables in your recognition engine must be thread-safe.</span></span>

<span data-ttu-id="71e05-107">單字清單是用來提高精確度的選擇性執行。</span><span class="sxs-lookup"><span data-stu-id="71e05-107">Word lists are an optional implementation used to increase accuracy.</span></span> <span data-ttu-id="71e05-108">如果您的辨識器會實作為字組清單，它必須是安全線程。</span><span class="sxs-lookup"><span data-stu-id="71e05-108">If your recognizer implements word lists, it must be thread-safe.</span></span> <span data-ttu-id="71e05-109">如需使用 word 清單的詳細資訊，請參閱 [使用應用程式字典](using-application-dictionaries.md)。</span><span class="sxs-lookup"><span data-stu-id="71e05-109">For more information about using word lists, see [Using Application Dictionaries](using-application-dictionaries.md).</span></span>

<span data-ttu-id="71e05-110">如需其他執行緒考慮的詳細資訊，請參閱 [TABLET PC 執行緒的考慮](tablet-pc-threading-considerations.md)。</span><span class="sxs-lookup"><span data-stu-id="71e05-110">For details about other threading considerations, see [Tablet PC Threading Considerations](tablet-pc-threading-considerations.md).</span></span>

 

 



