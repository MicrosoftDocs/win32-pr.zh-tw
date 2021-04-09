---
title: IDL 介面主體
description: IDL 介面主體包含遠端程序呼叫中使用的資料類型，以及遠端程式的函式原型。
ms.assetid: b07524a7-b27e-4ea2-ae34-068c07d9a444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565cbe6493bd865030b77b5e9ef6275b444ca451
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682700"
---
# <a name="the-idl-interface-body"></a><span data-ttu-id="060c2-103">IDL 介面主體</span><span class="sxs-lookup"><span data-stu-id="060c2-103">The IDL Interface Body</span></span>

<span data-ttu-id="060c2-104">IDL 介面主體包含遠端程序呼叫中使用的資料類型，以及遠端程式的函式原型。</span><span class="sxs-lookup"><span data-stu-id="060c2-104">The IDL interface body contains data types used in remote procedure calls and the function prototypes for the remote procedures.</span></span> <span data-ttu-id="060c2-105">介面主體也可以包含 imports、pragma、常數宣告和類型宣告。</span><span class="sxs-lookup"><span data-stu-id="060c2-105">The interface body can also contain imports, pragmas, constant declarations, and type declarations.</span></span> <span data-ttu-id="060c2-106">在 Microsoft 擴充模式中，MIDL 編譯器也會允許變數定義形式的隱含宣告。</span><span class="sxs-lookup"><span data-stu-id="060c2-106">In Microsoft-extensions mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="060c2-107">下列範例顯示的 IDL 檔案包含介面的定義。</span><span class="sxs-lookup"><span data-stu-id="060c2-107">The following example shows an IDL file containing the definition of an interface.</span></span> <span data-ttu-id="060c2-108">在大括弧之間發生之介面定義的主體，包含常數 (**BUFSIZE**) 的定義、) 的類型 (**PCONTEXT \_ 控制碼 \_ 類型** ，以及某些遠端程式 (**RemoteOpen**、 **RemoteRead**、 **RemoteClose** 和 **Shutdown**) 。</span><span class="sxs-lookup"><span data-stu-id="060c2-108">The body of the interface definition, which occurs between the curly brackets, contains the definition of a constant (**BUFSIZE**), a type (**PCONTEXT\_HANDLE\_TYPE**), and some remote procedures (**RemoteOpen**, **RemoteRead**, **RemoteClose**, and **Shutdown**).</span></span>

``` syntax
[ 
  uuid (ba209999-0c6c-11d2-97cf-00c04f8eea45), 
  version(1.0), 
  pointer_default(unique) 
] 
interface cxhndl 
{ 
 
  const short BUFSIZE = 1024;  
 
  typedef [context_handle] void *PCONTEXT_HANDLE_TYPE; 
 
  short RemoteOpen( 
      [out] PCONTEXT_HANDLE_TYPE *pphContext, 
      [in, string] unsigned char *pszFile 
  ); 
 
   short RemoteRead( 
      [in]  PCONTEXT_HANDLE_TYPE phContext, 
      [out] unsigned char achBuf[BUFSIZE], 
      [out] short *pcbBuf 
  ); 
 
  short RemoteClose( [in, out] PCONTEXT_HANDLE_TYPE *pphContext ); 
 
  void Shutdown(void); 
 
}
```

<span data-ttu-id="060c2-109">如需詳細資訊，請參閱 [MIDL 語言參考](/windows/desktop/Midl/midl-language-reference)。</span><span class="sxs-lookup"><span data-stu-id="060c2-109">For more information see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 