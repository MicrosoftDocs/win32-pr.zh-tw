---
description: TopoEdit 模組
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: TopoEdit 模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026531"
---
# <a name="topoedit-modules"></a><span data-ttu-id="bd815-103">TopoEdit 模組</span><span class="sxs-lookup"><span data-stu-id="bd815-103">TopoEdit Modules</span></span>

<span data-ttu-id="bd815-104">TopoEdit 工具隨附于 Windows Server 2008 和更新版本的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="bd815-104">The TopoEdit tool is provided with the Windows SDK for Windows Server 2008 and later.</span></span> <span data-ttu-id="bd815-105">此工具需要 Windows Vista 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="bd815-105">The tool requires Windows Vista or later.</span></span>

<span data-ttu-id="bd815-106">TopoEdit 模組位於 SDK 的 Bin 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="bd815-106">The TopoEdit modules are located in the Bin folder of the SDK.</span></span> <span data-ttu-id="bd815-107">這些模組包括：</span><span class="sxs-lookup"><span data-stu-id="bd815-107">These modules are:</span></span>

-   <span data-ttu-id="bd815-108">TopoEdit.exe-應用程式可執行檔</span><span class="sxs-lookup"><span data-stu-id="bd815-108">TopoEdit.exe—Application executable</span></span>
-   <span data-ttu-id="bd815-109">TEDUTIL.dll-擴充 DLL</span><span class="sxs-lookup"><span data-stu-id="bd815-109">TEDUTIL.dll—Extension DLL</span></span>

<span data-ttu-id="bd815-110">SDK 安裝會註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="bd815-110">The SDK installation registers the DLL.</span></span> <span data-ttu-id="bd815-111">但是，如果失敗，請在命令提示字元中執行下列命令。</span><span class="sxs-lookup"><span data-stu-id="bd815-111">However, if this fails, at a command prompt, run the following.</span></span>


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



<span data-ttu-id="bd815-112">TopoEdit 的原始程式碼也提供為 Windows SDK 中的範例。</span><span class="sxs-lookup"><span data-stu-id="bd815-112">Source code for TopoEdit is also provided as a sample in the Windows SDK.</span></span> <span data-ttu-id="bd815-113">它位於下列目錄：</span><span class="sxs-lookup"><span data-stu-id="bd815-113">It is located in the following directory:</span></span>

<span data-ttu-id="bd815-114"><samples root>\\多媒體 \\ 媒體基礎 \\ TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bd815-114"><samples root>\\Multimedia\\Media Foundation\\TopoEdit</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd815-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd815-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd815-116">TopoEdit 簡介</span><span class="sxs-lookup"><span data-stu-id="bd815-116">Introduction to TopoEdit</span></span>](introduction-to-topoedit.md)
</dt> <dt>

[<span data-ttu-id="bd815-117">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="bd815-117">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



