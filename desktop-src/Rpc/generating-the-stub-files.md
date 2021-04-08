---
title: 產生存根檔案
description: 定義用戶端/伺服器介面之後，您通常會開發用戶端和伺服器原始程式檔。
ms.assetid: e4d08bee-ab9a-4426-a1af-72a7d763797f
keywords:
- 遠端程序呼叫 RPC、工作、產生存根檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e092663711be60a3a0dc0dd8a4e99c0fa92a3ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839952"
---
# <a name="generating-the-stub-files"></a><span data-ttu-id="eb50e-104">產生存根檔案</span><span class="sxs-lookup"><span data-stu-id="eb50e-104">Generating the Stub Files</span></span>

<span data-ttu-id="eb50e-105">定義用戶端/伺服器介面之後，您通常會開發用戶端和伺服器原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="eb50e-105">After defining the client/server interface, you usually develop your client and server source files.</span></span> <span data-ttu-id="eb50e-106">接下來，請使用單一 makefile 來產生存根和標頭檔。</span><span class="sxs-lookup"><span data-stu-id="eb50e-106">Next use a single makefile to generate the stub and header files.</span></span> <span data-ttu-id="eb50e-107">編譯和連結用戶端和伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="eb50e-107">Compile and link the client and server applications.</span></span> <span data-ttu-id="eb50e-108">但是，如果這是您第一次暴露在分散式運算環境中，您可能會想要立即叫用 MIDL 編譯器來查看 MIDL 產生的內容，然後再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="eb50e-108">However, if this is your first exposure to the distributed computing environment, you may want to invoke the MIDL compiler now to see what MIDL generates before you continue.</span></span> <span data-ttu-id="eb50e-109">當您安裝平臺軟體發展工具組 (SDK) 時，會自動安裝 MIDL 編譯器 (Midl.exe) 。</span><span class="sxs-lookup"><span data-stu-id="eb50e-109">The MIDL compiler (Midl.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="eb50e-110">當您編譯這些檔案時，請確定 Hello 和 acf 都在相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="eb50e-110">When you compile these files, make sure that Hello.idl and Hello.acf are in the same directory.</span></span> <span data-ttu-id="eb50e-111">下列命令會產生標頭檔的 Hello .h，以及用戶端和伺服器 stub、Hello \_ c 和 hello \_ s.c。</span><span class="sxs-lookup"><span data-stu-id="eb50e-111">The following command will generate the header file Hello.h, and the client and server stubs, Hello\_c.c and Hello\_s.c.</span></span>

<span data-ttu-id="eb50e-112">**midl hello .idl**</span><span class="sxs-lookup"><span data-stu-id="eb50e-112">**midl hello.idl**</span></span>

<span data-ttu-id="eb50e-113">請注意，Hello. h 包含 HelloProc 和關機的函式原型，以及兩個記憶體管理函式、 **midl \_ 使用者 \_ 配置** 和 **midl \_ 使用者 \_ 免費** 的向前宣告。</span><span class="sxs-lookup"><span data-stu-id="eb50e-113">Notice that Hello.h contains function prototypes for HelloProc and Shutdown, as well as forward declarations for two memory management functions, **midl\_user\_allocate** and **midl\_user\_free**.</span></span> <span data-ttu-id="eb50e-114">您將在伺服器應用程式中提供這兩個函數。</span><span class="sxs-lookup"><span data-stu-id="eb50e-114">You will provide these two functions in the server application.</span></span> <span data-ttu-id="eb50e-115">如果從伺服器將資料傳輸至用戶端 (透過 \[ **out** \] 參數) 您也必須在用戶端應用程式中提供這兩個記憶體管理函數。</span><span class="sxs-lookup"><span data-stu-id="eb50e-115">If data were being transmitted from the server to the client (by means of an \[**out**\] parameter) you would also need to provide these two memory management functions in the client application.</span></span>

<span data-ttu-id="eb50e-116">請注意全域控制碼變數、hello \_ IfHandle、用戶端和伺服器介面控制碼名稱的定義、hello \_ v1 \_ 0 \_ c \_ ifspec 和 hello \_ v1 \_ 0 \_ s \_ ifspec。</span><span class="sxs-lookup"><span data-stu-id="eb50e-116">Note the definitions for the global handle variable, hello\_IfHandle, and the client and server interface handle names, hello\_v1\_0\_c\_ifspec and hello\_v1\_0\_s\_ifspec.</span></span> <span data-ttu-id="eb50e-117">用戶端和伺服器應用程式會在執行時間呼叫中使用介面控制碼名稱。</span><span class="sxs-lookup"><span data-stu-id="eb50e-117">The client and server applications will use the interface handle names in run-time calls.</span></span>

<span data-ttu-id="eb50e-118">到目前為止，您不需要對存根檔案進行任何動作，例如，您可以使用 \_ \_ s.c。</span><span class="sxs-lookup"><span data-stu-id="eb50e-118">At this point, you don't need to do anything with the stub files Hello\_c.c and hello\_s.c.</span></span>

``` syntax
/*file: hello.h */
/* this ALWAYS GENERATED file contains the definitions for the interfaces */
/* File created by MIDL compiler version 3.00.06 
/* at Tue Feb 20 11:33:32 1996 */
/* Compiler settings for hello.idl:
    Os, W1, Zp8, env=Win32, ms_ext, c_ext
    error checks: none */
//@@MIDL_FILE_HEADING(  )
#include "Rpc.h"
#include "rpcndr.h"
 
#ifndef __hello_h_
#define __hello_h_
 
#ifdef __cplusplus
extern "C"{
#endif 
 
/* Forward Declarations */ 
 
void __RPC_FAR * __RPC_USER MIDL_user_allocate(size_t);
void __RPC_USER MIDL_user_free( void __RPC_FAR * ); 
 
#ifndef __hello_INTERFACE_DEFINED__
#define __hello_INTERFACE_DEFINED__
 
/****************************************
 * Generated header for interface: hello
 * at Tue Feb 20 11:33:32 1996
 * using MIDL 3.00.06
 ****************************************/
/* [implicit_handle][version][uuid] */ 
 
            /* size is 0 */
void HelloProc( 
    /* [string][in] */ unsigned char __RPC_FAR *pszString);
    /* size is 0 */
void Shutdown( void);
extern handle_t hello_IfHandle;
 
extern RPC_IF_HANDLE hello_v1_0_c_ifspec;
extern RPC_IF_HANDLE hello_v1_0_s_ifspec;
#endif /* __hello_INTERFACE_DEFINED__ */
 
/* Additional Prototypes for ALL interfaces */
/* end of Additional Prototypes */
#ifdef __cplusplus
}
#endif
#endif
```

 

 




