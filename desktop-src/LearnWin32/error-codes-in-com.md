---
title: COM 中的錯誤碼
description: COM 中的錯誤碼
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733cbe0799a22b0f0c01ee9cb226ad7e0b8660da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103956"
---
# <a name="error-codes-in-com"></a><span data-ttu-id="db9b1-103">COM 中的錯誤碼</span><span class="sxs-lookup"><span data-stu-id="db9b1-103">Error Codes in COM</span></span>

<span data-ttu-id="db9b1-104">為了表示成功或失敗，COM 方法和函式會傳回 **HRESULT** 類型的值。</span><span class="sxs-lookup"><span data-stu-id="db9b1-104">To indicate success or failure, COM methods and functions return a value of type **HRESULT**.</span></span> <span data-ttu-id="db9b1-105">**HRESULT** 是32位的整數。</span><span class="sxs-lookup"><span data-stu-id="db9b1-105">An **HRESULT** is a 32-bit integer.</span></span> <span data-ttu-id="db9b1-106">**HRESULT** 的高序位位表示成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="db9b1-106">The high-order bit of the **HRESULT** signals success or failure.</span></span> <span data-ttu-id="db9b1-107">零 (0) 表示成功，1表示失敗。</span><span class="sxs-lookup"><span data-stu-id="db9b1-107">Zero (0) indicates success and 1 indicates failure.</span></span>

<span data-ttu-id="db9b1-108">這會產生下列數值範圍：</span><span class="sxs-lookup"><span data-stu-id="db9b1-108">This produces the following numeric ranges:</span></span>

-   <span data-ttu-id="db9b1-109">成功碼：0x0 –0x7FFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="db9b1-109">Success codes: 0x0–0x7FFFFFFF.</span></span>
-   <span data-ttu-id="db9b1-110">錯誤碼：0x80000000 –0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="db9b1-110">Error codes: 0x80000000–0xFFFFFFFF.</span></span>

<span data-ttu-id="db9b1-111">少數的 COM 方法不會傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="db9b1-111">A small number of COM methods do not return an **HRESULT** value.</span></span> <span data-ttu-id="db9b1-112">例如， [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 和 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 方法會傳回不帶正負號的 long 值。</span><span class="sxs-lookup"><span data-stu-id="db9b1-112">For example, the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods return unsigned long values.</span></span> <span data-ttu-id="db9b1-113">但是傳回錯誤碼的每個 COM 方法都會傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="db9b1-113">But every COM method that returns an error code does so by returning an **HRESULT** value.</span></span>

<span data-ttu-id="db9b1-114">若要檢查 COM 方法是否成功，請檢查傳回之 **HRESULT** 的高序位位。</span><span class="sxs-lookup"><span data-stu-id="db9b1-114">To check whether a COM method succeeds, examine the high-order bit of the returned **HRESULT**.</span></span> <span data-ttu-id="db9b1-115">Windows SDK 標頭提供兩種可簡化此作業的宏： [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded) 的宏和 [**失敗**](/windows/desktop/api/winerror/nf-winerror-failed) 的宏。</span><span class="sxs-lookup"><span data-stu-id="db9b1-115">The Windows SDK headers provide two macros that make this easier: the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) macro and the [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="db9b1-116">如果 **HRESULT** 是成功碼，**成功** 的宏會傳回 **TRUE** ，如果是錯誤碼，則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="db9b1-116">The **SUCCEEDED** macro returns **TRUE** if an **HRESULT** is a success code and **FALSE** if it is an error code.</span></span> <span data-ttu-id="db9b1-117">下列範例會檢查 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 是否成功。</span><span class="sxs-lookup"><span data-stu-id="db9b1-117">The following example checks whether [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) succeeds.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



<span data-ttu-id="db9b1-118">有時候，測試反向條件會比較方便。</span><span class="sxs-lookup"><span data-stu-id="db9b1-118">Sometimes it is more convenient to test the inverse condition.</span></span> <span data-ttu-id="db9b1-119">[**失敗**](/windows/desktop/api/winerror/nf-winerror-failed)的宏會與 [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded)的相反。</span><span class="sxs-lookup"><span data-stu-id="db9b1-119">The [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro does the opposite of [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span></span> <span data-ttu-id="db9b1-120">它會針對錯誤碼傳回 **TRUE** ，並針對成功代碼傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="db9b1-120">It returns **TRUE** for an error code and **FALSE** for a success code.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



<span data-ttu-id="db9b1-121">稍後在本課程模組中，我們將探討如何結構您的程式碼來處理 COM 錯誤的一些實用建議。</span><span class="sxs-lookup"><span data-stu-id="db9b1-121">Later in this module, we will look at some practical advice for how to structure your code to handle COM errors.</span></span> <span data-ttu-id="db9b1-122"> (請參閱 [COM 中的錯誤處理](error-handling-in-com.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="db9b1-122">(See [Error Handling in COM](error-handling-in-com.md).)</span></span>

## <a name="next"></a><span data-ttu-id="db9b1-123">下一個</span><span class="sxs-lookup"><span data-stu-id="db9b1-123">Next</span></span>

[<span data-ttu-id="db9b1-124">在 COM 中建立物件</span><span class="sxs-lookup"><span data-stu-id="db9b1-124">Creating an Object in COM</span></span>](creating-an-object-in-com.md)

 

 
