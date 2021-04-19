---
description: Windows 執行階段字串的控制碼。
ms.assetid: 763ACE57-EFDD-482E-851E-668D7756C5DF
title: 'HSTRING (Hstring) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9e73d7627a4bab8f02a95056e5b208569d922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970996"
---
# <a name="hstring"></a><span data-ttu-id="82465-103">HSTRING</span><span class="sxs-lookup"><span data-stu-id="82465-103">HSTRING</span></span>

<span data-ttu-id="82465-104">Windows 執行階段字串的控制碼。</span><span class="sxs-lookup"><span data-stu-id="82465-104">A handle to a Windows Runtime string.</span></span>


```C++
typedef HSTRING__* HSTRING;
```



## <a name="remarks"></a><span data-ttu-id="82465-105">備註</span><span class="sxs-lookup"><span data-stu-id="82465-105">Remarks</span></span>

<span data-ttu-id="82465-106">使用 **HSTRING** 代表 Windows 執行階段中的不可變字串。</span><span class="sxs-lookup"><span data-stu-id="82465-106">Use **HSTRING** to represent immutable strings in the Windows Runtime.</span></span>

<span data-ttu-id="82465-107">JavaScript 和其他語言（例如 C 和 \# Microsoft Visual Basic）都可以使用使用 **HSTRING** 表示的字串。</span><span class="sxs-lookup"><span data-stu-id="82465-107">JavaScript and other languages, such as C\#, and Microsoft Visual Basic, can use strings that are represented by using **HSTRING**.</span></span> <span data-ttu-id="82465-108">下表顯示 **HSTRING** 如何以其他語言表示。</span><span class="sxs-lookup"><span data-stu-id="82465-108">The following table shows how an **HSTRING** is represented in other languages.</span></span>



| <span data-ttu-id="82465-109">程式設計語言</span><span class="sxs-lookup"><span data-stu-id="82465-109">Programming Language</span></span>                                                                    | <span data-ttu-id="82465-110">字串表示</span><span class="sxs-lookup"><span data-stu-id="82465-110">String Representation</span></span>                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="82465-111">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="82465-111">C++/WinRT</span></span>](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt)              | <span data-ttu-id="82465-112">[winrt：： hstring](/uwp/cpp-ref-for-winrt/hstring) 類別</span><span class="sxs-lookup"><span data-stu-id="82465-112">[winrt::hstring](/uwp/cpp-ref-for-winrt/hstring) class</span></span>     |
| <span data-ttu-id="82465-113">Visual C++ 元件延伸模組 ([c + +/cx](/cpp/cppcx/visual-c-language-reference-c-cx)) </span><span class="sxs-lookup"><span data-stu-id="82465-113">Visual C++ component extensions ([C++/CX](/cpp/cppcx/visual-c-language-reference-c-cx))</span></span> | <span data-ttu-id="82465-114">[Platform：： String](/cpp/cppcx/platform-string-class) 類別</span><span class="sxs-lookup"><span data-stu-id="82465-114">[Platform::String](/cpp/cppcx/platform-string-class) class</span></span> |
| <span data-ttu-id="82465-115">JavaScript</span><span class="sxs-lookup"><span data-stu-id="82465-115">JavaScript</span></span>                                                                              | <span data-ttu-id="82465-116">字串物件</span><span class="sxs-lookup"><span data-stu-id="82465-116">String object</span></span>                                              |
| <span data-ttu-id="82465-117">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="82465-117">.NET Framework</span></span>                                                                          | <span data-ttu-id="82465-118">System.String 類別</span><span class="sxs-lookup"><span data-stu-id="82465-118">System.String class</span></span>                                        |



 

<span data-ttu-id="82465-119">**HSTRING** 控制碼是標準的控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="82465-119">The **HSTRING** handle is a standard handle type.</span></span> <span data-ttu-id="82465-120">就語義而言，包含 **Null** 值的 **HSTRING** 代表空字串，其中包含零個內容字元和一個結束的 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="82465-120">Semantically, an **HSTRING** containing the value **NULL** represents the empty string, which consists of zero content characters and a terminating **NULL** character.</span></span> <span data-ttu-id="82465-121">以零個字元透過 [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) 建立字串，會產生控制碼值 **Null**。</span><span class="sxs-lookup"><span data-stu-id="82465-121">Creating a string via [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) with zero characters will produce the handle value **NULL**.</span></span> <span data-ttu-id="82465-122">使用值 **Null** 來呼叫 [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer)時，將會傳回空字串的指標，該字串後面只有 **NUL** 終止字元。</span><span class="sxs-lookup"><span data-stu-id="82465-122">When calling [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) with the value **NULL**, a pointer to an empty string followed only by the **NUL** terminating character will be returned.</span></span> <span data-ttu-id="82465-123">沒有相異值可代表未初始化的 **HSTRING** 。</span><span class="sxs-lookup"><span data-stu-id="82465-123">No distinct value exists to represent an **HSTRING** that is uninitialized.</span></span>

<span data-ttu-id="82465-124">呼叫 [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) 函式來建立新的 **HSTRING**，然後呼叫 [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) 函式來釋放支援字串記憶體的參考。</span><span class="sxs-lookup"><span data-stu-id="82465-124">Call the [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) function to create a new **HSTRING**, and call the [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) function to release the reference to the backing string memory.</span></span> <span data-ttu-id="82465-125">呼叫 [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) 函式來建立字串參考，也稱為 *快速傳遞字串*。</span><span class="sxs-lookup"><span data-stu-id="82465-125">Call the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function to create a string reference, which is also called a *fast-pass string*.</span></span>

<span data-ttu-id="82465-126">藉由呼叫 [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)函數來複製 **HSTRING** 。</span><span class="sxs-lookup"><span data-stu-id="82465-126">Copy an **HSTRING** by calling the [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) function.</span></span>

