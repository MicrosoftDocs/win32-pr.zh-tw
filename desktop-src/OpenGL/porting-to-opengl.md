---
title: 移植至 OpenGL
description: 移植至 OpenGL
ms.assetid: 6799e10b-2f7c-4516-92ea-43667784f8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8efd2a34ac5d7fb6fc52aef3f24a556712b2c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372358"
---
# <a name="porting-to-opengl"></a><span data-ttu-id="cd00b-103">移植至 OpenGL</span><span class="sxs-lookup"><span data-stu-id="cd00b-103">Porting to OpenGL</span></span>

<span data-ttu-id="cd00b-104">OpenGL 是針對硬體和作業系統之間的相容性而設計的。</span><span class="sxs-lookup"><span data-stu-id="cd00b-104">OpenGL is designed for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="cd00b-105">這項設計可讓程式設計人員更輕鬆地將 OpenGL 程式從某個系統移植到另一個系統。</span><span class="sxs-lookup"><span data-stu-id="cd00b-105">This design makes it easier for programmers to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="cd00b-106">雖然每個作業系統都有獨特的需求，但您目前程式中的大部分 OpenGL 程式碼都可以依原樣使用。</span><span class="sxs-lookup"><span data-stu-id="cd00b-106">While each operating system has unique requirements, much of the OpenGL code in your current programs can be used as is.</span></span> <span data-ttu-id="cd00b-107">若要將您的 OpenGL 應用程式移植到 Microsoft Windows，您必須修改您的程式，以使用 Windows 視窗化系統。</span><span class="sxs-lookup"><span data-stu-id="cd00b-107">To port your OpenGL application to Microsoft Windows, you'll have to modify your programs to work with the Windows windowing systems.</span></span>

<span data-ttu-id="cd00b-108">在一般情況中，應用程式會從兩個平臺的其中一個移植至適用于 Windows 的 OpenGL：</span><span class="sxs-lookup"><span data-stu-id="cd00b-108">In general applications are ported to OpenGL for Windows from one of two platforms:</span></span>

-   <span data-ttu-id="cd00b-109">為 X 視窗系統開發的 OpenGL 應用程式，以及 X 程式庫 (Xlib) </span><span class="sxs-lookup"><span data-stu-id="cd00b-109">OpenGL applications developed for the X Window System and the X library (Xlib)</span></span>
-   <span data-ttu-id="cd00b-110">鳶尾花 GL 應用程式</span><span class="sxs-lookup"><span data-stu-id="cd00b-110">IRIS GL applications</span></span>

<span data-ttu-id="cd00b-111">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="cd00b-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="cd00b-112">移植至適用于 Windows 的 OpenGL 的簡介</span><span class="sxs-lookup"><span data-stu-id="cd00b-112">Introduction to Porting to OpenGL for Windows</span></span>](introduction-to-porting-to-opengl-for-windows-nt--windows-2000--and-windows-95-98.md)
-   [<span data-ttu-id="cd00b-113">OpenGL 函數及其鳶尾花 GL 對等專案</span><span class="sxs-lookup"><span data-stu-id="cd00b-113">OpenGL Functions and Their IRIS GL Equivalents</span></span>](opengl-functions-and-their-iris-gl-equivalents.md)
-   [<span data-ttu-id="cd00b-114">鳶尾花 GL 和 OpenGL 差異</span><span class="sxs-lookup"><span data-stu-id="cd00b-114">IRIS GL and OpenGL Differences</span></span>](iris-gl-and-opengl-differences.md)

 

 




