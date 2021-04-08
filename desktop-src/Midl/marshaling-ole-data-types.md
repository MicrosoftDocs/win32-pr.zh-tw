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
# <a name="marshaling-ole-data-types"></a>封送處理 OLE 資料類型

為了讓您更輕鬆地使用某些 Automation 和 OLE 資料類型，以及 COM 中經常使用的一些系統控制碼，您可以匯入 Windows IDL 檔案並連結至 OLE 和 Automation DLL 檔案，以使用這些資料類型的 typedef 和其相關的 helper 函式。 這些檔案會自動安裝在您的系統上。

-   若要在遠端程序呼叫中使用 [**BSTR**](/previous-versions/windows/desktop/automat/bstr) 資料類型，請將 wtypes.h .idl 檔案匯入到您的介面定義 (idl) 檔案，並在建立分散式應用程式時連結至 oleaut32.lib。 這會讓您的存根使用現成的 helper 函式 **BSTR \_ UserSize**、 **bstr \_ UserMarshal**、 **bstr \_ UserUnmarshal** 和 **BSTR \_ UserFree**。
-   若要使用其他 Automation 資料類型（例如 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 和 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray)）或使用這些類型的型別 (例如， [**DISPPARAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) 和 [**EXCEPINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)) ，請將 objidl.idl .idl 檔匯入至 idl 檔案，並在組建階段連結至 oleaut32.lib。 這可讓您使用適當的 helper 常式。
-   若要使用 OLE 資料類型 (例如 CLIPFORMAT、SNB、STGMEDIUM、ASYNC \_ STGMEDIUM) 或系統控制碼 (例如 HMETAFILE \_ PICT、HENHMETAFILE、HMETAFILE、HBITMAP、HPALETTE 和 HGLOBAL) ，請將 objidl.idl .idl 檔案匯入到您的介面定義檔中，並在組建時連結至 ole32.lib .lib。
-   下列 OLE 控制碼也會使用 [電傳 **\[ \_ 封送 \]** 處理] 屬性來定義，但是只會在電腦中做為控制碼，因為它們無法用於遠端程序呼叫中的其他電腦： HWND、HMENU、HACCEL、HDC、HFONT、HICON、HBRUSH。 將 objidl.idl .idl 檔案匯入至 IDL 檔案，並在組建階段連結至 ole32.lib，以在單一電腦上的處理序間通訊中使用這些控制碼。

如需詳細資訊，請參閱 [有線 \_ 封送處理屬性](/windows/desktop/Rpc/the-wire-marshal-attribute)、 [類型 \_ UserSize](/windows/desktop/Rpc/the-type-usersize-function)函式、類型 [ \_ UserMarshal 函數](/windows/desktop/Rpc/the-type-usermarshal-function)、 [類型 \_ UserUnmarshal](/windows/desktop/Rpc/the-type-userunmarshal-function)函式、 [類型 \_ UserFree](/windows/desktop/Rpc/the-type-userfree-function)函式，以及 [特定32位或64位平臺的目標存根](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md)。

 

 