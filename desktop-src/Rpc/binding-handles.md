---
title: 系結控制碼
description: 系結是在用戶端程式和伺服器程式之間建立邏輯連接的程式。 在用戶端與伺服器之間撰寫系結的資訊是由稱為系結控制碼的結構所表示。
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07973deb8319b44a82795a6402ef5e1a9310c2c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507955"
---
# <a name="binding-handles"></a><span data-ttu-id="21e4e-104">系結控制碼</span><span class="sxs-lookup"><span data-stu-id="21e4e-104">Binding Handles</span></span>

<span data-ttu-id="21e4e-105">系結是在用戶端程式和伺服器程式之間建立邏輯連接的程式。</span><span class="sxs-lookup"><span data-stu-id="21e4e-105">Binding is the process of creating a logical connection between a client program and a server program.</span></span> <span data-ttu-id="21e4e-106">在用戶端與伺服器之間撰寫系結的資訊是由稱為系結控制碼的結構所表示。</span><span class="sxs-lookup"><span data-stu-id="21e4e-106">The information that composes the binding between client and server is represented by a structure called a binding handle.</span></span>

<span data-ttu-id="21e4e-107">系結控制碼類似于 fopen C 執行時間程式庫函式傳回的檔案控制代碼，或是函式 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 傳回的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="21e4e-107">A binding handle is analogous to a file handle that the fopen C run-time library function returns, or a window handle that the function [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) returns.</span></span>

<span data-ttu-id="21e4e-108">如同這些控制碼，您的應用程式無法直接存取及操作系結控制碼中的資訊。</span><span class="sxs-lookup"><span data-stu-id="21e4e-108">As with these handles, your application cannot directly access and manipulate the information in the binding handle.</span></span> <span data-ttu-id="21e4e-109">系結控制碼資料結構中的資訊僅適用于 RPC 執行時間程式庫。</span><span class="sxs-lookup"><span data-stu-id="21e4e-109">The information in a binding handle data structure is available only to the RPC run-time libraries.</span></span> <span data-ttu-id="21e4e-110">您可以提供控制碼、執行時間程式庫存取和操作適當的資料。</span><span class="sxs-lookup"><span data-stu-id="21e4e-110">You provide the handle, the run-time libraries access and manipulate the appropriate data.</span></span>

<span data-ttu-id="21e4e-111">本節提供下列主題中系結控制碼的討論：</span><span class="sxs-lookup"><span data-stu-id="21e4e-111">This section presents a discussion on binding handles in the following topics:</span></span>

-   [<span data-ttu-id="21e4e-112">系結控制碼的類型</span><span class="sxs-lookup"><span data-stu-id="21e4e-112">Types of Binding Handles</span></span>](types-of-binding-handles.md)
-   [<span data-ttu-id="21e4e-113">用戶端系結</span><span class="sxs-lookup"><span data-stu-id="21e4e-113">Client-Side Binding</span></span>](client-side-binding.md)
-   [<span data-ttu-id="21e4e-114">伺服器端系結</span><span class="sxs-lookup"><span data-stu-id="21e4e-114">Server-Side Binding</span></span>](server-side-binding.md)
-   [<span data-ttu-id="21e4e-115">完整且部分系結的控制碼</span><span class="sxs-lookup"><span data-stu-id="21e4e-115">Fully and Partially Bound Handles</span></span>](fully-and-partially-bound-handles.md)
-   [<span data-ttu-id="21e4e-116">解讀系結資訊</span><span class="sxs-lookup"><span data-stu-id="21e4e-116">Interpreting Binding Information</span></span>](interpreting-binding-information.md)
-   [<span data-ttu-id="21e4e-117">Microsoft RPC Binding-Handle 擴充功能</span><span class="sxs-lookup"><span data-stu-id="21e4e-117">Microsoft RPC Binding-Handle Extensions</span></span>](microsoft-rpc-binding-handle-extensions.md)
-   [<span data-ttu-id="21e4e-118">Binding 處理函式</span><span class="sxs-lookup"><span data-stu-id="21e4e-118">Binding-Handle Functions</span></span>](binding-handle-functions.md)
-   [<span data-ttu-id="21e4e-119">RPC 名稱服務資料庫</span><span class="sxs-lookup"><span data-stu-id="21e4e-119">The RPC Name Service Database</span></span>](the-rpc-name-service-database.md)

 

 