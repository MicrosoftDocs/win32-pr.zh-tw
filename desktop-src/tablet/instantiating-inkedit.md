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
# <a name="instantiating-inkedit"></a>具現化 InkEdit

本主題說明可具現化 [InkEdit](inkedit-control.md) 控制項的各種方式。

## <a name="visual-basic-net-and-c"></a>Visual Basic .NET 和 C\#

如果您正在使用 Microsoft Visual Basic .NET 或 C \# ，請從 Visual Studio 的工具箱將 [InkEdit](./inkedit-control.md) 控制項拖曳至您想要顯示控制項的表單或頁面。

## <a name="win32c"></a>Win32/c + +

[InkEdit](inkedit-control-reference.md)控制項是 Rich Edit 4.5 Win32 OLE 可嵌入控制項的超級類別。

Win32 應用程式會藉由呼叫[ () 的 CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa)將[InkEdit](inkedit-control-reference.md)控制項具現化，並以視窗類別的形式傳遞 InkEdit。 INKEDIT 定義于筆跡中。 建立控制項之後，您可以使用訊息「與」控制項「交談」。 豐富的編輯訊息 (EM \_ \*) 會從 InkEdit 傳遞至非改變的 rich edit; 所有現有的豐富編輯功能都可以使用。

若要建立 [InkEdit](inkedit-control-reference.md) 控制項，請呼叫 [CreateWindow () ](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數，並指定 InkEdit 視窗類別。 使用 [LoadLibrary () ](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 註冊 InkEd.dll。 \_為視窗類別參數指定 INKEDIT 類別定義的常數，並使用下列範例中所指定的視窗樣式。

### <a name="instantiating-a-multiline-inkedit-control"></a>具現化多行 InkEdit 控制項


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



### <a name="instantiating-a-single-line-inkedit-control"></a>將 Single-Line InkEdit 控制項具現化


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
> 不同于 RichEdit，您必須在建立[InkEdit](inkedit-control-reference.md)控制項之前務必先呼叫[CoInitialize () ](/windows/win32/api/objbase/nf-objbase-coinitialize) 。 當您的應用程式關閉時，請呼叫 [CoUninitialize () ](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 。 在呼叫 CoUninitialize () 之後，您必須呼叫 [FreeLibrary (s \_ hlib) ](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 來遞減 InkEdit.dll 檔案上的參考計數。

 

如果您使用 [ [ES \_ NOIME](../controls/rich-edit-control-styles.md) ] 視窗樣式，則無法使用內建的更正支援。 如果您未指定父視窗，則會將控制項建立為最上層視窗，並 \_ 新增 WS SYSMENU 樣式，這也會停用內建的更正支援。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將筆墨控制項新增至專案](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
