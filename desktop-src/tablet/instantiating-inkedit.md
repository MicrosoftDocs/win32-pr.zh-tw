---
description: 本主題說明可具現化 InkEdit 控制項的各種方式。
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: 具現化 InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde7e94566b076a4d9d6f6928fc08199ee71fa19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469184"
---
# <a name="instantiating-inkedit"></a><span data-ttu-id="eeb24-103">具現化 InkEdit</span><span class="sxs-lookup"><span data-stu-id="eeb24-103">Instantiating InkEdit</span></span>

<span data-ttu-id="eeb24-104">本主題說明可具現化 [InkEdit](inkedit-control.md) 控制項的各種方式。</span><span class="sxs-lookup"><span data-stu-id="eeb24-104">This topic describes the various ways that you can instantiate an [InkEdit](inkedit-control.md) control.</span></span>

## <a name="visual-basic-net-and-c"></a><span data-ttu-id="eeb24-105">Visual Basic .NET 和 C\#</span><span class="sxs-lookup"><span data-stu-id="eeb24-105">Visual Basic .NET and C\#</span></span>

<span data-ttu-id="eeb24-106">如果您正在使用 Microsoft Visual Basic .NET 或 C \# ，請從 Visual Studio 的工具箱將 [InkEdit](./inkedit-control.md) 控制項拖曳至您想要顯示控制項的表單或頁面。</span><span class="sxs-lookup"><span data-stu-id="eeb24-106">If you are working with Microsoft Visual Basic .NET or C\#, drag the [InkEdit](./inkedit-control.md) control from the Toolbox in Visual Studio to the form or page where you want the control to appear.</span></span>

## <a name="win32c"></a><span data-ttu-id="eeb24-107">Win32/c + +</span><span class="sxs-lookup"><span data-stu-id="eeb24-107">Win32/C++</span></span>

<span data-ttu-id="eeb24-108">[InkEdit](inkedit-control-reference.md)控制項是 Rich Edit 4.5 Win32 OLE 可嵌入控制項的超級類別。</span><span class="sxs-lookup"><span data-stu-id="eeb24-108">The [InkEdit](inkedit-control-reference.md) control is a superclass of the Rich Edit 4.5 Win32 OLE embeddable control.</span></span>

<span data-ttu-id="eeb24-109">Win32 應用程式會藉由呼叫[ () 的 CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa)將[InkEdit](inkedit-control-reference.md)控制項具現化，並以視窗類別的形式傳遞 InkEdit。</span><span class="sxs-lookup"><span data-stu-id="eeb24-109">Win32 applications instantiate the [InkEdit](inkedit-control-reference.md) control by calling [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) and passing INKEDIT as the window class.</span></span> <span data-ttu-id="eeb24-110">INKEDIT 定義于筆跡中。</span><span class="sxs-lookup"><span data-stu-id="eeb24-110">INKEDIT is defined in InkEd.h.</span></span> <span data-ttu-id="eeb24-111">建立控制項之後，您可以使用訊息「與」控制項「交談」。</span><span class="sxs-lookup"><span data-stu-id="eeb24-111">After the control is created, you can "talk" to the control with messages.</span></span> <span data-ttu-id="eeb24-112">豐富的編輯訊息 (EM \_ \*) 會從 InkEdit 傳遞至非改變的 rich edit; 所有現有的豐富編輯功能都可以使用。</span><span class="sxs-lookup"><span data-stu-id="eeb24-112">Rich Edit messages (EM\_\*) are passed from InkEdit to Rich Edit unaltered; all of the existing Rich Edit functionality is available.</span></span>

<span data-ttu-id="eeb24-113">若要建立 [InkEdit](inkedit-control-reference.md) 控制項，請呼叫 [CreateWindow () ](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數，並指定 InkEdit 視窗類別。</span><span class="sxs-lookup"><span data-stu-id="eeb24-113">To create an [InkEdit](inkedit-control-reference.md) control, call the [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) function, specifying the InkEdit window class.</span></span> <span data-ttu-id="eeb24-114">使用 [LoadLibrary () ](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 註冊 InkEd.dll。</span><span class="sxs-lookup"><span data-stu-id="eeb24-114">Use [LoadLibrary()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to register InkEd.dll.</span></span> <span data-ttu-id="eeb24-115">\_為視窗類別參數指定 INKEDIT 類別定義的常數，並使用下列範例中所指定的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="eeb24-115">Specify the INKEDIT\_CLASS defined constant for the window class parameter and use the window styles as specified in the following examples.</span></span>

### <a name="instantiating-a-multiline-inkedit-control"></a><span data-ttu-id="eeb24-116">具現化多行 InkEdit 控制項</span><span class="sxs-lookup"><span data-stu-id="eeb24-116">Instantiating a Multiline InkEdit Control</span></span>


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER|ES_MULTILINE,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



### <a name="instantiating-a-single-line-inkedit-control"></a><span data-ttu-id="eeb24-117">將 Single-Line InkEdit 控制項具現化</span><span class="sxs-lookup"><span data-stu-id="eeb24-117">Instantiating a Single-Line InkEdit Control</span></span>


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



> [!Note]  
> <span data-ttu-id="eeb24-118">不同于 RichEdit，您必須在建立[InkEdit](inkedit-control-reference.md)控制項之前務必先呼叫[CoInitialize () ](/windows/win32/api/objbase/nf-objbase-coinitialize) 。</span><span class="sxs-lookup"><span data-stu-id="eeb24-118">Unlike with RichEdit, you must be sure to call [CoInitialize()](/windows/win32/api/objbase/nf-objbase-coinitialize) before creating the [InkEdit](inkedit-control-reference.md) control.</span></span> <span data-ttu-id="eeb24-119">當您的應用程式關閉時，請呼叫 [CoUninitialize () ](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 。</span><span class="sxs-lookup"><span data-stu-id="eeb24-119">Call [CoUninitialize()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) when your application shuts down.</span></span> <span data-ttu-id="eeb24-120">在呼叫 CoUninitialize () 之後，您必須呼叫 [FreeLibrary (s \_ hlib) ](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 來遞減 InkEdit.dll 檔案上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="eeb24-120">After calling CoUninitialize(), you must call [FreeLibrary(s\_hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) to decrement the reference count on the InkEdit.dll file.</span></span>

 

<span data-ttu-id="eeb24-121">如果您使用 [ [ES \_ NOIME](../controls/rich-edit-control-styles.md) ] 視窗樣式，則無法使用內建的更正支援。</span><span class="sxs-lookup"><span data-stu-id="eeb24-121">If you use the [ES\_NOIME](../controls/rich-edit-control-styles.md) window style, the built-in correction support is not available.</span></span> <span data-ttu-id="eeb24-122">如果您未指定父視窗，則會將控制項建立為最上層視窗，並 \_ 新增 WS SYSMENU 樣式，這也會停用內建的更正支援。</span><span class="sxs-lookup"><span data-stu-id="eeb24-122">If you don't specify a parent window, the control is created as a top-level window and the WS\_SYSMENU style is added; this also disables the built-in correction support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeb24-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="eeb24-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeb24-124">將筆墨控制項新增至專案</span><span class="sxs-lookup"><span data-stu-id="eeb24-124">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
