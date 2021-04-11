---
description: 若要建立 Dynamic-Link 程式庫 (DLL) ，您必須建立一或多個原始程式碼檔案，而且可能是用來匯出函數的連結器檔案。
ms.assetid: b66ea0e8-84c3-40be-bf02-765b9dd61f9f
title: Dynamic-Link 程式庫建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12d296b1494cfcedcdfa823eb1a3dd4d408427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691567"
---
# <a name="dynamic-link-library-creation"></a><span data-ttu-id="1c131-103">Dynamic-Link 程式庫建立</span><span class="sxs-lookup"><span data-stu-id="1c131-103">Dynamic-Link Library Creation</span></span>

<span data-ttu-id="1c131-104">若要建立 Dynamic-Link 程式庫 (DLL) ，您必須建立一或多個原始程式碼檔案，而且可能是用來匯出函數的連結器檔案。</span><span class="sxs-lookup"><span data-stu-id="1c131-104">To create a Dynamic-Link Library (DLL), you must create one or more source code files, and possibly a linker file for exporting the functions.</span></span> <span data-ttu-id="1c131-105">如果您打算允許使用 DLL 的應用程式使用載入時間動態連結，您也必須建立匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="1c131-105">If you plan to allow applications that use your DLL to use load-time dynamic linking, you must also create an import library.</span></span>

## <a name="creating-source-files"></a><span data-ttu-id="1c131-106">建立原始檔</span><span class="sxs-lookup"><span data-stu-id="1c131-106">Creating Source Files</span></span>

