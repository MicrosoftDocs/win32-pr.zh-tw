---
description: 本節列出在 Direct3D 應用程式中使用裝置視窗時，可能會遇到的問題。
ms.assetid: 7cfd2ad6-fb85-4303-9fa4-6fe7d16d9951
title: '使用裝置 Windows (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56352ef0ec66def620a0ae0995d92d8b421722e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106986224"
---
# <a name="working-with-device-windows-direct3d-9"></a><span data-ttu-id="b3b38-103">使用裝置 Windows (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="b3b38-103">Working with Device Windows (Direct3D 9)</span></span>

<span data-ttu-id="b3b38-104">本節列出在 Direct3D 應用程式中使用裝置視窗時，可能會遇到的問題。</span><span class="sxs-lookup"><span data-stu-id="b3b38-104">This section lists an issue that you might encounter when working with device windows in Direct3D applications.</span></span>

-   <span data-ttu-id="b3b38-105">Direct3D 只會使用 Direct3D 訊息處理函式來連結焦點視窗，而不是裝置視窗，而且只會處理焦點視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="b3b38-105">Direct3D only hooks up the focus windows instead of the device window with the Direct3D message processing function, and only processes the focus window messages.</span></span> <span data-ttu-id="b3b38-106">因此，焦點視窗應該是任何裝置視窗的父系。</span><span class="sxs-lookup"><span data-stu-id="b3b38-106">So, the focus window should be the parent of any device window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3b38-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3b38-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3b38-108">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="b3b38-108">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



