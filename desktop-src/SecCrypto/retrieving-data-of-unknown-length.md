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
# <a name="retrieving-data-of-unknown-length"></a><span data-ttu-id="0707b-103">正在抓取未知長度的資料</span><span class="sxs-lookup"><span data-stu-id="0707b-103">Retrieving Data of Unknown Length</span></span>

<span data-ttu-id="0707b-104">許多函式會將可能大量的資料傳回給應用程式做為其中一個參數提供的位址。</span><span class="sxs-lookup"><span data-stu-id="0707b-104">Many functions return a potentially large amount of data to an address provided as one of the parameters by the application.</span></span> <span data-ttu-id="0707b-105">在上述所有情況下，會以類似的方式執行作業（如果不相同）。</span><span class="sxs-lookup"><span data-stu-id="0707b-105">In all these cases, the operation is performed in a similar, if not identical, fashion.</span></span> <span data-ttu-id="0707b-106">指向傳回資料位置的參數將會使用標記法慣例，其中 pb 或 pv 是參數名稱的前兩個字元。</span><span class="sxs-lookup"><span data-stu-id="0707b-106">The parameter that points to the location of the returned data will use the notation convention where pb or pv are the first two characters of the parameter name.</span></span> <span data-ttu-id="0707b-107">另一個參數會以 pcb 作為參數名稱的前三個字元。</span><span class="sxs-lookup"><span data-stu-id="0707b-107">Another parameter will have pcb as the first three characters of the parameter name.</span></span> <span data-ttu-id="0707b-108">此參數代表將傳回至 pb 或 pv 位置之資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0707b-108">This parameter represents the size, in bytes, of the data that will be returned to the pb or pv location.</span></span> <span data-ttu-id="0707b-109">例如，請考慮下列函數規格：</span><span class="sxs-lookup"><span data-stu-id="0707b-109">For example, consider the following function specification:</span></span>

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

<span data-ttu-id="0707b-110">在此範例中， *>pbdata* 是將傳回資料的位置指標，而 *pcbData* 則是傳回資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0707b-110">In this example, *pbData* is a pointer to the location where the data will be returned, and *pcbData* is the size, in bytes, of the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="0707b-111">Pcb 參數的附屬參數有時可能會有稍微不同的前置詞，例如 p 或 pv。</span><span class="sxs-lookup"><span data-stu-id="0707b-111">The companion parameter to the pcb parameter may sometimes carry a slightly different prefix, such as p or pv.</span></span> <span data-ttu-id="0707b-112">此外，對於使用前置詞 pwsz 和 pcch 組合的參數，pcch 參數是傳回的資料的計數（以字元為單位 ([*Unicode*](../secgloss/u-gly.md) 或 [*ASCII*](../secgloss/a-gly.md)）（適用) ）。</span><span class="sxs-lookup"><span data-stu-id="0707b-112">Also, for companion parameters using the combination of prefixes pwsz and pcch, the pcch parameter is the count, in characters ([*Unicode*](../secgloss/u-gly.md) or [*ASCII*](../secgloss/a-gly.md), as applicable), of the returned data.</span></span>

 

<span data-ttu-id="0707b-113">如果 *>pbdata* 參數所指定的緩衝區不夠大，無法容納傳回的資料，此函式會設定錯誤的 \_ \_ 資料程式碼 (可透過呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式來查看) 並將所需的緩衝區大小（以位元組為單位）儲存在 *pcbData* 所指向的變數中。</span><span class="sxs-lookup"><span data-stu-id="0707b-113">If the buffer specified by the *pbData* parameter is not large enough to hold the returned data, the function sets the ERROR\_MORE\_DATA code (which can be seen by calling the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function) and stores the required buffer size, in bytes, in the variable pointed to by *pcbData*.</span></span>

<span data-ttu-id="0707b-114">如果 *>pbdata* 的輸入為 **Null** ，且 *pcbData* 不是 **null**，則不會傳回任何錯誤，且函式會傳回 *pcbData* 所指向之變數中所需記憶體緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0707b-114">If **NULL** is input for *pbData* and *pcbData* is not **NULL**, no error is returned, and the function returns the size, in bytes, of the needed memory buffer in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="0707b-115">這可讓應用程式判斷所傳回資料的大小，以及配置的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="0707b-115">This lets an application determine the size of, and the best way to allocate, a buffer for the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="0707b-116">當輸入 **Null** 做為 *>pbdata* 的輸入，以判斷所傳回的資料是否符合指定的緩衝區所需的大小時，第二次呼叫以所需資料填入緩衝區的函式，可能不會使用整個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0707b-116">When **NULL** is input for *pbData* to determine the size needed to ensure that the returned data fits in the specified buffer, the second call to the function which populates the buffer with the desired data may not use the whole buffer.</span></span> <span data-ttu-id="0707b-117">第二次呼叫之後，傳回的資料實際大小會包含在 *pcbData* 中。</span><span class="sxs-lookup"><span data-stu-id="0707b-117">After the second call, the actual size of the data returned is contained in *pcbData*.</span></span> <span data-ttu-id="0707b-118">處理資料時，請使用此大小。</span><span class="sxs-lookup"><span data-stu-id="0707b-118">Use this size when processing the data.</span></span>

 

<span data-ttu-id="0707b-119">下列範例會示範如何針對此用途來執行輸入和輸出參數。</span><span class="sxs-lookup"><span data-stu-id="0707b-119">The following example shows how input and output parameters might be implemented for this purpose.</span></span>


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



 

 
