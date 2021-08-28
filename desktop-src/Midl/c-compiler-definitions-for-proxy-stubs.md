---
title: C-Proxy/Stub 的編譯器定義
description: 標頭檔 Rpcproxy 包含下列巨集定義，在建立分散式 COM 應用程式時，每個定義都可能很方便。 這些宏會使用/D (或-D) 預處理器參數在 C 編譯時間進行叫用。
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL 編譯器 MIDL，C-編譯器，proxy/stub 的定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b272b8b540420930366864c45e993172f5c00e67
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882061"
---
# <a name="c-compiler-definitions-for-proxystubs"></a>C-Proxy/Stub 的編譯器定義

標頭檔 Rpcproxy 包含下列巨集定義，在建立分散式 COM 應用程式時，每個定義都可能很方便。 這些宏會使用 [**/d**](-d.md) (或-D) 預處理器參數在 C 編譯時間進行叫用。



| MACRO                                                                                                                                                                                           | 說明                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 註冊 \_ PROXY \_ DLL                                                                                                                                                                            | 產生 **DllMain**、 **DllRegisterServer** 和 **DllUnregisterServer** 函數，以自動註冊 proxy DLL。                                                                                       |
| PROXY \_ CLSID = &lt; CLSID&gt;                                                                                                                                                                      | 指定伺服器的類別識別碼。 如果未定義這個宏，預設 CLSID 就是 MIDL 編譯器在 Proxy/Stub 伺服器的 IDL 規格中遇到的第一個介面識別碼。 |
| PROXY \_ CLSID \_ 為 = {0x *8hexdigits*、0x *4hexdigits*、0x *4hexdigits*、{0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、}} | 以二進位十六進位格式指定伺服器類別識別碼的值。                                                                                                                                           |



 

藉由在編譯 Dlldata.c 時定義 **REGISTER \_ proxy \_ dll** 宏，您的 PROXY/存根封送處理 dll 將會自動包含 **DllMain**、 **DllRegisterServer** 和 **DllUnregisterServer** 函數的預設定義。 您可以使用這些功能，在系統登錄中自行註冊 proxy DLL。

此預設註冊程式碼會使用第一個介面的 GUID，作為登錄整個 proxy/存根 DLL 伺服器的 CLSID。 COM 稍後會使用這個 CLSID 來找出並載入已編譯的 proxy/存根伺服器，以供伺服器所註冊的任何介面封送處理之用。 當應用程式進行跨越執行緒、進程或電腦界限的介面方法呼叫時，COM 會使用介面識別碼登錄專案來找出 proxy/存根封送處理伺服器的 CLSID 登錄專案。 然後，它會使用此 CLSID 來載入伺服器 (（如果尚未載入）) ，以便可以封送處理介面呼叫。

**\_** = &lt; &gt; 當您想要明確指定 proxy/stub 伺服器的 clsid，而不是依賴預設 CLSID 時，請使用 proxy clsid clsid 宏。 例如，如果您要建立標準封送處理 DLL 做為您自己的同進程 COM 伺服器，或您需要定義自己的 **DllMain** 來處理 DLL \_ 進程 \_ 附加。

使用 **proxy \_ clsid \_**= 宏而非 **PROXY \_ clsid** ，以定義 **\_ GUID** 宏所使用的二進位十六進位格式來定義 CLSID 的值。

另請注意，當預設的 **DllRegisterServer** 函式執行時，它會使用 >threadingmodel = Both 來註冊伺服器。

下列 makefile 範例會使用 **註冊 \_ proxy \_ DLL** 和 **PROXY \_ CLSID**= 宏：

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL \
    /DPROXY_CLSID=7a98c250-6808-11cf-b73b-00aa00b677a7
example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
```

如需有關 [**/d**](-d.md) 預處理器選項的詳細資訊，請參閱 C 編譯器檔。

 

 




