---
title: 無視窗控制項
description: 無視窗控制項
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372658"
---
# <a name="windowless-controls"></a><span data-ttu-id="f43c3-103">無視窗控制項</span><span class="sxs-lookup"><span data-stu-id="f43c3-103">Windowless Controls</span></span>

<span data-ttu-id="f43c3-104">ActiveX 控制項96規格包含無視窗控制項的定義。</span><span class="sxs-lookup"><span data-stu-id="f43c3-104">The ActiveX Controls 96 specification includes a definition for windowless controls.</span></span> <span data-ttu-id="f43c3-105">這類控制項無法在自己的視窗中操作，而且需要容器以提供控制項可能繪製的共用視窗，請參閱 ActiveX SDK。</span><span class="sxs-lookup"><span data-stu-id="f43c3-105">Such controls do not operate in their own window and require a container to offer a shared window into which the control may draw, see the ActiveX SDK.</span></span> <span data-ttu-id="f43c3-106">無視窗控制項的設計是為了與舊版的控制項容器相容，方法是在這種情況下建立自己的視窗，無視窗控制項容器應以傳統方式裝載視窗控制項，而不會有任何問題。</span><span class="sxs-lookup"><span data-stu-id="f43c3-106">Windowless controls are designed to be compatible with older control containers by creating their own window in that situation, windowless control containers should host windowed controls in the traditional way with no problem.</span></span> <span data-ttu-id="f43c3-107">不過，容器可以用來區別可在無視窗模式下運作的控制項，因此定義適當的元件類別目錄，可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="f43c3-107">It may however be useful for a container to distinguish those controls that can operate in a windowless mode, so an appropriate component category is defined.</span></span>

<span data-ttu-id="f43c3-108">CATID-{1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID \_ WindowlessObject</span><span class="sxs-lookup"><span data-stu-id="f43c3-108">CATID - {1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID\_WindowlessObject</span></span>

## <a name="related-topics"></a><span data-ttu-id="f43c3-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="f43c3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f43c3-110">元件類別</span><span class="sxs-lookup"><span data-stu-id="f43c3-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




