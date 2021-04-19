---
title: " (OpenGL) 處理錯誤"
description: 當 OpenGL 偵測到錯誤時，它會記錄目前的錯誤碼。
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- 處理 OpenGL 時發生錯誤
- OpenGL 錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2005eb38f85e6e57f814a3ec61abf8b76fa4761
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967704"
---
# <a name="error-handling-opengl"></a><span data-ttu-id="f5df5-105"> (OpenGL) 處理錯誤</span><span class="sxs-lookup"><span data-stu-id="f5df5-105">Error Handling (OpenGL)</span></span>

<span data-ttu-id="f5df5-106">當 OpenGL 偵測到錯誤時，它會記錄目前的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f5df5-106">When OpenGL detects an error, it records a current error code.</span></span> <span data-ttu-id="f5df5-107">會忽略造成錯誤的函式，因此它不會影響 OpenGL 狀態或畫面格緩衝區內容。</span><span class="sxs-lookup"><span data-stu-id="f5df5-107">The function that caused the error is ignored, so it has no effect on the OpenGL state or on the framebuffer contents.</span></span> <span data-ttu-id="f5df5-108"> (，如果記錄的錯誤是 \_ GL \_ 的記憶體不足，則函式 \_ 的結果為未定義。 ) 記錄之後，除非您呼叫 [**glGetError**](glgeterror.md) 查詢函式，而該函式會傳回目前的錯誤碼，否則不會清除目前的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f5df5-108">(If the error recorded was GL\_OUT\_OF\_MEMORY, however, the results of the function are undefined.) Once recorded, the current error code isn't cleared until you call the [**glGetError**](glgeterror.md) query function, which returns the current error code.</span></span>

<span data-ttu-id="f5df5-109">OpenGL 的執行可能會傳回多個目前的錯誤碼，每個錯誤碼都會保持設定直到查詢為止。</span><span class="sxs-lookup"><span data-stu-id="f5df5-109">Implementations of OpenGL may return multiple current error codes, each of which remains set until queried.</span></span> <span data-ttu-id="f5df5-110">當 \_ \_ 您查詢所有目前的錯誤碼或沒有錯誤時，glGetError 函式會傳回 GL 無錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5df5-110">The **glGetError** function returns GL\_NO\_ERROR once you've queried all the current error codes or if there is no error.</span></span> <span data-ttu-id="f5df5-111">因此，如果您收到錯誤代碼，請呼叫 **glGetError** 直到 GL \_ 未 \_ 傳回錯誤，以確定您已探索到所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5df5-111">Therefore, if you obtain an error code, call **glGetError** until GL\_NO\_ERROR is returned to be sure you've discovered all the errors.</span></span> <span data-ttu-id="f5df5-112">如需錯誤碼清單，請參閱 [OpenGL 錯誤碼](opengl-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="f5df5-112">For the list of error codes, see [OpenGL error codes](opengl-error-codes.md).</span></span>

<span data-ttu-id="f5df5-113">您可以使用 [**gluErrorString**](gluerrorstring.md) x.glu 隊函式來取得對應至傳入之錯誤碼的描述性字串。</span><span class="sxs-lookup"><span data-stu-id="f5df5-113">You can use the [**gluErrorString**](gluerrorstring.md) GLU function to obtain a descriptive string corresponding to the error code passed in.</span></span> <span data-ttu-id="f5df5-114">如需 **gluErrorString** 的詳細資訊，請參閱 [處理錯誤](handling-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="f5df5-114">For more information on **gluErrorString**, see [Handling Errors](handling-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="f5df5-115">如果偵測到錯誤，X.GLU 隊函數通常會傳回錯誤值。</span><span class="sxs-lookup"><span data-stu-id="f5df5-115">GLU functions often return error values if an error is detected.</span></span> <span data-ttu-id="f5df5-116">此外，OpenGL 公用程式程式庫會定義錯誤碼 X.GLU 隊 \_ 無效 \_ 的列舉、X.glu 隊 \_ 無效 \_ 值和 x.glu 隊 \_ \_ 記憶體不足 \_ ，其意義與相關的 OpenGL 錯誤碼相同。</span><span class="sxs-lookup"><span data-stu-id="f5df5-116">Also, the OpenGL Utility library defines the error codes GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY, which have the same meaning as the related OpenGL error codes.</span></span>

 

 

 




