---
title: 為64位 Windows 準備您的應用程式
description: 有幾項功能可讓您更輕鬆地開發將在32和64位的 Windows 上執行的應用程式。 其中大部分（例如新的資料類型）都是在準備進行64位 Windows 時所述。
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- 64位工具組64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f3b40d2fb22b84abdd4322f476981dc54c7ad3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186079"
---
# <a name="preparing-your-application-for-64-bit-windows"></a><span data-ttu-id="f3f72-105">為64位 Windows 準備您的應用程式</span><span class="sxs-lookup"><span data-stu-id="f3f72-105">Preparing Your Application for 64-bit Windows</span></span>

<span data-ttu-id="f3f72-106">有幾項功能可讓您更輕鬆地開發將在32和64位的 Windows 上執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f3f72-106">There are several features that make it easier for you to develop applications that will run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="f3f72-107">其中大部分（例如新的資料類型）都是在 [準備進行64位 Windows](getting-ready-for-64-bit-windows.md)時所述。</span><span class="sxs-lookup"><span data-stu-id="f3f72-107">Most of these, such as the new data types, are described in [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

<span data-ttu-id="f3f72-108">隨附于 Windows SDK 的64位工具組包含64位 MIDL 編譯器，Midl.exe，用於產生原生64位的存根以及32位的存根。</span><span class="sxs-lookup"><span data-stu-id="f3f72-108">The 64-bit toolkit that ships with the Windows SDK includes a 64-bit MIDL compiler, Midl.exe, for generating native 64-bit stubs, as well as 32-bit stubs.</span></span> <span data-ttu-id="f3f72-109">使用 **/env win64** 參數只產生64位的存根。</span><span class="sxs-lookup"><span data-stu-id="f3f72-109">Use the **/env win64** switch to generate 64-bit stubs only.</span></span> <span data-ttu-id="f3f72-110">預設值是產生兩個平臺上執行的雙重存根。</span><span class="sxs-lookup"><span data-stu-id="f3f72-110">The default is to generate dual stubs that run on both platforms.</span></span>

<span data-ttu-id="f3f72-111">請注意，64位 MIDL 只支援 [**/Oicf**](/windows/desktop/Midl/-oi) 和 [**/os**](/windows/desktop/Midl/-os) 優化模式。</span><span class="sxs-lookup"><span data-stu-id="f3f72-111">Note that the 64-bit MIDL supports the [**/Oicf**](/windows/desktop/Midl/-oi) and [**/Os**](/windows/desktop/Midl/-os) optimization modes only.</span></span>

 

 