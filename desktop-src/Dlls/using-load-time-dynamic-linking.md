---
description: 建立 DLL 之後，您可以使用它在應用程式中定義的函式。 以下是簡單的主控台應用程式，它會使用從 Myputs.dll 匯出的 myPuts 函式 (請參閱建立簡單的 Dynamic-Link 程式庫) 。
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: 使用 Load-Time 動態連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e5d14ba2190528c44d892b957d22b273fd4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999874"
---
# <a name="using-load-time-dynamic-linking"></a><span data-ttu-id="d2c04-104">使用 Load-Time 動態連結</span><span class="sxs-lookup"><span data-stu-id="d2c04-104">Using Load-Time Dynamic Linking</span></span>

<span data-ttu-id="d2c04-105">建立 DLL 之後，您可以使用它在應用程式中定義的函式。</span><span class="sxs-lookup"><span data-stu-id="d2c04-105">After you have created a DLL, you can use the functions it defines in an application.</span></span> <span data-ttu-id="d2c04-106">以下是簡單的主控台應用程式，它會使用從 Myputs.dll 匯出的 myPuts 函式 (請參閱 [建立簡單的 Dynamic-Link 程式庫](creating-a-simple-dynamic-link-library.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d2c04-106">The following is a simple console application that uses the myPuts function exported from Myputs.dll (see [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).</span></span>

<span data-ttu-id="d2c04-107">由於這個範例會明確呼叫 DLL 函式，因此應用程式的模組必須與匯入程式庫 Myputs 連結。</span><span class="sxs-lookup"><span data-stu-id="d2c04-107">Because this example calls the DLL function explicitly, the module for the application must be linked with the import library Myputs.lib.</span></span> <span data-ttu-id="d2c04-108">如需建立 Dll 的詳細資訊，請參閱您的開發工具隨附的檔。</span><span class="sxs-lookup"><span data-stu-id="d2c04-108">For more information about building DLLs, see the documentation included with your development tools.</span></span>


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a><span data-ttu-id="d2c04-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2c04-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2c04-110">載入時間動態連結</span><span class="sxs-lookup"><span data-stu-id="d2c04-110">Load-Time Dynamic Linking</span></span>](load-time-dynamic-linking.md)
</dt> </dl>

 

 



