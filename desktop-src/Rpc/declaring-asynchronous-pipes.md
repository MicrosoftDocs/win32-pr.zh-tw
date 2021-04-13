---
title: 宣告非同步管道
description: 下列範例 IDL 檔案會定義典型的管道結構，以及具有管道的非同步 RPC 函式。
ms.assetid: ddd20212-18f5-41f6-9f6e-0edbe5e517a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f8fb11d89d92bcee5b2b8b052a381077aeb82c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300444"
---
# <a name="declaring-asynchronous-pipes"></a><span data-ttu-id="f9119-103">宣告非同步管道</span><span class="sxs-lookup"><span data-stu-id="f9119-103">Declaring Asynchronous Pipes</span></span>

<span data-ttu-id="f9119-104">下列範例 IDL 檔案會定義典型的管道結構，以及具有管道的非同步 RPC 函式。</span><span class="sxs-lookup"><span data-stu-id="f9119-104">The following example IDL file defines a typical pipe structure, and an asynchronous RPC function with pipes.</span></span>

## <a name="example"></a><span data-ttu-id="f9119-105">範例</span><span class="sxs-lookup"><span data-stu-id="f9119-105">Example</span></span>

``` syntax
//file: Xasyncpipe.idl:
//
interface IMyAsyncPipe 
{
    //define the pipe type
    typedef pipe int aysnc_intpipe ;
 
    //then use it as a parameter
    int MyAsyncPipe(
        handle_t hBinding, 
        [in] a,
        [in] ASYNC_INTPIPE *inpipe, 
        [out] ASYNC_INTPIPE *outpipe, 
        [out] int *b) ;
};
//other function declarations
 
//other interface definitions
//end Xasyncpipe.idl
 
//file:Xasyncpipe.acf:
//file: Xasyncpipe.acf:
interface IMyAsyncPipe
{
    [async] MyAsyncPipe () ;
} ;
//
//end Xasyncpipe.acf
```

<span data-ttu-id="f9119-106">下列程式碼片段顯示典型的管道結構定義。</span><span class="sxs-lookup"><span data-stu-id="f9119-106">The following code fragment shows a typical pipe structure definition.</span></span> <span data-ttu-id="f9119-107">它包含推播和提取程式的指標、用來保存管道資料的緩衝區，以及用來協調程式的狀態變數：</span><span class="sxs-lookup"><span data-stu-id="f9119-107">It contains pointers to push and pull procedures, a buffer to hold the pipe data, and a state variable to coordinate the procedures:</span></span>

``` syntax
//
typedef struct ASYNC_MYPIPE
{
    RPC_STATUS (__RPC_FAR * pull) (
        char __RPC_FAR * state,
        small __RPC_FAR * buf,
        unsigned long esize,
        unsigned long __RPC_FAR * ecount );
    RPC_STATUS (__RPC_FAR * push) (
        char __RPC_FAR * state,
        small __RPC_FAR * buf,
        unsigned long ecount );
    void *Reserved;
    char __RPC_FAR * state;
}ASYNC_INTPIPE;
```

 

 




