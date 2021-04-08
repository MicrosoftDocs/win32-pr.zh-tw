---
title: C-Proxy/Stub 的編譯器定義
description: 標頭檔 Rpcproxy 包含下列巨集定義，在建立分散式 COM 應用程式時，每個定義都可能很方便。 這些宏會使用/D (或-D) 預處理器參數在 C 編譯時間進行叫用。
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL 編譯器 MIDL，C-編譯器，proxy/stub 的定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1504c600c3f86a934ab3daa132b041c7310af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021844"
---
# <a name="c-compiler-definitions-for-proxystubs"></a><span data-ttu-id="d1ae8-105">C-Proxy/Stub 的編譯器定義</span><span class="sxs-lookup"><span data-stu-id="d1ae8-105">C-Compiler Definitions for Proxy/Stubs</span></span>

<span data-ttu-id="d1ae8-106">標頭檔 Rpcproxy 包含下列巨集定義，在建立分散式 COM 應用程式時，每個定義都可能很方便。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-106">The header file Rpcproxy.h includes the following macro definitions, each of which may be convenient when building distributed COM application.</span></span> <span data-ttu-id="d1ae8-107">這些宏會使用 [**/d**](-d.md) (或-D) 預處理器參數在 C 編譯時間進行叫用。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-107">These macros are invoked with the [**/D**](-d.md) (or -D) preprocessor switch at the C-compile time.</span></span>



| <span data-ttu-id="d1ae8-108">MACRO</span><span class="sxs-lookup"><span data-stu-id="d1ae8-108">MACRO</span></span>                                                                                                                                                                                           | <span data-ttu-id="d1ae8-109">Description</span><span class="sxs-lookup"><span data-stu-id="d1ae8-109">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ae8-110">註冊 \_ PROXY \_ DLL</span><span class="sxs-lookup"><span data-stu-id="d1ae8-110">REGISTER\_PROXY\_DLL</span></span>                                                                                                                                                                            | <span data-ttu-id="d1ae8-111">產生 **DllMain**、 **DllRegisterServer** 和 **DllUnregisterServer** 函數，以自動註冊 proxy DLL。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-111">Generates **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions for automatically registering a proxy DLL.</span></span>                                                                                       |
| <span data-ttu-id="d1ae8-112">PROXY \_ CLSID =<clsid></span><span class="sxs-lookup"><span data-stu-id="d1ae8-112">PROXY\_CLSID=<clsid></span></span>                                                                                                                                                                      | <span data-ttu-id="d1ae8-113">指定伺服器的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-113">Specifies a class identifier for the server.</span></span> <span data-ttu-id="d1ae8-114">如果未定義這個宏，預設 CLSID 就是 MIDL 編譯器在 Proxy/Stub 伺服器的 IDL 規格中遇到的第一個介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-114">If this macro is not defined, the default CLSID is the first interface identifier that the MIDL compiler encounters in the IDL specification for the Proxy/Stub server.</span></span> |
| <span data-ttu-id="d1ae8-115">PROXY \_ CLSID \_ 為 = {0x *8hexdigits*、0x *4hexdigits*、0x *4hexdigits*、{0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、0x *2hexdigits*、}}</span><span class="sxs-lookup"><span data-stu-id="d1ae8-115">PROXY\_CLSID\_IS={0x *8hexdigits*, 0x *4hexdigits*,0x *4hexdigits*, {0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*,}}</span></span> | <span data-ttu-id="d1ae8-116">以二進位十六進位格式指定伺服器類別識別碼的值。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-116">Specifies the value of the server's class identifier in binary hex format.</span></span>                                                                                                                                           |



 

<span data-ttu-id="d1ae8-117">藉由在編譯 Dlldata.c 時定義 **REGISTER \_ proxy \_ dll** 宏，您的 PROXY/存根封送處理 dll 將會自動包含 **DllMain**、 **DllRegisterServer** 和 **DllUnregisterServer** 函數的預設定義。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-117">By defining the **REGISTER\_PROXY\_DLL** macro when compiling Dlldata.c, your proxy/stub marshaling DLL will automatically include default definitions for the **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions.</span></span> <span data-ttu-id="d1ae8-118">您可以使用這些功能，在系統登錄中自行註冊 proxy DLL。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-118">You can use these functions to self-register your proxy DLL in the system registry.</span></span>

