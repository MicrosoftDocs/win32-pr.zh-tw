---
description: ShowJAVAConsole 函式是適用于 JAVA 開發人員的偵錯工具。 在 Internet Explorer 內執行的 applet (或其他 JAVA 程式碼) 可以用來顯示錯誤訊息和其他資訊。
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: ShowJAVAConsole 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 522885bfdd07843549375977630d8d1a7c6776f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977524"
---
# <a name="showjavaconsole-function"></a><span data-ttu-id="3196e-104">ShowJAVAConsole 函式</span><span class="sxs-lookup"><span data-stu-id="3196e-104">ShowJavaConsole function</span></span>

<span data-ttu-id="3196e-105">**ShowJAVAConsole** 函式是適用于 JAVA 開發人員的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="3196e-105">The **ShowJavaConsole** function is a debugging aid for Java developers.</span></span> <span data-ttu-id="3196e-106">在 Internet Explorer 內執行的 applet (或其他 JAVA 程式碼) 可以用來顯示錯誤訊息和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="3196e-106">Applets (or other Java code) running within Internet Explorer can use it to display error messages and other information.</span></span>

## <a name="syntax"></a><span data-ttu-id="3196e-107">語法</span><span class="sxs-lookup"><span data-stu-id="3196e-107">Syntax</span></span>


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a><span data-ttu-id="3196e-108">參數</span><span class="sxs-lookup"><span data-stu-id="3196e-108">Parameters</span></span>

<span data-ttu-id="3196e-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="3196e-109">This function has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="3196e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3196e-110">Return value</span></span>

<span data-ttu-id="3196e-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3196e-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3196e-112">備註</span><span class="sxs-lookup"><span data-stu-id="3196e-112">Remarks</span></span>

<span data-ttu-id="3196e-113">呼叫 **ShowJAVAConsole** 會導致 java 虛擬機器 (VM) 顯示 java 主控台視窗。</span><span class="sxs-lookup"><span data-stu-id="3196e-113">Calling **ShowJavaConsole** causes the Java virtual machine (VM) to display the Java console window.</span></span> <span data-ttu-id="3196e-114">JAVA 主控台視窗本身可以顯示在呼叫進程中執行的 JAVA 程式碼的偵錯工具輸出。</span><span class="sxs-lookup"><span data-stu-id="3196e-114">The Java console window itself can display debugging output from Java code running in the calling process.</span></span> <span data-ttu-id="3196e-115">一般來說，這僅供裝載 JAVA VM 的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="3196e-115">Typically, this would be used only by an application hosting the Java VM.</span></span> <span data-ttu-id="3196e-116">每個進程只有一個 JAVA 主控台視窗;對 API 的多個呼叫會導致相同的視窗顯示。</span><span class="sxs-lookup"><span data-stu-id="3196e-116">There is only a single Java console window per process; multiple calls to the API result in the same window being displayed.</span></span> <span data-ttu-id="3196e-117">換句話說，如果主控台視窗已經顯示，就不會發生任何事;如果視窗尚未顯示，或使用者已關閉，則會快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="3196e-117">In other words, if the console window is already displayed, nothing happens; if the window has not been displayed, or the user has closed it, then the window pops up.</span></span>

<span data-ttu-id="3196e-118">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="3196e-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3196e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3196e-119">Requirements</span></span>



| <span data-ttu-id="3196e-120">需求</span><span class="sxs-lookup"><span data-stu-id="3196e-120">Requirement</span></span> | <span data-ttu-id="3196e-121">值</span><span class="sxs-lookup"><span data-stu-id="3196e-121">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3196e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3196e-122">DLL</span></span><br/> | <dl> <span data-ttu-id="3196e-123"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3196e-123"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
