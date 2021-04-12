---
description: 許多函式會將可能大量的資料傳回給應用程式做為其中一個參數提供的位址。
ms.assetid: ef99edef-39b2-4d78-9c01-13720215d47f
title: 正在抓取未知長度的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30620018f3c4871bd27299c3dd21ae42936c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848663"
---
# <a name="retrieving-data-of-unknown-length"></a>正在抓取未知長度的資料

許多函式會將可能大量的資料傳回給應用程式做為其中一個參數提供的位址。 在上述所有情況下，會以類似的方式執行作業（如果不相同）。 指向傳回資料位置的參數將會使用標記法慣例，其中 pb 或 pv 是參數名稱的前兩個字元。 另一個參數會以 pcb 作為參數名稱的前三個字元。 此參數代表將傳回至 pb 或 pv 位置之資料的大小（以位元組為單位）。 例如，請考慮下列函數規格：

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

在此範例中， *>pbdata* 是將傳回資料的位置指標，而 *pcbData* 則是傳回資料的大小（以位元組為單位）。

> [!Note]  
> Pcb 參數的附屬參數有時可能會有稍微不同的前置詞，例如 p 或 pv。 此外，對於使用前置詞 pwsz 和 pcch 組合的參數，pcch 參數是傳回的資料的計數（以字元為單位 ([*Unicode*](../secgloss/u-gly.md) 或 [*ASCII*](../secgloss/a-gly.md)）（適用) ）。

 

如果 *>pbdata* 參數所指定的緩衝區不夠大，無法容納傳回的資料，此函式會設定錯誤的 \_ \_ 資料程式碼 (可透過呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式來查看) 並將所需的緩衝區大小（以位元組為單位）儲存在 *pcbData* 所指向的變數中。

如果 *>pbdata* 的輸入為 **Null** ，且 *pcbData* 不是 **null**，則不會傳回任何錯誤，且函式會傳回 *pcbData* 所指向之變數中所需記憶體緩衝區的大小（以位元組為單位）。 這可讓應用程式判斷所傳回資料的大小，以及配置的最佳方式。

> [!Note]  
> 當輸入 **Null** 做為 *>pbdata* 的輸入，以判斷所傳回的資料是否符合指定的緩衝區所需的大小時，第二次呼叫以所需資料填入緩衝區的函式，可能不會使用整個緩衝區。 第二次呼叫之後，傳回的資料實際大小會包含在 *pcbData* 中。 處理資料時，請使用此大小。

 

下列範例會示範如何針對此用途來執行輸入和輸出參數。


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void MyHandleError(char *s);

void main()
{

// Set up SomeFunction variables.
PCCRL_CONTEXT pCrlContext; // Initialized elsewhere.
DWORD dwPropId;            // Initialized elsewhere.
DWORD cbData;
BYTE  *pbData;

// Call SomeFunction to set cbData, the size of 
// the buffer needed for pbData.
if(SomeFunction(
     pCrlContext, 
     dwPropId, 
     NULL, 
     &cbData))
{
       printf("The function succeeded.\n");
}
else
{

// The function call failed. Handle the error.
       MyHandleError("Function call failed.");
}

// The call succeeded; the size for the needed buffer, in bytes, 
// now resides in cbData.

// Malloc memory for the size of the message.
if(pbData = (BYTE*)malloc(cbData))
{
   printf("Memory has been allocated.\n");
}
else
{

   // The allocation failed. Write an error message and exit.
   MyHandleError("Malloc operation failed. ");
}

// The space for the buffer has been allocated.
// Call SomeFunction to fill the buffer with the data.
if(SomeFunction(
      pCrlContext, 
      dwPropId, 
      pbData, 
      &cbData))
{
       printf("The function succeeded.\n");
}
else
{

   // The second function call failed. Handle the error.
   MyHandleError("The second call to the function failed.");
}

// The function succeeded; the data is now in the buffer
// pointed to by pbData. Note that cbData is
// updated with the actual size of the data returned. Use this size 
// to process bytes of pbData.

// When you have finished using the allocated memory, free it.
free(pbData);

} // End of main

//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the 
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.
void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program.\n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr,"Error number %x.\n",GetLastError());
    fprintf(stderr,"Program terminating.\n");
    exit(1);
}
```



 

 
