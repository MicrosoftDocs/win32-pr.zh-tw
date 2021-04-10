---
title: 封送處理 OLE 資料類型
description: 封送處理 Automation 和 OLE 資料類型。
ms.assetid: 0cab4208-d40d-40a1-88f2-4933b52c0c29
keywords:
- MIDL 和 COM MIDL，封送處理 OLE 資料類型
- 封送處理 MIDL
- OLE 資料 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970c6e0fef9d0fc88b8a0a11a087fa4396d7a7c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681821"
---
# <a name="marshaling-ole-data-types"></a><span data-ttu-id="a526a-106">封送處理 OLE 資料類型</span><span class="sxs-lookup"><span data-stu-id="a526a-106">Marshaling OLE Data Types</span></span>

<span data-ttu-id="a526a-107">為了讓您更輕鬆地使用某些 Automation 和 OLE 資料類型，以及 COM 中經常使用的一些系統控制碼，您可以匯入 Windows IDL 檔案並連結至 OLE 和 Automation DLL 檔案，以使用這些資料類型的 typedef 和其相關的 helper 函式。</span><span class="sxs-lookup"><span data-stu-id="a526a-107">To make it easier to use certain Automation and OLE data types, as well as some system handles frequently used in COM, typedefs for these data types and their related helper functions are available by importing Windows IDL files and linking to the OLE and Automation DLL files.</span></span> <span data-ttu-id="a526a-108">這些檔案會自動安裝在您的系統上。</span><span class="sxs-lookup"><span data-stu-id="a526a-108">These files are automatically installed on your system.</span></span>

-   <span data-ttu-id="a526a-109">若要在遠端程序呼叫中使用 [**BSTR**](/previous-versions/windows/desktop/automat/bstr) 資料類型，請將 wtypes.h .idl 檔案匯入到您的介面定義 (idl) 檔案，並在建立分散式應用程式時連結至 oleaut32.lib。</span><span class="sxs-lookup"><span data-stu-id="a526a-109">To use the [**BSTR**](/previous-versions/windows/desktop/automat/bstr) data type in remote procedure calls, import the wtypes.idl file into your interface definition (IDL) file and link to Oleaut32.lib when building your distributed application.</span></span> <span data-ttu-id="a526a-110">這會讓您的存根使用現成的 helper 函式 **BSTR \_ UserSize**、 **bstr \_ UserMarshal**、 **bstr \_ UserUnmarshal** 和 **BSTR \_ UserFree**。</span><span class="sxs-lookup"><span data-stu-id="a526a-110">This will let your stubs use the ready-made helper functions **BSTR\_UserSize**, **BSTR\_UserMarshal**, **BSTR\_UserUnmarshal**, and **BSTR\_UserFree**.</span></span>
-   <span data-ttu-id="a526a-111">若要使用其他 Automation 資料類型（例如 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 和 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray)）或使用這些類型的型別 (例如， [**DISPPARAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) 和 [**EXCEPINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)) ，請將 objidl.idl .idl 檔匯入至 idl 檔案，並在組建階段連結至 oleaut32.lib。</span><span class="sxs-lookup"><span data-stu-id="a526a-111">To use other Automation data types, such as [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) and [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray), or types that use those types (for example, [**DISPPARAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) and [**EXCEPINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)), import the objidl.idl file into your IDL file and link to the oleaut32.lib at build time.</span></span> <span data-ttu-id="a526a-112">這可讓您使用適當的 helper 常式。</span><span class="sxs-lookup"><span data-stu-id="a526a-112">This will allow you to use the appropriate helper routines.</span></span>
-   <span data-ttu-id="a526a-113">若要使用 OLE 資料類型 (例如 CLIPFORMAT、SNB、STGMEDIUM、ASYNC \_ STGMEDIUM) 或系統控制碼 (例如 HMETAFILE \_ PICT、HENHMETAFILE、HMETAFILE、HBITMAP、HPALETTE 和 HGLOBAL) ，請將 objidl.idl .idl 檔案匯入到您的介面定義檔中，並在組建時連結至 ole32.lib .lib。</span><span class="sxs-lookup"><span data-stu-id="a526a-113">To use OLE data types (such as CLIPFORMAT, SNB, STGMEDIUM, ASYNC\_STGMEDIUM), or system handles (such as HMETAFILE\_PICT, HENHMETAFILE, HMETAFILE, HBITMAP, HPALETTE, and HGLOBAL), import the objidl.idl file into your interface definition file and link to the ole32.lib at build time.</span></span>
-   <span data-ttu-id="a526a-114">下列 OLE 控制碼也會使用 [電傳 **\[ \_ 封送 \]** 處理] 屬性來定義，但是只會在電腦中做為控制碼，因為它們無法用於遠端程序呼叫中的其他電腦： HWND、HMENU、HACCEL、HDC、HFONT、HICON、HBRUSH。</span><span class="sxs-lookup"><span data-stu-id="a526a-114">The following OLE handles are also defined with the **\[wire\_marshal\]** attribute, but only as handles within a computer since they cannot be used in remote procedure calls to other computers at this time: HWND, HMENU, HACCEL, HDC, HFONT, HICON, HBRUSH.</span></span> <span data-ttu-id="a526a-115">將 objidl.idl .idl 檔案匯入至 IDL 檔案，並在組建階段連結至 ole32.lib，以在單一電腦上的處理序間通訊中使用這些控制碼。</span><span class="sxs-lookup"><span data-stu-id="a526a-115">Import the objidl.idl file into your IDL file and link to ole32.lib at build time to use these handles in interprocess communication on a single computer.</span></span>

<span data-ttu-id="a526a-116">如需詳細資訊，請參閱 [有線 \_ 封送處理屬性](/windows/desktop/Rpc/the-wire-marshal-attribute)、 [類型 \_ UserSize](/windows/desktop/Rpc/the-type-usersize-function)函式、類型 [ \_ UserMarshal 函數](/windows/desktop/Rpc/the-type-usermarshal-function)、 [類型 \_ UserUnmarshal](/windows/desktop/Rpc/the-type-userunmarshal-function)函式、 [類型 \_ UserFree](/windows/desktop/Rpc/the-type-userfree-function)函式，以及 [特定32位或64位平臺的目標存根](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md)。</span><span class="sxs-lookup"><span data-stu-id="a526a-116">For more information, see [The wire\_marshal Attribute](/windows/desktop/Rpc/the-wire-marshal-attribute), [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function), [The type\_UserMarshal Function](/windows/desktop/Rpc/the-type-usermarshal-function), [The type\_UserUnmarshal Function](/windows/desktop/Rpc/the-type-userunmarshal-function), [The type\_UserFree Function](/windows/desktop/Rpc/the-type-userfree-function), and [Targeting Stubs for Specific 32-bit or 64-bit Platforms](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md).</span></span>

 

 