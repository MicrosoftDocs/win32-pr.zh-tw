---
title: LIBMAIN.Cpp
description: 在範例提供者元件中，Adssmp.dll 標準 DLL 進入點的程式碼範例位於 Libmain .cpp 中。 下表列出支援的常式。
ms.assetid: aa05fbd1-509d-4ed6-8a49-1ce11ce54c0e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e309d3c6454901b26f5ab67351033b39d73dd7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968409"
---
# <a name="libmaincpp"></a><span data-ttu-id="d087d-104">LIBMAIN.Cpp</span><span class="sxs-lookup"><span data-stu-id="d087d-104">LIBMAIN.CPP</span></span>

<span data-ttu-id="d087d-105">在範例提供者元件中，Adssmp.dll 標準 DLL 進入點的程式碼範例位於 Libmain .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="d087d-105">In the example provider component, a code example of the standard DLL entry point for Adssmp.dll is in Libmain.cpp.</span></span> <span data-ttu-id="d087d-106">下表列出支援的常式。</span><span class="sxs-lookup"><span data-stu-id="d087d-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="d087d-107">項目</span><span class="sxs-lookup"><span data-stu-id="d087d-107">Item</span></span>                                  | <span data-ttu-id="d087d-108">描述</span><span class="sxs-lookup"><span data-stu-id="d087d-108">Description</span></span>                                                              |
|---------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="d087d-109">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="d087d-109">**DllGetClassObject**</span></span><br/>      | <span data-ttu-id="d087d-110">用來尋找 class factory 的標準 DLL 進入點。</span><span class="sxs-lookup"><span data-stu-id="d087d-110">Standard DLL entry point for locating class factories.</span></span><br/>        |
| <span data-ttu-id="d087d-111">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="d087d-111">**DllCanUnloadNow**</span></span><br/>        | <span data-ttu-id="d087d-112">標準 DLL 進入點，用來判斷 DLL 是否可以卸載。</span><span class="sxs-lookup"><span data-stu-id="d087d-112">Standard DLL entry point to determine if DLL can be unloaded.</span></span><br/> |
| <span data-ttu-id="d087d-113">**LibMain**</span><span class="sxs-lookup"><span data-stu-id="d087d-113">**LibMain**</span></span><br/>                | <span data-ttu-id="d087d-114">標準 DLL 初始化進入點。</span><span class="sxs-lookup"><span data-stu-id="d087d-114">Standard DLL initialization entry point.</span></span><br/>                      |
| <span data-ttu-id="d087d-115">**IsCompatibleOleVersion**</span><span class="sxs-lookup"><span data-stu-id="d087d-115">**IsCompatibleOleVersion**</span></span><br/> | <span data-ttu-id="d087d-116">確認與 OLE 執行時間的相容性。</span><span class="sxs-lookup"><span data-stu-id="d087d-116">Verify compatibility with the OLE run time.</span></span><br/>                   |
| <span data-ttu-id="d087d-117">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="d087d-117">**DllMain**</span></span><br/>                | <span data-ttu-id="d087d-118">大部分 Windows 2000 或 Windows NT 版本的進入點。</span><span class="sxs-lookup"><span data-stu-id="d087d-118">Entry point for most Windows 2000 or Windows NT versions.</span></span><br/>     |



 

 

 





