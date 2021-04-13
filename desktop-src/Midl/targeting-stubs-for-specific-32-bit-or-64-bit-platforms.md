---
title: 以特定32位或64位平臺為目標的存根
description: Microsoft RPC 和 MIDL 3.0 和更新版本編譯器的部分功能是平臺特定的功能。
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- 32位平臺 MIDL
- 64位平臺 MIDL
- stub MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526265a60f8b2ef2f31d19d0356d4ec3a3ae8c8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301568"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a><span data-ttu-id="af456-106">以特定32位或64位平臺為目標的存根</span><span class="sxs-lookup"><span data-stu-id="af456-106">Targeting Stubs for Specific 32-bit or 64-bit Platforms</span></span>

<span data-ttu-id="af456-107">Microsoft RPC 和 MIDL 3.0 和更新版本編譯器的部分功能是平臺特定的功能。</span><span class="sxs-lookup"><span data-stu-id="af456-107">Some of the features of Microsoft RPC and the MIDL 3.0 and later compilers are platform-specific.</span></span>

<span data-ttu-id="af456-108">為了預防起見，MIDL 3.0 和更新版本的編譯器會產生防止在 C 編譯階段進行相容性檢查的防護。</span><span class="sxs-lookup"><span data-stu-id="af456-108">As a precaution, the MIDL 3.0 and later compilers generate guards that facilitate compatibility checking during the C-compilation phase.</span></span> <span data-ttu-id="af456-109">MIDL 會產生兩種類型的防護：與平臺相關的防護 (32 位和64位) ，以及相依于 (功能集相依性) 的相依性防護。</span><span class="sxs-lookup"><span data-stu-id="af456-109">MIDL generates two types of guards: a platform-dependent guard (32-bit versus 64-bit) and a release-dependent guard (feature set dependency).</span></span> <span data-ttu-id="af456-110">例如，MIDL 會產生下列防護，以防止 C-編譯其他平臺的32位存根：</span><span class="sxs-lookup"><span data-stu-id="af456-110">For example, MIDL generates the following guard to prevent C-compiling of a 32-bit stub for other platforms:</span></span>

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

<span data-ttu-id="af456-111">發行相依的防護是由在處理的 IDL 檔案 (s) 和 [**/target**](-target.md) 參數中找到的一組功能所觸發。</span><span class="sxs-lookup"><span data-stu-id="af456-111">The release-dependent guard is triggered by a set of features found in the processed IDL file(s) and by the [**/target**](-target.md) switch.</span></span> <span data-ttu-id="af456-112">例如，如果介面使用僅在 Windows 2000 或更新版本上支援的功能，MIDL 會產生具有目標 \_ \_ NT50 \_ 或 \_ 更新版本宏的防護。</span><span class="sxs-lookup"><span data-stu-id="af456-112">For example, if the interface uses features supported only on WindowsÂ 2000 or later, MIDL generates a guard with the TARGET\_IS\_NT50\_OR\_LATER macro.</span></span>

<span data-ttu-id="af456-113">Rpcndr 中定義的 guard 宏取決於 WINVER 和 WIN32 WINNT 的設定， \_ \_ 並由 C/c + + 編譯器進行評估。</span><span class="sxs-lookup"><span data-stu-id="af456-113">The guard macros, defined in Rpcndr.h, depend on the setting of WINVER and \_WIN32\_WINNT and are evaluated by the C/C++ compiler.</span></span>

<span data-ttu-id="af456-114">如果您在 C 編譯時間收到錯誤訊息，指出您需要特定平臺來執行存根，請先檢查以確定您未使用此平臺上無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="af456-114">If, at C-compile time, you get an error message indicating that you need a specific platform to run a stub, first check to make sure you have not used a feature that is not available on this platform.</span></span> <span data-ttu-id="af456-115">觸發特定防護的功能會列在此防護主體中。</span><span class="sxs-lookup"><span data-stu-id="af456-115">The features triggering a particular guard are listed in the body of the guard.</span></span> <span data-ttu-id="af456-116">在上述範例中，-Oicf 編譯器參數觸發了此防護。</span><span class="sxs-lookup"><span data-stu-id="af456-116">In the previous example, the -Oicf compiler switch triggered the guard.</span></span> <span data-ttu-id="af456-117">這種類型的值得注意的功能包括 [**/robust**](-robust.md)參數和 \[ [](async.md) \] windows 2000 和更新版本上可用的 async 屬性、[**管道**](pipe.md)類型的函式、/Oif 編譯器選項，以及 \[ [**使用者 \_ 封送**](user-marshal.md)處理 \] 和 \[ [**網路 \_ 封送**](wire-marshal.md)處理 \] 屬性。</span><span class="sxs-lookup"><span data-stu-id="af456-117">Notable features of this kind include the [**/robust**](-robust.md) switch and the \[[**async**](async.md)\] attribute available on WindowsÂ 2000 and later, the [**pipe**](pipe.md) type constructor, the /Oif compiler option, and the \[[**user\_marshal**](user-marshal.md)\] and \[[**wire\_marshal**](wire-marshal.md)\] attributes.</span></span> <span data-ttu-id="af456-118">使用這些功能的存根將無法在舊版系統上執行。</span><span class="sxs-lookup"><span data-stu-id="af456-118">Stubs using these features will not run on earlier systems.</span></span>

<span data-ttu-id="af456-119">如果您知道您的目標平臺對您所使用的功能而言是正確的，但仍收到錯誤，您可能需要適當地設定環境變數。</span><span class="sxs-lookup"><span data-stu-id="af456-119">If you know that your target platform is correct for the features you are using and still receive an error, you may need to set the environment variables appropriately.</span></span>

<span data-ttu-id="af456-120">**若要建立 Windows 2000 或更新版本**</span><span class="sxs-lookup"><span data-stu-id="af456-120">**To build for WindowsÂ 2000 or later releases**</span></span>

-   <span data-ttu-id="af456-121">將這一行新增至您的 makefile：</span><span class="sxs-lookup"><span data-stu-id="af456-121">Add this line to your makefile:</span></span>

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a><span data-ttu-id="af456-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="af456-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af456-123">**/target**</span><span class="sxs-lookup"><span data-stu-id="af456-123">**/target**</span></span>](-target.md)
</dt> <dt>

[<span data-ttu-id="af456-124">**/robust**</span><span class="sxs-lookup"><span data-stu-id="af456-124">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="af456-125">**async**</span><span class="sxs-lookup"><span data-stu-id="af456-125">**async**</span></span>](async.md)
</dt> <dt>

[<span data-ttu-id="af456-126">**非同步 \_ uuid**</span><span class="sxs-lookup"><span data-stu-id="af456-126">**async\_uuid**</span></span>](async-uuid.md)
</dt> <dt>

[<span data-ttu-id="af456-127">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="af456-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="af456-128">**管道**</span><span class="sxs-lookup"><span data-stu-id="af456-128">**pipe**</span></span>](pipe.md)
</dt> <dt>

[<span data-ttu-id="af456-129">**網路 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="af456-129">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="af456-130">**使用者 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="af456-130">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="af456-131">封送處理 OLE 資料類型</span><span class="sxs-lookup"><span data-stu-id="af456-131">Marshaling OLE Data Types</span></span>](marshaling-ole-data-types.md)
</dt> </dl>

 

 




