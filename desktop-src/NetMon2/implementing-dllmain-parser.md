---
description: 網路監視器使用 DllMain 匯出函式來識別剖析器是否存在，以及釋放網路監視器用來儲存剖析器相關資訊的資源。
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: 執行 DllMain 剖析器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55dd1ab7432920ac7496643c7c6f9aa0692daf56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689703"
---
# <a name="implementing-dllmain-parser"></a><span data-ttu-id="f1280-103">執行 DllMain 剖析器</span><span class="sxs-lookup"><span data-stu-id="f1280-103">Implementing DllMain Parser</span></span>

<span data-ttu-id="f1280-104">網路監視器使用 **DllMain** 匯出函式來識別剖析器是否存在，以及釋放網路監視器用來儲存剖析器相關資訊的資源。</span><span class="sxs-lookup"><span data-stu-id="f1280-104">Network Monitor uses the **DllMain** export function to identify the existence of the parser, and release resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="f1280-105">當網路監視器第一次呼叫 **DllMain** 時，剖析器 DLL 會呼叫 [**CreateProtocol**](createprotocol.md) 來執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="f1280-105">When Network Monitor calls **DllMain** for the first time, the parser DLL calls [**CreateProtocol**](createprotocol.md) to do the following:</span></span>

-   <span data-ttu-id="f1280-106">指定剖析器偵測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f1280-106">Specify the protocol that the parser detects.</span></span>
-   <span data-ttu-id="f1280-107">針對網路監視器呼叫的其餘剖析器匯出函數提供進入點。</span><span class="sxs-lookup"><span data-stu-id="f1280-107">Provide entry points for remaining parser export functions that Network Monitor calls.</span></span>

<span data-ttu-id="f1280-108">當網路監視器上次呼叫 **dllmain** 時， **Dllmain** 會呼叫 [**DestroyProtocol**](destroyprotocol.md) ，釋放網路監視器用來儲存剖析器相關資訊的所有資源。</span><span class="sxs-lookup"><span data-stu-id="f1280-108">When Network Monitor calls **DllMain** for the last time, **DllMain** calls [**DestroyProtocol**](destroyprotocol.md) to release all resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="f1280-109">下列程式識別執行 **DllMain** 所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="f1280-109">The following procedure identifies the steps necessary to implement **DllMain**.</span></span>

<span data-ttu-id="f1280-110">**若要執行 DllMain**</span><span class="sxs-lookup"><span data-stu-id="f1280-110">**To implement DllMain**</span></span>

1.  <span data-ttu-id="f1280-111">指定 [**CreateProtocol**](createprotocol.md)函數和全域附加變數的 [**e**](entrypoints.md)結構。</span><span class="sxs-lookup"><span data-stu-id="f1280-111">Specify the [**ENTRYPOINTS**](entrypoints.md) structure for the [**CreateProtocol**](createprotocol.md) function and global Attach variable.</span></span> <span data-ttu-id="f1280-112">Attach 變數用來追蹤正在執行的通訊協定實例數目。</span><span class="sxs-lookup"><span data-stu-id="f1280-112">The Attach variable is used to track the number of protocol instances that are running.</span></span>
2.  <span data-ttu-id="f1280-113">查看作業系統所設定的 *命令* 參數值。</span><span class="sxs-lookup"><span data-stu-id="f1280-113">Look at the value of the *Command* parameter that the operating system sets.</span></span>

    <span data-ttu-id="f1280-114">如果 *命令* 參數設定為 DLL \_ 進程 \_ 附加且附加為0，則呼叫 [**CreateProtocol**](createprotocol.md) 以提供下列匯出函數的通訊協定名稱和進入點。</span><span class="sxs-lookup"><span data-stu-id="f1280-114">If the *Command* parameter is set to DLL\_PROCESS\_ATTACH and Attach is 0, then call [**CreateProtocol**](createprotocol.md) to provide the protocol name and entry points for the following export functions.</span></span>

    -   <span data-ttu-id="f1280-115">**註冊**</span><span class="sxs-lookup"><span data-stu-id="f1280-115">**Register**</span></span>
    -   <span data-ttu-id="f1280-116">**取消註冊**</span><span class="sxs-lookup"><span data-stu-id="f1280-116">**Deregister**</span></span>
    -   <span data-ttu-id="f1280-117">**RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="f1280-117">**RecognizeFrame**</span></span>
    -   <span data-ttu-id="f1280-118">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="f1280-118">**AttachProperties**</span></span>
    -   <span data-ttu-id="f1280-119">只有網路監視器將會顯示) 的通訊協定屬性時，才需要 **FormatProperties** (。</span><span class="sxs-lookup"><span data-stu-id="f1280-119">**FormatProperties** (only required if Network Monitor will be displaying the protocol properties).</span></span>

    <span data-ttu-id="f1280-120">如果 *命令* 參數設定為 DLL 進程卸 \_ \_ 離且附加為0，則使用 [**CreateProtocol**](createprotocol.md)傳回的實例控制碼來呼叫 [**DestroyProtocol**](destroyprotocol.md) 。</span><span class="sxs-lookup"><span data-stu-id="f1280-120">If the *Command* parameter is set to DLL\_PROCESS\_DETACH and Attach is 0, then call [**DestroyProtocol**](destroyprotocol.md) using the instance handle that [**CreateProtocol**](createprotocol.md) returns.</span></span>

3.  <span data-ttu-id="f1280-121">傳回 **true** ，因為 **DllMain** 剖析器函式必須一律傳回 **true**。</span><span class="sxs-lookup"><span data-stu-id="f1280-121">Return **TRUE** because the **DllMain** parser function must always return **TRUE**.</span></span>

<span data-ttu-id="f1280-122">以下是 **DllMain** 的基本執行。</span><span class="sxs-lookup"><span data-stu-id="f1280-122">The following is a basic implementation of **DllMain**.</span></span> <span data-ttu-id="f1280-123">此程式碼範例會使用 case 語句來設陷 *命令* 參數的值，以判斷是否應該呼叫 [**CreateProtocol**](createprotocol.md) 或 [**DestroyProtocol**](destroyprotocol.md) 。</span><span class="sxs-lookup"><span data-stu-id="f1280-123">The code example uses a case statement to trap values of the *Command* parameter to determine if [**CreateProtocol**](createprotocol.md) or [**DestroyProtocol**](destroyprotocol.md) should be called.</span></span>

``` syntax
#include <windows.h>

// Entry point structure for parser export functions and global
// Attach variable.
ENTRYPOINTS EntryPoints =
{
  Register,
  Deregister,
  RecognizeFrame,
  AttachProperties,
  FormatProperties
};

DWORD Attached = 0; 

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved)
{
  switch(Command)
  {
  // Call CreateProtocol.
  case DLL_PROCESS_ATTACH:
       // Loading parser DLL.
       if(Attached == 0)
       {
         hProtocol = CreateProtocol( "ProtocolName",
                                     &EntryPoints,
                                     ENTRYPOINTS_SIZE);
       }
       Attached++;
       break;
  // Call DestroyProtocol.
  case DLL_PROCESS_DETACH:
       // Unloading parser DLL.
       Attached--;
       if(Attached == 0)
       {
         DestroyProtocol( hProtocol);
       }
       break;
  }
  return TRUE;
}
```

 

 



