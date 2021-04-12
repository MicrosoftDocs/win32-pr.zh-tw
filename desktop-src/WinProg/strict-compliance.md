---
title: 嚴格合規性
description: 當您啟用 STRICT 類型檢查時，會成功編譯的部分原始程式碼可能會產生錯誤訊息。
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375841"
---
# <a name="strict-compliance"></a><span data-ttu-id="3ccc5-103">嚴格合規性</span><span class="sxs-lookup"><span data-stu-id="3ccc5-103">STRICT Compliance</span></span>

<span data-ttu-id="3ccc5-104">當您啟用 **STRICT** 類型檢查時，會成功編譯的部分原始程式碼可能會產生錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-104">Some source code that compiles successfully might produce error messages when you enable **STRICT** type checking.</span></span> <span data-ttu-id="3ccc5-105">下列各節說明在啟用 **STRICT** 時進行程式碼編譯的基本需求。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-105">The following sections describe the minimal requirements for making your code compile when **STRICT** is enabled.</span></span> <span data-ttu-id="3ccc5-106">建議執行其他步驟，尤其是為了產生可移植的程式碼。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-106">Additional steps are recommended, especially to produce portable code.</span></span>

## <a name="general-requirements"></a><span data-ttu-id="3ccc5-107">一般需求</span><span class="sxs-lookup"><span data-stu-id="3ccc5-107">General Requirements</span></span>

<span data-ttu-id="3ccc5-108">主要需求是您必須宣告正確的控制碼類型和函式指標，而不是依賴更多一般類型。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-108">The principal requirement is that you must declare correct handle types and function pointers instead of relying on more general types.</span></span> <span data-ttu-id="3ccc5-109">您無法使用另一個需要的控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-109">You cannot use one handle type where another is expected.</span></span> <span data-ttu-id="3ccc5-110">這也表示您可能必須變更函式宣告，並使用更多型別轉換。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-110">This also means that you may have to change function declarations and use more type casts.</span></span>

<span data-ttu-id="3ccc5-111">為了獲得最佳結果，只有在必要時才使用泛型 **控制碼** 類型。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-111">For best results, the generic **HANDLE** type should be used only when necessary.</span></span>

## <a name="declaring-functions-within-your-application"></a><span data-ttu-id="3ccc5-112">在您的應用程式中宣告函數</span><span class="sxs-lookup"><span data-stu-id="3ccc5-112">Declaring Functions Within Your Application</span></span>

<span data-ttu-id="3ccc5-113">確定已宣告所有的應用程式函數。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-113">Make sure all application functions are declared.</span></span> <span data-ttu-id="3ccc5-114">建議將所有函式宣告放在 include 檔案中，因為您可以輕鬆地掃描您的宣告，並尋找應變更的參數和傳回類型。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-114">Placing all function declarations in an include file is recommended because you can easily scan your declarations and look for parameter and return types that should be changed.</span></span>

<span data-ttu-id="3ccc5-115">如果您使用 **/Zg** 編譯器選項來建立函式的標頭檔，請記住，您將會根據您是否已啟用 **STRICT** 型別檢查來取得不同的結果。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-115">If you use the **/Zg** compiler option to create header files for your functions, remember that you will get different results depending on whether you have enabled **STRICT** type checking.</span></span> <span data-ttu-id="3ccc5-116">在 **STRICT** 停用的情況下，所有的控制碼類型都會產生相同的基底類型。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-116">With **STRICT** disabled, all handle types generate the same base type.</span></span> <span data-ttu-id="3ccc5-117">在 **STRICT** 啟用的情況下，它們會產生不同的基底類型。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-117">With **STRICT** enabled, they generate different base types.</span></span> <span data-ttu-id="3ccc5-118">若要避免發生衝突，您必須在每次啟用或停用 **STRICT** 時重新建立標頭檔，或編輯標頭檔以使用類型 **HWND**、 **HDC**、 **控制碼** 等，而不是基底類型。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-118">To avoid conflict, you need to re-create the header file each time you enable or disable **STRICT**, or edit the header file to use the types **HWND**, **HDC**, **HANDLE**, and so on, instead of the base types.</span></span>

<span data-ttu-id="3ccc5-119">您從 Windows 複製到原始程式碼的任何函式宣告可能已變更，而您的本機宣告可能已過期。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-119">Any function declarations that you copied from Windows.h into your source code may have changed, and your local declaration may be out of date.</span></span> <span data-ttu-id="3ccc5-120">移除本機宣告。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-120">Remove your local declaration.</span></span>

## <a name="types-that-require-casts"></a><span data-ttu-id="3ccc5-121">需要轉換的類型</span><span class="sxs-lookup"><span data-stu-id="3ccc5-121">Types that Require Casts</span></span>

<span data-ttu-id="3ccc5-122">某些函式具有泛型傳回類型或參數。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-122">Some functions have generic return types or parameters.</span></span> <span data-ttu-id="3ccc5-123">例如，視內容而定， [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式會傳回可能任意數目之類型的資料。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-123">For example, the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function returns data that may be any number of types, depending on the context.</span></span> <span data-ttu-id="3ccc5-124">當您在原始程式碼中看到任何這些函式時，請確定您使用正確的型別轉換，而且它盡可能明確。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-124">When you see any of these functions in your source code, make sure that you use the correct type cast and that it is as specific as possible.</span></span> <span data-ttu-id="3ccc5-125">下列清單是這些函數的範例。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-125">The following list is an example of these functions.</span></span>