<span data-ttu-id="d1ae8-119">此預設註冊程式碼會使用第一個介面的 GUID，作為登錄整個 proxy/存根 DLL 伺服器的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-119">This default registration code uses the GUID of the first interface encountered as the CLSID for registering the entire proxy/stub DLL server.</span></span> <span data-ttu-id="d1ae8-120">COM 稍後會使用這個 CLSID 來找出並載入已編譯的 proxy/存根伺服器，以供伺服器所註冊的任何介面封送處理之用。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-120">COM later uses this CLSID to locate and load the compiled proxy/stub server for the marshaling of any of the interfaces the server is registered to handle.</span></span> <span data-ttu-id="d1ae8-121">當應用程式進行跨越執行緒、進程或電腦界限的介面方法呼叫時，COM 會使用介面識別碼登錄專案來找出 proxy/存根封送處理伺服器的 CLSID 登錄專案。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-121">When an application makes an interface method call that crosses thread, process, or computer boundaries, COM uses the interface identifier registry entry to locate the CLSID registry entry for the proxy/stub marshaling server.</span></span> <span data-ttu-id="d1ae8-122">然後，它會使用此 CLSID 來載入伺服器 (（如果尚未載入）) ，以便可以封送處理介面呼叫。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-122">It then uses this CLSID to load the server (if it isn't already loaded) so that the interface call can then be marshaled.</span></span>

<span data-ttu-id="d1ae8-123">**\_** = <clsid> 當您想要明確指定 proxy/stub 伺服器的 clsid 而不是依賴預設 clsid 時，請使用 proxy CLSID 宏。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-123">Use the **PROXY\_CLSID**=<clsid> macro when you want to explicitly specify the proxy/stub server's CLSID rather than rely on the default CLSID.</span></span> <span data-ttu-id="d1ae8-124">例如，如果您要建立標準封送處理 DLL 做為您自己的同進程 COM 伺服器，或您需要定義自己的 **DllMain** 來處理 DLL \_ 進程 \_ 附加。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-124">For example, if you are building a standard marshaling DLL as your own in-process COM server, or if you need to define your own **DllMain** to handle DLL\_PROCESS\_ATTACH.</span></span>

<span data-ttu-id="d1ae8-125">使用 **proxy \_ clsid \_**= 宏而非 **PROXY \_ clsid** ，以定義 **\_ GUID** 宏所使用的二進位十六進位格式來定義 CLSID 的值。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-125">Use **PROXY\_CLSID\_IS**= macro instead of **PROXY\_CLSID** to define the value of the CLSID in the binary hexadecimal format that the **DEFINE\_GUID** macro uses.</span></span>

<span data-ttu-id="d1ae8-126">另請注意，當預設的 **DllRegisterServer** 函式執行時，它會使用 >threadingmodel = Both 來註冊伺服器。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-126">Also note that when the default **DllRegisterServer** function runs, it registers the server with ThreadingModel=Both.</span></span>

<span data-ttu-id="d1ae8-127">下列 makefile 範例會使用 **註冊 \_ proxy \_ DLL** 和 **PROXY \_ CLSID**= 宏：</span><span class="sxs-lookup"><span data-stu-id="d1ae8-127">The following makefile example uses the **REGISTER\_PROXY\_DLL** and **PROXY\_CLSID**= macros:</span></span>

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

<span data-ttu-id="d1ae8-128">如需有關 [**/d**](-d.md) 預處理器選項的詳細資訊，請參閱 C 編譯器檔。</span><span class="sxs-lookup"><span data-stu-id="d1ae8-128">For more information on the [**/D**](-d.md) preprocessor option, see your C compiler documentation.</span></span>

 

 




