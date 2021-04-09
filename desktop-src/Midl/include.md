---
title: include 屬性
description: ACF include 語句會指定要包含在產生的存根程式碼中的一或多個標頭檔。
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- 包含屬性 MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092349"
---
# <a name="include-attribute"></a><span data-ttu-id="f2864-104">include 屬性</span><span class="sxs-lookup"><span data-stu-id="f2864-104">include attribute</span></span>

<span data-ttu-id="f2864-105">ACF **include** 語句會指定要包含在產生的存根程式碼中的一或多個標頭檔。</span><span class="sxs-lookup"><span data-stu-id="f2864-105">The ACF **include** statement specifies one or more header files to be included in the generated stub code.</span></span>

``` syntax
include filenames;
```

## <a name="parameters"></a><span data-ttu-id="f2864-106">參數</span><span class="sxs-lookup"><span data-stu-id="f2864-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2864-107">*檔案名*</span><span class="sxs-lookup"><span data-stu-id="f2864-107">*filenames*</span></span> 
</dt> <dd>

<span data-ttu-id="f2864-108">指定一或多個 C 語言標頭檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2864-108">Specifies the name of one or more C-language header files.</span></span> <span data-ttu-id="f2864-109">使用完整的檔案名，包括。H 副檔名並以引號括住每個檔案名。</span><span class="sxs-lookup"><span data-stu-id="f2864-109">Use the full file name, including the .H extension and enclose each file name in quotation marks.</span></span> <span data-ttu-id="f2864-110">以逗號分隔多個 C 語言標頭檔名稱。</span><span class="sxs-lookup"><span data-stu-id="f2864-110">Separate multiple C-language header file names with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2864-111">備註</span><span class="sxs-lookup"><span data-stu-id="f2864-111">Remarks</span></span>

<span data-ttu-id="f2864-112">由於 **include** 語句的結果，產生的 stub 程式碼將包含 C 預處理器 **\# include** 語句。</span><span class="sxs-lookup"><span data-stu-id="f2864-112">As a result of the **include** statement, the generated stub code will contain a C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="f2864-113">您會在編譯存根時提供 C 語言標頭檔。</span><span class="sxs-lookup"><span data-stu-id="f2864-113">You supply the C-language header file when compiling the stubs.</span></span> <span data-ttu-id="f2864-114">Include 語句依賴 C 編譯器機制來搜尋目錄結構中包含的檔案。</span><span class="sxs-lookup"><span data-stu-id="f2864-114">Include statements rely on the C-compiler mechanism of searching the directory structure for included files.</span></span>

> [!Note]  
> <span data-ttu-id="f2864-115">使用匯 [**入**](import.md) 指示詞，而不是包含您想要提供給 IDL 檔案之資料類型之系統檔案的 **include** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="f2864-115">Use the [**import**](import.md) directive rather than the **include** directive for system files that contain data types you want to make available to the IDL file.</span></span> <span data-ttu-id="f2864-116">匯 **入** 指示詞會忽略函式原型，並可讓您使用 MIDL 編譯器參數，以優化支援常式的產生。</span><span class="sxs-lookup"><span data-stu-id="f2864-116">The **import** directive ignores function prototypes and allows you to use MIDL compiler switches that optimize the generation of support routines.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f2864-117">範例</span><span class="sxs-lookup"><span data-stu-id="f2864-117">Examples</span></span>

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a><span data-ttu-id="f2864-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2864-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2864-119">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="f2864-119">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="f2864-120">**進口**</span><span class="sxs-lookup"><span data-stu-id="f2864-120">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="f2864-121">匯入檔案和型別程式庫</span><span class="sxs-lookup"><span data-stu-id="f2864-121">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="f2864-122">匯入系統標頭檔</span><span class="sxs-lookup"><span data-stu-id="f2864-122">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