-   [<span data-ttu-id="3ccc5-126">**LocalLock**</span><span class="sxs-lookup"><span data-stu-id="3ccc5-126">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [<span data-ttu-id="3ccc5-127">**GlobalLock**</span><span class="sxs-lookup"><span data-stu-id="3ccc5-127">**GlobalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [<span data-ttu-id="3ccc5-128">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="3ccc5-128">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [<span data-ttu-id="3ccc5-129">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="3ccc5-129">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [<span data-ttu-id="3ccc5-130">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="3ccc5-130">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="3ccc5-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="3ccc5-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [<span data-ttu-id="3ccc5-132">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="3ccc5-132">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

<span data-ttu-id="3ccc5-133">當您呼叫 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)、 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)或 [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)時，應該先將結果轉換成 **UINT \_ 指標** 類型。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-133">When you call [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), or [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), you should first cast the result to type **UINT\_PTR**.</span></span> <span data-ttu-id="3ccc5-134">針對傳回 **LRESULT** 或 **LONG \_ PTR** 值的任何函式，您必須採取類似的步驟，其中結果包含控制碼。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-134">You need to take similar steps for any function that returns an **LRESULT** or **LONG\_PTR** value, where the result contains a handle.</span></span> <span data-ttu-id="3ccc5-135">這是撰寫可移植程式碼的必要項，因為控制碼的大小會隨著 Windows 版本而有所不同。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-135">This is necessary for writing portable code because the size of a handle varies, depending on the version of Windows.</span></span> <span data-ttu-id="3ccc5-136"> (**UINT \_ PTR**) 轉換可確保正確的轉換。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-136">The (**UINT\_PTR**) cast ensures proper conversion.</span></span> <span data-ttu-id="3ccc5-137">下列程式碼顯示 **SendMessage** 將控制碼傳回給筆刷的範例：</span><span class="sxs-lookup"><span data-stu-id="3ccc5-137">The following code shows an example in which **SendMessage** returns a handle to a brush:</span></span>


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



<span data-ttu-id="3ccc5-138">[ **CreateWindow** ] 和 [ **CreateWindowEx** ] 參數 *hmenu* 有時會用來傳遞整數控制項識別碼 (識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-138">The **CreateWindow** and **CreateWindowEx** parameter *hmenu* is sometimes used to pass an integer control identifier (ID).</span></span> <span data-ttu-id="3ccc5-139">在此情況下，您必須將識別碼轉換成 **HMENU** 型別：</span><span class="sxs-lookup"><span data-stu-id="3ccc5-139">In this case, you must cast the ID to an **HMENU** type:</span></span>


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a><span data-ttu-id="3ccc5-140">其他考量</span><span class="sxs-lookup"><span data-stu-id="3ccc5-140">Additional Considerations</span></span>

<span data-ttu-id="3ccc5-141">若要充分利用 **嚴格** 的型別檢查，您應該遵循其他指導方針。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-141">To get the most benefit from **STRICT** type checking, there are additional guidelines you should follow.</span></span> <span data-ttu-id="3ccc5-142">如果您進行下列變更，您的程式碼將會在未來的 Windows 版本中更容易移植。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-142">Your code will be more portable in future versions of Windows if you make the following changes.</span></span>

<span data-ttu-id="3ccc5-143">**WPARAM**、 **LPARAM**、 **LRESULT** 和 **LPVOID** 類型都是多型 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-143">The types **WPARAM**, **LPARAM**, **LRESULT**, and **LPVOID** are *polymorphic data types*.</span></span> <span data-ttu-id="3ccc5-144">它們會在不同的時間保存不同類型的資料，即使已啟用 **STRICT** 型別檢查也是一樣。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-144">They hold different kinds of data at different times, even when **STRICT** type checking is enabled.</span></span> <span data-ttu-id="3ccc5-145">若要取得類型檢查的優點，您應該儘快轉換這些類型的值。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-145">To get the benefit of type checking, you should cast values of these types as soon as possible.</span></span> <span data-ttu-id="3ccc5-146"> (請注意，message crackers 會以可移植的方式自動為您重新轉換 *wParam* 和 *lParam* ) 。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-146">(Note that message crackers automatically recast *wParam* and *lParam* for you in a portable way.)</span></span>

<span data-ttu-id="3ccc5-147">請特別小心區別 **HMODULE** 和 **HINSTANCE** 類型。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-147">Take special care to distinguish **HMODULE** and **HINSTANCE** types.</span></span> <span data-ttu-id="3ccc5-148">即使已啟用 **STRICT** ，它們也會定義為相同的基底類型。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-148">Even with **STRICT** enabled, they are defined as the same base type.</span></span> <span data-ttu-id="3ccc5-149">大部分的核心模組管理函式都會使用 **HINSTANCE** 類型，但有一些函數會傳回或只接受 **HMODULE** 類型。</span><span class="sxs-lookup"><span data-stu-id="3ccc5-149">Most kernel module management functions use **HINSTANCE** types, but there are a few functions that return or accept only **HMODULE** types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ccc5-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ccc5-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ccc5-151">停用 STRICT</span><span class="sxs-lookup"><span data-stu-id="3ccc5-151">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="3ccc5-152">啟用 STRICT</span><span class="sxs-lookup"><span data-stu-id="3ccc5-152">Enabling STRICT</span></span>](enabling-strict.md)
</dt> </dl>

 

 