---
title: ADSI 錯誤碼
description: 所有 ADSI 錯誤碼都會以 COM HRESULT 值的形式傳回。
ms.assetid: 573889e4-37af-4aca-afd7-ef06bcf8aa0d
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、參考、錯誤碼
- 錯誤碼 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d9383998429b2ec64dd16fbed0d0df314f0d72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839247"
---
# <a name="adsi-error-codes"></a><span data-ttu-id="bece9-105">ADSI 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bece9-105">ADSI Error Codes</span></span>

<span data-ttu-id="bece9-106">所有 ADSI 錯誤碼都會以 COM **HRESULT** 值的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="bece9-106">All ADSI error codes are returned as COM **HRESULT** values.</span></span> <span data-ttu-id="bece9-107">它們可以分組為下列四種類型：</span><span class="sxs-lookup"><span data-stu-id="bece9-107">They can be grouped into the following four types:</span></span>

-   [<span data-ttu-id="bece9-108">一般 COM 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bece9-108">Generic COM error codes</span></span>](generic-com-error-codes.md)
-   [<span data-ttu-id="bece9-109">一般 ADSI 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bece9-109">Generic ADSI error codes</span></span>](generic-adsi-error-codes.md)
-   [<span data-ttu-id="bece9-110">ADSI 的 Win32 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bece9-110">Win32 error codes for ADSI</span></span>](win32-error-codes-for-adsi.md)
-   [<span data-ttu-id="bece9-111">ADSI 的 LDAP 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bece9-111">LDAP error codes for ADSI</span></span>](ldap-error-codes-for-adsi.md)

<span data-ttu-id="bece9-112">此外，某些介面會提供其他錯誤資訊，稱為 ADSI 擴充的錯誤訊息，可使用 [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) 函式取得。</span><span class="sxs-lookup"><span data-stu-id="bece9-112">In addition, certain interfaces provide additional error information, known as ADSI extended error messages, which can be obtained using the [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) function.</span></span>

<span data-ttu-id="bece9-113">最後，本節所示的 c + + [範例程式碼](code-example-for-working-with-adsi-error-messages.md) 會示範如何工作 ADSI 錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="bece9-113">Finally, the C++ [example code](code-example-for-working-with-adsi-error-messages.md) shown in this section shows how to work ADSI error messages.</span></span>

 

 




