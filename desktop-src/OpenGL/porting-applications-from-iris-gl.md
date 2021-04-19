---
title: 從鳶尾花 GL 移植應用程式
description: 從鳶尾花 GL 移植應用程式
ms.assetid: d410b516-76a1-4cab-a843-801aa6215db5
keywords:
- Windows 上的 OpenGL，鳶尾花 GL 移植
- 移植至 OpenGL、鳶尾花 GL
- OpenGL 移植，鳶尾花 GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c9e739b40f63bb2fd00bb62b4e5ec5566df3c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966825"
---
# <a name="porting-applications-from-iris-gl"></a><span data-ttu-id="e7abc-106">從鳶尾花 GL 移植應用程式</span><span class="sxs-lookup"><span data-stu-id="e7abc-106">Porting Applications from IRIS GL</span></span>

<span data-ttu-id="e7abc-107">本節列出鳶尾花 GL 和 OpenGL 之間的重要差異，並說明將程式碼從鳶尾花 GL 移植至 OpenGL 的基本步驟。</span><span class="sxs-lookup"><span data-stu-id="e7abc-107">This section lists important differences between IRIS GL and OpenGL and describes the basic steps for porting code from IRIS GL to OpenGL.</span></span> <span data-ttu-id="e7abc-108">如需鳶尾花 GL 和 Open GL 之間差異的完整清單，請參閱 [鳶尾花 gl 和 OpenGL 差異](iris-gl-and-opengl-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="e7abc-108">For a complete list of the differences between IRIS GL and Open GL, see [IRIS GL and OpenGL Differences](iris-gl-and-opengl-differences.md).</span></span>

<span data-ttu-id="e7abc-109">將鳶尾花 GL 程式移植到適用于 Windows 的 OpenGL 需要比從 X 視窗系統轉換 OpenGL 程式更多的工作。</span><span class="sxs-lookup"><span data-stu-id="e7abc-109">Porting IRIS GL programs to OpenGL for Windows requires considerably more work than converting OpenGL programs from the X Window System.</span></span> <span data-ttu-id="e7abc-110">雖然鳶尾花 GL 程式是設計來搭配特定的硬體和軟體來執行，但 OpenGL 是針對各種系統之間的可攜性而設計的。</span><span class="sxs-lookup"><span data-stu-id="e7abc-110">While IRIS GL programs are designed to run with specific hardware and software, OpenGL was designed for portability among various systems.</span></span>

<span data-ttu-id="e7abc-111">下表列出 OpenGL 與鳶尾花 GL 程式之間的一些主要差異。</span><span class="sxs-lookup"><span data-stu-id="e7abc-111">The following table lists some of the key differences between OpenGL and IRIS GL programs.</span></span>



| <span data-ttu-id="e7abc-112">OpenGL 程式碼</span><span class="sxs-lookup"><span data-stu-id="e7abc-112">OpenGL code</span></span>                                                                                                                                              | <span data-ttu-id="e7abc-113">鳶尾花 GL 程式碼</span><span class="sxs-lookup"><span data-stu-id="e7abc-113">IRIS GL code</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7abc-114">獨立作業系統;未包含視窗化、事件處理、緩衝區配置/管理等功能。</span><span class="sxs-lookup"><span data-stu-id="e7abc-114">Operating system independent; contains no functions for windowing, event handling, buffer allocation/management, and so on.</span></span>                              | <span data-ttu-id="e7abc-115">相依于作業系統;視窗化系統函數會與轉譯函數混合使用。</span><span class="sxs-lookup"><span data-stu-id="e7abc-115">Dependent on operating system; windowing-system functions are mixed with rendering functions.</span></span> <span data-ttu-id="e7abc-116">鳶尾花 GL 中沒有任何 windows 管理員。</span><span class="sxs-lookup"><span data-stu-id="e7abc-116">There is no windows manager in IRIS GL.</span></span> |
| <span data-ttu-id="e7abc-117">使用標準的通用命名慣例。</span><span class="sxs-lookup"><span data-stu-id="e7abc-117">Uses a standard, common naming convention.</span></span> <span data-ttu-id="e7abc-118">OpenGL 函數和定義型別開頭為 "gl" 前置詞，以防止與其他程式庫發生衝突。</span><span class="sxs-lookup"><span data-stu-id="e7abc-118">OpenGL functions and defined types begin with a "gl" prefix to prevent conflicts with other libraries.</span></span>        | <span data-ttu-id="e7abc-119">不使用函數和定義型別的一般命名慣例。</span><span class="sxs-lookup"><span data-stu-id="e7abc-119">Does not use a common naming convention for functions and defined types.</span></span>                                                              |
| <span data-ttu-id="e7abc-120">直接且一致地管理狀態變數 (例如色彩、霧化、材質、光源等) 。</span><span class="sxs-lookup"><span data-stu-id="e7abc-120">Manages state variables (such as color, fog, texture, lighting, and so on) directly and consistently.</span></span> <span data-ttu-id="e7abc-121">不使用資料表來載入狀態變數值。</span><span class="sxs-lookup"><span data-stu-id="e7abc-121">Does not use tables to load state-variable values.</span></span> | <span data-ttu-id="e7abc-122">使用資料表管理狀態變數，且必須將變數系結至資料表值。</span><span class="sxs-lookup"><span data-stu-id="e7abc-122">Uses tables to manage state variables and must bind variables to table values.</span></span>                                                        |
| <span data-ttu-id="e7abc-123">無法編輯顯示清單。</span><span class="sxs-lookup"><span data-stu-id="e7abc-123">Display lists cannot be edited.</span></span>                                                                                                                          | <span data-ttu-id="e7abc-124">可以編輯顯示清單。</span><span class="sxs-lookup"><span data-stu-id="e7abc-124">Display lists can be edited.</span></span>                                                                                                          |
| <span data-ttu-id="e7abc-125">未提供字型的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="e7abc-125">Does not provide a file format for fonts.</span></span>                                                                                                                | <span data-ttu-id="e7abc-126">提供函式來處理字型和文字字串以及字型的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="e7abc-126">Provides functions to handle fonts and text strings and a file format for fonts.</span></span>                                                      |
| <span data-ttu-id="e7abc-127">包含 GL 公用程式 (X.GLU 隊) 程式庫，其中包含額外的函式和常式 (例如 NURBS 和二次轉譯常式) 。</span><span class="sxs-lookup"><span data-stu-id="e7abc-127">Includes a GL Utility (GLU) library that contains additional functions and routines (such as NURBS and quadratic rendering routines).</span></span>                    | <span data-ttu-id="e7abc-128">不支援 X.GLU 隊程式庫。</span><span class="sxs-lookup"><span data-stu-id="e7abc-128">Does not support the GLU library.</span></span>                                                                                                     |



 

<span data-ttu-id="e7abc-129">**使用下列一般程式，將您的鳶尾花 GL 程式移植至 OpenGL**</span><span class="sxs-lookup"><span data-stu-id="e7abc-129">**Use the following general procedure to port your IRIS GL programs to OpenGL**</span></span>

1.  <span data-ttu-id="e7abc-130">重寫任何呼叫視窗管理員、視窗設定、裝置或事件的程式碼，或將色彩對應載入至對等的 Windows 程式碼。</span><span class="sxs-lookup"><span data-stu-id="e7abc-130">Rewrite any code that makes calls to a window manager, window configuration, device, or event, or where you load a color map to equivalent Windows code.</span></span> <span data-ttu-id="e7abc-131">將應用程式從一個作業系統重寫為另一個作業系統可能很複雜而且很困難。</span><span class="sxs-lookup"><span data-stu-id="e7abc-131">Rewriting an application from one operating system to another can be complex and difficult.</span></span> <span data-ttu-id="e7abc-132">本主題已超出本節的範圍。</span><span class="sxs-lookup"><span data-stu-id="e7abc-132">This subject is beyond the scope of this section.</span></span>
2.  <span data-ttu-id="e7abc-133">找出使用鳶尾花 GL 函數和常式的任何程式碼。</span><span class="sxs-lookup"><span data-stu-id="e7abc-133">Locate any code that uses IRIS GL functions and routines.</span></span> <span data-ttu-id="e7abc-134">將這些函式轉譯為其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="e7abc-134">Translate these functions to their equivalent OpenGL functions.</span></span> <span data-ttu-id="e7abc-135">如需鳶尾花 GL 函式和常式及其對等的 OpenGL 對應專案的完整清單，請參閱 OpenGL 函式 [及其鳶尾花 GL](opengl-functions-and-their-iris-gl-equivalents.md)對應專案。</span><span class="sxs-lookup"><span data-stu-id="e7abc-135">For a complete listing of IRIS GL functions and routines and their equivalent OpenGL counterparts, see [OpenGL Functions and Their IRIS GL Equivalents](opengl-functions-and-their-iris-gl-equivalents.md).</span></span>
3.  <span data-ttu-id="e7abc-136">變更鳶尾花 GL 程式碼，如 [特殊鳶尾花 Gl 移植問題](special-iris-gl-porting-issues.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e7abc-136">Change IRIS GL code as described in [Special IRIS GL Porting Issues](special-iris-gl-porting-issues.md).</span></span>

<!-- -->

1.  <span data-ttu-id="e7abc-137">重寫任何呼叫視窗管理員、視窗設定、裝置或事件的程式碼，或將色彩對應載入至對等的 Windows 程式碼。</span><span class="sxs-lookup"><span data-stu-id="e7abc-137">Rewrite any code that makes calls to a window manager, window configuration, device, or event, or where you load a color map to equivalent Windows code.</span></span> <span data-ttu-id="e7abc-138">將應用程式從一個作業系統重寫為另一個作業系統可能很複雜而且很困難。</span><span class="sxs-lookup"><span data-stu-id="e7abc-138">Rewriting an application from one operating system to another can be complex and difficult.</span></span> <span data-ttu-id="e7abc-139">本主題已超出本節的範圍。</span><span class="sxs-lookup"><span data-stu-id="e7abc-139">This subject is beyond the scope of this section.</span></span>
2.  <span data-ttu-id="e7abc-140">找出使用鳶尾花 GL 函數和常式的任何程式碼。</span><span class="sxs-lookup"><span data-stu-id="e7abc-140">Locate any code that uses IRIS GL functions and routines.</span></span> <span data-ttu-id="e7abc-141">將這些函式轉譯為其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="e7abc-141">Translate these functions to their equivalent OpenGL functions.</span></span> <span data-ttu-id="e7abc-142">如需鳶尾花 GL 函式和常式及其對等的 OpenGL 對應專案的完整清單，請參閱 OpenGL 函式 [及其鳶尾花 GL](opengl-functions-and-their-iris-gl-equivalents.md)對應專案。</span><span class="sxs-lookup"><span data-stu-id="e7abc-142">For a complete listing of IRIS GL functions and routines and their equivalent OpenGL counterparts, see [OpenGL Functions and Their IRIS GL Equivalents](opengl-functions-and-their-iris-gl-equivalents.md).</span></span>
3.  <span data-ttu-id="e7abc-143">變更鳶尾花 GL 程式碼，如 [特殊鳶尾花 Gl 移植問題](special-iris-gl-porting-issues.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e7abc-143">Change IRIS GL code as described in [Special IRIS GL Porting Issues](special-iris-gl-porting-issues.md).</span></span>

 

 




