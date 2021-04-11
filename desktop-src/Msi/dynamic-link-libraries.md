---
description: 自訂動作可以呼叫動態連結程式庫中所定義的函式， (DLL) 以 C 或 c + + 撰寫。
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: 'Dynamic-Link 程式庫 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026879"
---
# <a name="dynamic-link-libraries-windows-installer"></a><span data-ttu-id="63e77-103">Dynamic-Link 程式庫 (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="63e77-103">Dynamic-Link Libraries (Windows Installer)</span></span>

<span data-ttu-id="63e77-104">自訂動作可以呼叫動態連結程式庫中所定義的函式， (DLL) 以 C 或 c + + 撰寫。</span><span class="sxs-lookup"><span data-stu-id="63e77-104">A custom action can call a function defined in a dynamic-link library (DLL) written in C or C++.</span></span> <span data-ttu-id="63e77-105">DLL 可以是在目前安裝期間安裝的檔案，或是源自于安裝資料庫之 [二進位資料表](binary-table.md) 的暫存二進位資料流程。</span><span class="sxs-lookup"><span data-stu-id="63e77-105">The DLL can exist as a file installed during the current installation or as a temporary binary stream originating from the [Binary table](binary-table.md) of the installation database.</span></span>

<span data-ttu-id="63e77-106">請注意，任何已呼叫的函式（包括 Dll 中的自訂動作）都必須指定 \_ \_ stdcall 呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="63e77-106">Note that any called functions, including custom actions in DLLs, must specify the \_\_stdcall calling convention.</span></span> <span data-ttu-id="63e77-107">例如，若要呼叫 CustomAction，請使用下列程式。</span><span class="sxs-lookup"><span data-stu-id="63e77-107">For example, to call CustomAction use the following.</span></span>


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="63e77-108">如需詳細資訊，請參閱[從自訂動作內部存取目前的安裝程式會話](accessing-the-current-installer-session-from-inside-a-custom-action.md)。</span><span class="sxs-lookup"><span data-stu-id="63e77-108">For more information see, [Accessing the Current Installer Session from Inside a Custom Action](accessing-the-current-installer-session-from-inside-a-custom-action.md)</span></span>

<span data-ttu-id="63e77-109">下列自訂動作類型會呼叫動態連結程式庫。</span><span class="sxs-lookup"><span data-stu-id="63e77-109">The following types of custom actions call a dynamic-link library.</span></span>



| <span data-ttu-id="63e77-110">自訂動作類型</span><span class="sxs-lookup"><span data-stu-id="63e77-110">Custom action type</span></span>                                 | <span data-ttu-id="63e77-111">Description</span><span class="sxs-lookup"><span data-stu-id="63e77-111">Description</span></span>                               |
|----------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="63e77-112">自訂動作類型1</span><span class="sxs-lookup"><span data-stu-id="63e77-112">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="63e77-113">儲存在二進位資料表資料流程中的 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="63e77-113">DLL file stored in a Binary table stream.</span></span> |
| [<span data-ttu-id="63e77-114">自訂動作類型17</span><span class="sxs-lookup"><span data-stu-id="63e77-114">Custom Action Type 17</span></span>](custom-action-type-17.md) | <span data-ttu-id="63e77-115">與產品一起安裝的 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="63e77-115">DLL file installed with a product.</span></span>        |



 

> [!Note]  
> <span data-ttu-id="63e77-116">若要使用 COM，您需要在自訂動作中呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 。</span><span class="sxs-lookup"><span data-stu-id="63e77-116">To use COM you need to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in the custom action.</span></span> <span data-ttu-id="63e77-117">如果您發現執行緒已經初始化，請勿退出。</span><span class="sxs-lookup"><span data-stu-id="63e77-117">Do not quit if you find that the thread has already been initialized.</span></span> <span data-ttu-id="63e77-118">例如，執行緒會在個別電腦安裝中初始化，但不會在每個使用者安裝中初始化。</span><span class="sxs-lookup"><span data-stu-id="63e77-118">For example, the thread is initialized in a per-machine installation but not in a per-user installation.</span></span>

 

<span data-ttu-id="63e77-119">請參閱 [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md) ，以取得所有自訂動作類型的摘要，以及它們如何編碼至 [CustomAction 資料表](customaction-table.md)。</span><span class="sxs-lookup"><span data-stu-id="63e77-119">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction table](customaction-table.md).</span></span>

 

 
