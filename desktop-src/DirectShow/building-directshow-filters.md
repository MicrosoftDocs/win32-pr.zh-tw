---
description: 建立 DirectShow 篩選器
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: 建立 DirectShow 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5553c4358f97809214ebbdea23c129aa7c214e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688212"
---
# <a name="building-directshow-filters"></a><span data-ttu-id="e8e5f-103">建立 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="e8e5f-103">Building DirectShow Filters</span></span>

<span data-ttu-id="e8e5f-104">建議使用 DirectShow 基類來實行 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-104">The DirectShow base classes are recommended for implementing DirectShow filters.</span></span> <span data-ttu-id="e8e5f-105">若要使用基類建立，請執行下列步驟，以及 [設定組建環境](setting-up-the-build-environment.md)所列的步驟：</span><span class="sxs-lookup"><span data-stu-id="e8e5f-105">To build with the base classes, perform the following steps, in addition to the steps listed in [Setting Up the Build Environment](setting-up-the-build-environment.md):</span></span>

-   <span data-ttu-id="e8e5f-106">在 \\ \\ \\ SDK 根目錄下，建立位於目錄範例多媒體 DirectShow BaseClasses 中的基類庫。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-106">Build the base class library, located in the directory Samples\\Multimedia\\DirectShow\\BaseClasses, under the SDK root directory.</span></span> <span data-ttu-id="e8e5f-107">程式庫有兩個版本：零售版 (Strmbase) 和 (Strmbasd .lib) 的 debug 版本。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-107">There are two versions of the library: a retail version (Strmbase.lib) and a debug version (Strmbasd.lib).</span></span>
-   <span data-ttu-id="e8e5f-108">包含標頭檔資料流程 .h。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-108">Include the header file Streams.h.</span></span>
-   <span data-ttu-id="e8e5f-109">使用 \_ \_ stdcall 呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-109">Use the \_\_stdcall calling convention.</span></span>
-   <span data-ttu-id="e8e5f-110">使用多執行緒 C 執行時間程式庫 (debug 或 retail，如適當的) 。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-110">Use the multithreaded C run-time library (debug or retail, as appropriate).</span></span>
-   <span data-ttu-id="e8e5f-111">包含匯出 DLL 函式 ( .def) 檔案的定義。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-111">Include a definition (.def) file that exports the DLL functions.</span></span> <span data-ttu-id="e8e5f-112">以下是定義檔的範例。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-112">The following is an example of a definition file.</span></span> <span data-ttu-id="e8e5f-113">它會假設輸出檔的名稱是 MyFilter.dll。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-113">It assumes that the output file is named MyFilter.dll.</span></span>
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   <span data-ttu-id="e8e5f-114">連結至下列程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-114">Link to the following lib files.</span></span>

    |              |                                      |
    |--------------|--------------------------------------|
    | <span data-ttu-id="e8e5f-115">Debug 組建</span><span class="sxs-lookup"><span data-stu-id="e8e5f-115">Debug Build</span></span>  | <span data-ttu-id="e8e5f-116">Strmbasd .lib、Msvcrtd.lib .lib、Winmm.dll .lib</span><span class="sxs-lookup"><span data-stu-id="e8e5f-116">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span></span> |
    | <span data-ttu-id="e8e5f-117">零售組建</span><span class="sxs-lookup"><span data-stu-id="e8e5f-117">Retail Build</span></span> | <span data-ttu-id="e8e5f-118">Strmbase .lib、Msvcrt.lib .lib、Winmm.dll .lib</span><span class="sxs-lookup"><span data-stu-id="e8e5f-118">Strmbase.lib, Msvcrt.lib, Winmm.lib</span></span>  |

    

     

-   <span data-ttu-id="e8e5f-119">選擇連結器設定中的 [忽略預設程式庫] 選項。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-119">Choose the "ignore default libraries" option in the linker settings.</span></span>
-   <span data-ttu-id="e8e5f-120">在原始程式碼中宣告 DLL 進入點，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e8e5f-120">Declare the DLL entry point in your source code, as follows:</span></span>
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

<span data-ttu-id="e8e5f-121">舊版本</span><span class="sxs-lookup"><span data-stu-id="e8e5f-121">Previous Versions</span></span>

<span data-ttu-id="e8e5f-122">針對 DirectShow 9.0 之前的基類庫版本，您也必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e8e5f-122">For versions of the base class library before DirectShow 9.0, you must also do the following:</span></span>

-   <span data-ttu-id="e8e5f-123">針對 debug 組建，請定義預處理器旗標的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-123">For debug builds, define the preprocessor flag DEBUG.</span></span>

<span data-ttu-id="e8e5f-124">DirectShow 9.0 和更新版本中可用的基類庫版本不需要執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="e8e5f-124">This step is not required for the version of the base class library that is available in DirectShow 9.0 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8e5f-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8e5f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8e5f-126">DirectShow 基類</span><span class="sxs-lookup"><span data-stu-id="e8e5f-126">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="e8e5f-127">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="e8e5f-127">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



