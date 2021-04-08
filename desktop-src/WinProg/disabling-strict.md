---
title: 停用 STRICT
description: 若要停用嚴格類型檢查，請定義符號名稱 NO \_ strict。 在 Visual C/c + + 中，您也可以指定/DNO \_ STRICT 作為編譯器選項，在命令列或 makefile 中指定這個定義。
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674184"
---
# <a name="disabling-strict"></a><span data-ttu-id="6870f-104">停用 STRICT</span><span class="sxs-lookup"><span data-stu-id="6870f-104">Disabling STRICT</span></span>

<span data-ttu-id="6870f-105">若要停用 **嚴格** 類型檢查，請定義符號名稱 **NO \_ strict**。</span><span class="sxs-lookup"><span data-stu-id="6870f-105">To disable **STRICT** type checking, define the symbol name **NO\_STRICT**.</span></span> <span data-ttu-id="6870f-106">在 Visual C/c + + 中，您也可以指定 **/DNO \_ STRICT** 作為編譯器選項，在命令列或 makefile 中指定這個定義。</span><span class="sxs-lookup"><span data-stu-id="6870f-106">In Visual C/C++, you can also specify this definition on the command line or in a makefile by specifying **/DNO\_STRICT** as a compiler option.</span></span>

<span data-ttu-id="6870f-107">若要針對逐檔案定義 **不 \_ 嚴格** 的，請在包含 Windows .h 之前插入 **\# 定義** 語句：</span><span class="sxs-lookup"><span data-stu-id="6870f-107">To define **NO\_STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define NO_STRICT
#include <windows.h>
```



<span data-ttu-id="6870f-108">為了獲得最佳結果，您也應該將錯誤訊息的警告層級設定為至少 **/W3**。</span><span class="sxs-lookup"><span data-stu-id="6870f-108">For best results, you should also set the warning level for error messages to at least **/W3**.</span></span> <span data-ttu-id="6870f-109">這對 Windows 的應用程式一律是建議的作法，因為會造成警告的編碼做法 (例如，傳遞錯誤的參數數目) 通常會在執行時間造成嚴重錯誤（如果未修正）。</span><span class="sxs-lookup"><span data-stu-id="6870f-109">This is always advisable with applications for Windows, because a coding practice that causes a warning (for example, passing the wrong number of parameters) usually causes a fatal error at run time if it is not corrected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6870f-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="6870f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6870f-111">啟用 STRICT</span><span class="sxs-lookup"><span data-stu-id="6870f-111">Enabling STRICT</span></span>](enabling-strict.md)
</dt> <dt>

[<span data-ttu-id="6870f-112">嚴格合規性</span><span class="sxs-lookup"><span data-stu-id="6870f-112">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 