<span data-ttu-id="1c131-107">DLL 的原始程式檔包含匯出的函式和資料、內建函式和資料，以及 DLL 的選擇性 [進入點函數](dynamic-link-library-entry-point-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="1c131-107">The source files for a DLL contain exported functions and data, internal functions and data, and an optional [entry-point function](dynamic-link-library-entry-point-function.md) for the DLL.</span></span> <span data-ttu-id="1c131-108">您可以使用任何支援建立以 Windows 為基礎之 Dll 的開發工具。</span><span class="sxs-lookup"><span data-stu-id="1c131-108">You may use any development tools that support the creation of Windows-based DLLs.</span></span>

<span data-ttu-id="1c131-109">如果多執行緒應用程式可能會使用您的 DLL，您應該將 DLL 設為「安全線程」。</span><span class="sxs-lookup"><span data-stu-id="1c131-109">If your DLL may be used by a multithreaded application, you should make your DLL "thread-safe".</span></span> <span data-ttu-id="1c131-110">您必須同步存取所有 DLL 的全域資料，以避免資料損毀。</span><span class="sxs-lookup"><span data-stu-id="1c131-110">You must synchronize access to all of the DLL's global data to avoid data corruption.</span></span> <span data-ttu-id="1c131-111">您也必須確定您只連結至安全線程的程式庫。</span><span class="sxs-lookup"><span data-stu-id="1c131-111">You must also ensure that you link only with libraries that are thread-safe as well.</span></span> <span data-ttu-id="1c131-112">例如，Microsoft Visual C++ 包含多個版本的 C 執行時間程式庫，其中一個不是安全線程，而兩個是。</span><span class="sxs-lookup"><span data-stu-id="1c131-112">For example, Microsoft Visual C++ contains multiple versions of the C Run-time Library, one that is not thread-safe and two that are.</span></span>

## <a name="exporting-functions"></a><span data-ttu-id="1c131-113">匯出函式</span><span class="sxs-lookup"><span data-stu-id="1c131-113">Exporting Functions</span></span>

<span data-ttu-id="1c131-114">如何指定要匯出 DLL 中的函式，取決於您用來開發的工具。</span><span class="sxs-lookup"><span data-stu-id="1c131-114">How you specify which functions in a DLL should be exported depends on the tools that you are using for development.</span></span> <span data-ttu-id="1c131-115">某些編譯器可讓您使用函式宣告中的修飾詞，直接在原始程式碼中匯出函式。</span><span class="sxs-lookup"><span data-stu-id="1c131-115">Some compilers allow you to export a function directly in the source code by using a modifier in the function declaration.</span></span> <span data-ttu-id="1c131-116">其他時候，您必須在傳遞給連結器的檔案中指定匯出。</span><span class="sxs-lookup"><span data-stu-id="1c131-116">Other times, you must specify exports in a file that you pass to the linker.</span></span>

<span data-ttu-id="1c131-117">例如，使用 Visual C++，有兩種可能的方式可以匯出 DLL 函式：使用 [**\_ \_ declspec (dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx)修飾詞或模組定義 ( .def) 檔。</span><span class="sxs-lookup"><span data-stu-id="1c131-117">For example, using Visual C++, there are two possible ways to export DLL functions: with the [**\_\_declspec(dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx) modifier or with a module-definition (.def) file.</span></span> <span data-ttu-id="1c131-118">如果您使用 **\_ \_ declspec (dllexport)** 修飾詞，就不需要使用 .def 檔。</span><span class="sxs-lookup"><span data-stu-id="1c131-118">If you use the **\_\_declspec(dllexport)** modifier, it is not necessary to use a .def file.</span></span> <span data-ttu-id="1c131-119">如需詳細資訊，請參閱 [從 DLL 匯出](/cpp/build/exporting-from-a-dll?view=vs-2019)。</span><span class="sxs-lookup"><span data-stu-id="1c131-119">For more information, see [Exporting from a DLL](/cpp/build/exporting-from-a-dll?view=vs-2019).</span></span>

## <a name="creating-an-import-library"></a><span data-ttu-id="1c131-120">建立匯入程式庫</span><span class="sxs-lookup"><span data-stu-id="1c131-120">Creating an Import Library</span></span>

<span data-ttu-id="1c131-121">匯入程式庫 ( .lib) 檔案包含連結器解析匯出 DLL 函式外部參考所需的資訊，因此系統可以在執行時間找到指定的 DLL 和匯出的 DLL 函式。</span><span class="sxs-lookup"><span data-stu-id="1c131-121">An import library (.lib) file contains information the linker needs to resolve external references to exported DLL functions, so the system can locate the specified DLL and exported DLL functions at run time.</span></span> <span data-ttu-id="1c131-122">當您建立 DLL 時，可以建立 DLL 的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="1c131-122">You can create an import library for your DLL when you build your DLL.</span></span>

<span data-ttu-id="1c131-123">如需詳細資訊，請參閱 [建立匯入程式庫和匯出](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019)檔案。</span><span class="sxs-lookup"><span data-stu-id="1c131-123">For more information, see [Building an Import Library and Export File](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019).</span></span>

## <a name="using-an-import-library"></a><span data-ttu-id="1c131-124">使用匯入程式庫</span><span class="sxs-lookup"><span data-stu-id="1c131-124">Using an Import Library</span></span>

<span data-ttu-id="1c131-125">例如，若要呼叫 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數，您必須將程式碼與匯入程式庫的程式庫連結。</span><span class="sxs-lookup"><span data-stu-id="1c131-125">For example, to call the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function, you must link your code with the import library User32.lib.</span></span> <span data-ttu-id="1c131-126">原因是， **CreateWindow** 位於名為 User32.dll 的系統 DLL 中，而 mscoree.dll 則是用來解析程式代碼中 User32.dll 匯出函式之呼叫的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="1c131-126">The reason is that **CreateWindow** resides in a system DLL named User32.dll, and User32.lib is the import library used to resolve the calls to exported functions in User32.dll in your code.</span></span> <span data-ttu-id="1c131-127">連結器會建立一個資料表，其中包含每個函式呼叫的位址。</span><span class="sxs-lookup"><span data-stu-id="1c131-127">The linker creates a table that contains the address of each function call.</span></span> <span data-ttu-id="1c131-128">載入 DLL 時，會修正 DLL 中函式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="1c131-128">Calls to functions in a DLL will be fixed up when the DLL is loaded.</span></span> <span data-ttu-id="1c131-129">當系統初始化程式時，它會載入 User32.dll，因為進程相依于該 DLL 中匯出的函式，並且會更新函式位址資料表中的專案。</span><span class="sxs-lookup"><span data-stu-id="1c131-129">While the system is initializing the process, it loads User32.dll because the process depends on exported functions in that DLL, and it updates the entries in the function address table.</span></span> <span data-ttu-id="1c131-130">所有的 **CreateWindow** 呼叫都會叫用從 User32.dll 匯出的函式。</span><span class="sxs-lookup"><span data-stu-id="1c131-130">All calls to **CreateWindow** invoke the function exported from User32.dll.</span></span>

<span data-ttu-id="1c131-131">如需詳細資訊，請參閱 [以 DLL 隱含連結](/previous-versions/d14wsce5(v=vs.140))。</span><span class="sxs-lookup"><span data-stu-id="1c131-131">For information, see [Linking Implicitly with a DLL](/previous-versions/d14wsce5(v=vs.140)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c131-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c131-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c131-133">建立簡單的動態連結程式庫</span><span class="sxs-lookup"><span data-stu-id="1c131-133">Creating a Simple Dynamic-link Library</span></span>](creating-a-simple-dynamic-link-library.md)
</dt> <dt>

[<span data-ttu-id="1c131-134">Dll (Visual C++) </span><span class="sxs-lookup"><span data-stu-id="1c131-134">DLLs (Visual C++)</span></span>](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
