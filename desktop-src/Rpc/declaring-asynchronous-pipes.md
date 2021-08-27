---
title: 宣告非同步管道
description: 下列範例 IDL 檔案會定義典型的管道結構，以及具有管道的非同步 RPC 函式。
ms.assetid: ddd20212-18f5-41f6-9f6e-0edbe5e517a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16c49bc722cd8069f446cc87567f20b1636dc77654f4387ca635f952e33dc83b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101668"
---
# <a name="declaring-asynchronous-pipes"></a>宣告非同步管道

下列範例 IDL 檔案會定義典型的管道結構，以及具有管道的非同步 RPC 函式。

## <a name="example"></a>範例

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

下列程式碼片段顯示典型的管道結構定義。 它包含推播和提取程式的指標、用來保存管道資料的緩衝區，以及用來協調程式的狀態變數：

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

 

 




