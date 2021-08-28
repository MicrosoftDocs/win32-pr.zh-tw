---
title: 產生存根檔案
description: 定義用戶端/伺服器介面之後，您通常會開發用戶端和伺服器原始程式檔。
ms.assetid: e4d08bee-ab9a-4426-a1af-72a7d763797f
keywords:
- 遠端程序呼叫 RPC、工作、產生存根檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03fbffb165e94b89e6801c212d0a8b63cd4e77fab28ad4a4afc4b4243ae0e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020878"
---
# <a name="generating-the-stub-files"></a>產生存根檔案

定義用戶端/伺服器介面之後，您通常會開發用戶端和伺服器原始程式檔。 接下來，請使用單一 makefile 來產生存根和標頭檔。 編譯和連結用戶端和伺服器應用程式。 但是，如果這是您第一次暴露在分散式運算環境中，您可能會想要立即叫用 MIDL 編譯器來查看 MIDL 產生的內容，然後再繼續進行。 當您安裝平臺軟體發展工具組 (SDK) 時，會自動安裝 MIDL 編譯器 (Midl.exe) 。

當您編譯這些檔案時，請確定 Hello 和 acf 都在相同的目錄中。 下列命令會產生標頭檔的 Hello .h，以及用戶端和伺服器 stub、Hello \_ c 和 hello \_ s.c。

**midl hello .idl**

請注意，Hello. h 包含 HelloProc 和關機的函式原型，以及兩個記憶體管理函式、 **midl \_ 使用者 \_ 配置** 和 **midl \_ 使用者 \_ 免費** 的向前宣告。 您將在伺服器應用程式中提供這兩個函數。 如果從伺服器將資料傳輸至用戶端 (透過 \[ **out** \] 參數) 您也必須在用戶端應用程式中提供這兩個記憶體管理函數。

請注意全域控制碼變數、hello \_ IfHandle、用戶端和伺服器介面控制碼名稱的定義、hello \_ v1 \_ 0 \_ c \_ ifspec 和 hello \_ v1 \_ 0 \_ s \_ ifspec。 用戶端和伺服器應用程式會在執行時間呼叫中使用介面控制碼名稱。

到目前為止，您不需要對存根檔案進行任何動作，例如，您可以使用 \_ \_ s.c。

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

 

 




