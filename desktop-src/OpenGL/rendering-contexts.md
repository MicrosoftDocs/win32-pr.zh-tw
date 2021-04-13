---
title: 轉譯內容
description: OpenGL 轉譯內容是所有 OpenGL 命令通過的通訊埠。 進行 OpenGL 呼叫的每個執行緒都必須有目前的轉譯內容。 轉譯內容會將 OpenGL 連結至 Windows 視窗化系統。
ms.assetid: 9fbbb0be-2db4-4bfc-9a5c-a43d71554abc
keywords:
- Windows 上的 OpenGL，轉譯內容
- 轉譯內容 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac2ac6c5948da2b7372d600377666cd9e4e074
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301371"
---
# <a name="rendering-contexts"></a><span data-ttu-id="52dfe-107">轉譯內容</span><span class="sxs-lookup"><span data-stu-id="52dfe-107">Rendering Contexts</span></span>

<span data-ttu-id="52dfe-108">OpenGL 轉譯 *內容* 是所有 OpenGL 命令通過的通訊埠。</span><span class="sxs-lookup"><span data-stu-id="52dfe-108">An OpenGL *rendering context* is a port through which all OpenGL commands pass.</span></span> <span data-ttu-id="52dfe-109">進行 OpenGL 呼叫的每個執行緒都必須有目前的轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="52dfe-109">Every thread that makes OpenGL calls must have a current rendering context.</span></span> <span data-ttu-id="52dfe-110">轉譯內容會將 OpenGL 連結至 Windows 視窗化系統。</span><span class="sxs-lookup"><span data-stu-id="52dfe-110">Rendering contexts link OpenGL to the Windows windowing systems.</span></span>

<span data-ttu-id="52dfe-111">當應用程式建立轉譯內容時，會指定 Windows 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="52dfe-111">An application specifies a Windows device context when it creates a rendering context.</span></span> <span data-ttu-id="52dfe-112">此轉譯內容適用于在裝置上以指定的裝置內容參考的繪圖。</span><span class="sxs-lookup"><span data-stu-id="52dfe-112">This rendering context is suitable for drawing on the device that the specified device context references.</span></span> <span data-ttu-id="52dfe-113">尤其是，轉譯內容與裝置內容具有相同的像素格式。</span><span class="sxs-lookup"><span data-stu-id="52dfe-113">In particular, the rendering context has the same pixel format as the device context.</span></span> <span data-ttu-id="52dfe-114">如需詳細資訊，請參閱轉譯 [內容函數](rendering-context-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="52dfe-114">For more information, see [Rendering Context Functions](rendering-context-functions.md).</span></span>

<span data-ttu-id="52dfe-115">儘管此關聯性，轉譯內容與裝置內容不同。</span><span class="sxs-lookup"><span data-stu-id="52dfe-115">Despite this relationship, a rendering context is not the same as a device context.</span></span> <span data-ttu-id="52dfe-116">裝置內容包含 Windows 的圖形元件 (GDI) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="52dfe-116">A device context contains information pertinent to the graphics component (GDI) of Windows.</span></span> <span data-ttu-id="52dfe-117">轉譯內容包含與 OpenGL 相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="52dfe-117">A rendering context contains information pertinent to OpenGL.</span></span> <span data-ttu-id="52dfe-118">您必須在 GDI 呼叫中明確指定裝置內容。</span><span class="sxs-lookup"><span data-stu-id="52dfe-118">A device context must be explicitly specified in a GDI call.</span></span> <span data-ttu-id="52dfe-119">轉譯內容在 OpenGL 呼叫中是隱含的。</span><span class="sxs-lookup"><span data-stu-id="52dfe-119">A rendering context is implicit in an OpenGL call.</span></span> <span data-ttu-id="52dfe-120">您應該先設定裝置內容的像素格式，然後再建立轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="52dfe-120">You should set a device context's pixel format before creating a rendering context.</span></span>

<span data-ttu-id="52dfe-121">進行 OpenGL 呼叫的執行緒必須有目前的轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="52dfe-121">A thread that makes OpenGL calls must have a current rendering context.</span></span> <span data-ttu-id="52dfe-122">如果應用程式從缺少目前呈現內容的執行緒進行 OpenGL 呼叫，就不會發生任何事;呼叫沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="52dfe-122">If an application makes OpenGL calls from a thread that lacks a current rendering context, nothing happens; the call has no effect.</span></span> <span data-ttu-id="52dfe-123">應用程式通常會建立轉譯內容，並將它設定為執行緒的目前轉譯內容，然後呼叫 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="52dfe-123">An application commonly creates a rendering context, sets it as a thread's current rendering context, and then calls OpenGL functions.</span></span> <span data-ttu-id="52dfe-124">當它完成呼叫 OpenGL 函式時，應用程式會從執行緒 uncouples 轉譯內容，然後刪除轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="52dfe-124">When it finishes calling OpenGL functions, the application uncouples the rendering context from the thread, and then deletes the rendering context.</span></span> <span data-ttu-id="52dfe-125">一個視窗可以一次繪製多個轉譯內容，但一個執行緒只能有一個目前的使用中轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="52dfe-125">A window can have multiple rendering contexts drawing to it at one time, but a thread can have only one current, active rendering context.</span></span>

<span data-ttu-id="52dfe-126">目前的轉譯內容有相關聯的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="52dfe-126">A current rendering context has an associated device context.</span></span> <span data-ttu-id="52dfe-127">該裝置內容的裝置內容必須與建立轉譯內容時所使用的相同，但必須參考相同的裝置，且具有相同的像素格式。</span><span class="sxs-lookup"><span data-stu-id="52dfe-127">That device context need not be the same device context as that used when the rendering context was created, but it must reference the same device and have the same pixel format.</span></span>

<span data-ttu-id="52dfe-128">一個執行緒只能有一個目前的轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="52dfe-128">A thread can have only one current rendering context.</span></span> <span data-ttu-id="52dfe-129">轉譯內容可以只是一個執行緒的最新狀態。</span><span class="sxs-lookup"><span data-stu-id="52dfe-129">A rendering context can be current to only one thread.</span></span>

 

 




