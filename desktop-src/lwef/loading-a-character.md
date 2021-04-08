---
title: 載入字元
description: 載入字元
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673119"
---
# <a name="loading-a-character"></a><span data-ttu-id="e557c-103">載入字元</span><span class="sxs-lookup"><span data-stu-id="e557c-103">Loading a Character</span></span>

<span data-ttu-id="e557c-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e557c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e557c-105">若要建立字元的動畫，您必須先載入該字元。</span><span class="sxs-lookup"><span data-stu-id="e557c-105">To animate a character, you must first load the character.</span></span> <span data-ttu-id="e557c-106">使用 [**load**](load-method.md) 方法載入字元的資料。</span><span class="sxs-lookup"><span data-stu-id="e557c-106">Use the [**Load**](load-method.md) method to load the character's data.</span></span> <span data-ttu-id="e557c-107">Microsoft Agent 支援兩種格式的字元和動畫資料：單一結構化檔案和不同的檔案。</span><span class="sxs-lookup"><span data-stu-id="e557c-107">Microsoft Agent supports two formats for character and animation data: a single structured file and separate files.</span></span> <span data-ttu-id="e557c-108">一般而言，您會使用單一檔案格式 (。當資料儲存在本機時，ACS) 。</span><span class="sxs-lookup"><span data-stu-id="e557c-108">Typically, you use the single file format (.ACS) when the data is stored locally.</span></span> <span data-ttu-id="e557c-109"> ( 的多個檔案格式。Acf。當您想要個別下載動畫時（例如從 HTTP 伺服器存取動畫時），ACA) 的效果最佳。</span><span class="sxs-lookup"><span data-stu-id="e557c-109">The multiple file format (.ACF, .ACA) works best when you want to download animations individually, such as when accessing animations from an HTTP server.</span></span>

<span data-ttu-id="e557c-110">用戶端應用程式只能載入相同字元的單一實例。</span><span class="sxs-lookup"><span data-stu-id="e557c-110">A client application can load only a single instance of the same character.</span></span> <span data-ttu-id="e557c-111">嘗試多次載入相同字元將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e557c-111">Any attempt to load the same character more than once will fail.</span></span> <span data-ttu-id="e557c-112">不過，應用程式可以透過提供與 Microsoft Agent 的個別連接，來載入相同字元的多個實例。</span><span class="sxs-lookup"><span data-stu-id="e557c-112">However, an application can have multiple instances of the same character loaded by providing separate connections to Microsoft Agent.</span></span> <span data-ttu-id="e557c-113">例如，應用程式可以從 Microsoft Agent 控制項的兩個複本載入相同的字元。</span><span class="sxs-lookup"><span data-stu-id="e557c-113">For example, an application could load the same character from two copies of the Microsoft Agent control.</span></span>

<span data-ttu-id="e557c-114">您也可以定義您自己的字元以搭配 Microsoft Agent 使用。</span><span class="sxs-lookup"><span data-stu-id="e557c-114">You can also define your own characters for use with Microsoft Agent.</span></span> <span data-ttu-id="e557c-115">您可以使用任何偏好的轉譯工具來建立影像，但最後您會得到 Windows 點陣圖格式檔案。</span><span class="sxs-lookup"><span data-stu-id="e557c-115">You may use any rendering tool you prefer to create the images, provided that you end up with Windows bitmap format files.</span></span> <span data-ttu-id="e557c-116">若要組合字元的影像並將其編譯成可搭配 Microsoft Agent 使用的動畫，請使用 Microsoft Agent 字元編輯器。</span><span class="sxs-lookup"><span data-stu-id="e557c-116">To assemble and compile a character's images into animations for use with Microsoft Agent, use the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="e557c-117">此工具可讓您定義字元的預設屬性，以及定義字元的動畫。</span><span class="sxs-lookup"><span data-stu-id="e557c-117">This tool enables you to define a character's default properties as well as define animations for the character.</span></span> <span data-ttu-id="e557c-118">當您建立字元時，Microsoft 代理程式字元編輯器也可讓您選取適當的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="e557c-118">The Microsoft Agent Character Editor also enables you to select the appropriate file format when you create a character.</span></span>

 

 




