---
title: OpenGL 圖形控制項
description: OpenGL 圖形控制項
ms.assetid: 327f2920-1bc9-4de7-aa12-3e9f74a94759
keywords:
- OpenGL、圖形控制項
- 圖形控制項 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6bb138a2d8c597fae2d92a1d1394c8ff05b03cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673267"
---
# <a name="opengl-graphic-control"></a><span data-ttu-id="b5135-105">OpenGL 圖形控制項</span><span class="sxs-lookup"><span data-stu-id="b5135-105">OpenGL Graphic Control</span></span>

<span data-ttu-id="b5135-106">OpenGL 提供您相當直接的控制權來控制兩層和三維圖形的基本作業。</span><span class="sxs-lookup"><span data-stu-id="b5135-106">OpenGL provides you with fairly direct control over the fundamental operations of two- and three-dimensional graphics.</span></span> <span data-ttu-id="b5135-107">這包括將這類參數指定為轉換矩陣、光源方程式係數、消除鋸齒方法和圖元更新運算子。</span><span class="sxs-lookup"><span data-stu-id="b5135-107">This includes specification of such parameters as transformation matrices, lighting equation coefficients, antialiasing methods, and pixel-update operators.</span></span> <span data-ttu-id="b5135-108">但是，它並不提供描述或建立複雜幾何物件模型的方法。</span><span class="sxs-lookup"><span data-stu-id="b5135-108">However, it doesn't provide you with a means for describing or modeling complex geometric objects.</span></span> <span data-ttu-id="b5135-109">因此，您發出的 OpenGL 命令會指定應該如何產生特定的結果 (應遵循的程式) 而不是該結果應該看起來的樣子。</span><span class="sxs-lookup"><span data-stu-id="b5135-109">Thus, the OpenGL commands you issue specify how a certain result should be produced (what procedure should be followed) rather than what exactly that result should look like.</span></span> <span data-ttu-id="b5135-110">也就是說，OpenGL 的程式基本上是程式性，而不是描述性的。</span><span class="sxs-lookup"><span data-stu-id="b5135-110">That is, OpenGL is fundamentally procedural rather than descriptive.</span></span> <span data-ttu-id="b5135-111">若要完全瞭解如何使用 OpenGL，它有助於知道其運作方式的順序。</span><span class="sxs-lookup"><span data-stu-id="b5135-111">To fully understand how to use OpenGL, it helps to know the order in which it carries out its operations.</span></span>

 

 