<span data-ttu-id="82465-127">藉由呼叫 [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) 函數來串連兩個字串。</span><span class="sxs-lookup"><span data-stu-id="82465-127">Concatenate two strings by calling the [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) function.</span></span>

<span data-ttu-id="82465-128">藉由呼叫 [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) 函數來存取支援字串記憶體。</span><span class="sxs-lookup"><span data-stu-id="82465-128">Access the backing string memory by calling the [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) function.</span></span>

<span data-ttu-id="82465-129">**HSTRING** 可以儲存和使用內嵌的 **NUL** 字元。</span><span class="sxs-lookup"><span data-stu-id="82465-129">**HSTRING** can store and use embedded **NUL** characters.</span></span> <span data-ttu-id="82465-130">使用 [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) 函式在使用可能產生非預期結果的任何函式之前，先檢查內嵌的 **NUL** 字元。</span><span class="sxs-lookup"><span data-stu-id="82465-130">Use the [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) function to check for embedded **NUL** characters before using any functions which may produce unexpected results.</span></span> <span data-ttu-id="82465-131">例如，大部分的 Windows 函式會使用 **LPCWSTR** 做為輸入參數，而且只會計算字串的長度，直到遇到第一個 **NUL** 為止。</span><span class="sxs-lookup"><span data-stu-id="82465-131">For example, most of the Windows functions use **LPCWSTR** as an input parameter, and they compute the length of the string only until the first **NUL** is encountered.</span></span>

<span data-ttu-id="82465-132">支援字串必須維持不變且以 null 終止。</span><span class="sxs-lookup"><span data-stu-id="82465-132">The backing string must remain immutable and null-terminated.</span></span> <span data-ttu-id="82465-133">當呼叫程式碼使用 [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) 函式來建立字串參考時，包含支援字串表示的記憶體是由呼叫端所擁有。</span><span class="sxs-lookup"><span data-stu-id="82465-133">When calling code creates a string reference by using the [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) function, the memory containing the backing string representation is owned by the caller.</span></span> <span data-ttu-id="82465-134">Windows 執行階段依賴原始字串的內容保持不變。</span><span class="sxs-lookup"><span data-stu-id="82465-134">The Windows Runtime relies on the contents of the original string to remain unchanged.</span></span> <span data-ttu-id="82465-135">將字串參考傳遞至 Windows 執行階段時，呼叫端必須負責確保字串的內容不會改變，而且會在呼叫期間以 **NUL** 終止。</span><span class="sxs-lookup"><span data-stu-id="82465-135">When passing a string reference into the Windows Runtime, it is the caller’s responsibility to ensure that the string’s contents are unchanging and **NUL** terminated for the duration of the call.</span></span> <span data-ttu-id="82465-136">當呼叫傳回時，Windows 執行階段會釋放字串參考的所有參考。</span><span class="sxs-lookup"><span data-stu-id="82465-136">The Windows Runtime releases all references to the string reference when the call returns.</span></span>

<span data-ttu-id="82465-137">當您以 out 參數的形式接收 **HSTRING** 時，最好在完成時將控制碼設為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="82465-137">When you receive an **HSTRING** as an out parameter, it is good practice to set the handle to **NULL** when you are finished with it.</span></span>

<span data-ttu-id="82465-138">呼叫 [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) 函式來配置可變動的字串緩衝區，您可用來建立不可變的 **HSTRING**。</span><span class="sxs-lookup"><span data-stu-id="82465-138">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to allocate a mutable string buffer that you can use to create an immutable **HSTRING**.</span></span> <span data-ttu-id="82465-139">當您完成填入緩衝區時，就會呼叫 [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) 函數來建立 **HSTRING**。</span><span class="sxs-lookup"><span data-stu-id="82465-139">When you have finished populating the buffer, you call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) function to create the **HSTRING**.</span></span> <span data-ttu-id="82465-140">這兩個階段的結構模式會啟用類似于「字串產生器」的功能。</span><span class="sxs-lookup"><span data-stu-id="82465-140">This two-phase construction pattern enables functionality that is similar to a "string builder."</span></span>

## <a name="requirements"></a><span data-ttu-id="82465-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="82465-141">Requirements</span></span>



| <span data-ttu-id="82465-142">需求</span><span class="sxs-lookup"><span data-stu-id="82465-142">Requirement</span></span> | <span data-ttu-id="82465-143">值</span><span class="sxs-lookup"><span data-stu-id="82465-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="82465-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82465-144">Minimum supported client</span></span><br/> | <span data-ttu-id="82465-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="82465-145">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="82465-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82465-146">Minimum supported server</span></span><br/> | <span data-ttu-id="82465-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="82465-147">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="82465-148">標頭</span><span class="sxs-lookup"><span data-stu-id="82465-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="82465-149"><dt>Hstring。h</dt></span><span class="sxs-lookup"><span data-stu-id="82465-149"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82465-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82465-150">See also</span></span>

<dl> <span data-ttu-id="82465-151"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="82465-151"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="82465-152">**WindowsCreateString**</span><span class="sxs-lookup"><span data-stu-id="82465-152">**WindowsCreateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowscreatestring)
</dt> <dt>

[<span data-ttu-id="82465-153">**WindowsDeleteString**</span><span class="sxs-lookup"><span data-stu-id="82465-153">**WindowsDeleteString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsdeletestring)
</dt> <dt>

[<span data-ttu-id="82465-154">**WindowsDuplicateString**</span><span class="sxs-lookup"><span data-stu-id="82465-154">**WindowsDuplicateString**</span></span>](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring)
</dt> <dt>

[<span data-ttu-id="82465-155">**WindowsPreallocateStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="82465-155">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> </dl>

 

 
