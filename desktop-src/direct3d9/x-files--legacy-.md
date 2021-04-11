---
description: X 檔案格式參考副檔名為 X 的檔案。
ms.assetid: 06b3dcb3-03fc-4d99-b8c3-32f56d8bf49e
title: 'X 檔案 (舊版)  (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0e4ce85a0ff5ecbc2f680f55b8162d13bc1042
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845951"
---
# <a name="x-files-legacy-direct3d-9"></a><span data-ttu-id="1393a-103">X 檔案 (舊版)  (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1393a-103">X Files (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="1393a-104">X 檔案格式參考副檔名為 X 的檔案。</span><span class="sxs-lookup"><span data-stu-id="1393a-104">The X file format refers to files with the .x file name extension.</span></span> <span data-ttu-id="1393a-105">X 檔案是透過 DirectX 2.0 引進。</span><span class="sxs-lookup"><span data-stu-id="1393a-105">X files were introduced with DirectX 2.0.</span></span> <span data-ttu-id="1393a-106">此格式的二進位版本後續是與 DirectX 3.0 一起發行，本檔也有相關說明。</span><span class="sxs-lookup"><span data-stu-id="1393a-106">A binary version of this format was subsequently released with DirectX 3.0, which is also described in this documentation.</span></span> <span data-ttu-id="1393a-107">DirectX 6.0 引進了介面和方法，可讓您讀取和寫入. x 檔案。</span><span class="sxs-lookup"><span data-stu-id="1393a-107">DirectX 6.0 introduced interfaces and methods that enable reading from and writing to .x files.</span></span>

<span data-ttu-id="1393a-108">X 檔案提供範本驅動的格式，可讓您儲存網格、紋理、動畫和使用者可定義的物件。</span><span class="sxs-lookup"><span data-stu-id="1393a-108">X files provide a template-driven format that enables the storage of meshes, textures, animations, and user-definable objects.</span></span> <span data-ttu-id="1393a-109">動畫集合的支援可讓您儲存預先定義的路徑以供即時播放。</span><span class="sxs-lookup"><span data-stu-id="1393a-109">Support for animation sets enables you to store predefined paths for playback in real time.</span></span> <span data-ttu-id="1393a-110">也支援實例和階層。</span><span class="sxs-lookup"><span data-stu-id="1393a-110">Instancing and hierarchies are also supported.</span></span> <span data-ttu-id="1393a-111">實例可啟用多個物件的參考，例如網格，而且每個檔案只會儲存一次其資料。</span><span class="sxs-lookup"><span data-stu-id="1393a-111">Instancing enables multiple references to an object, such as a mesh, while storing its data only once per file.</span></span> <span data-ttu-id="1393a-112">階層可用來表示資料記錄之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="1393a-112">Hierarchies are used to express relationships between data records.</span></span>

<span data-ttu-id="1393a-113">. X 檔案格式提供低層級的資料基本資料，讓應用程式透過範本來定義較高層級的基本專案。</span><span class="sxs-lookup"><span data-stu-id="1393a-113">The .x file format provides low-level data primitives on which applications define higher-level primitives through templates.</span></span>

<span data-ttu-id="1393a-114">以謹慎的 3ds max 或 Alias \| Wavefront 的 Maya 應用程式建立的立體模型，可以轉換成具有適用于別名 Maya 之 DirectX 延伸模組的. x 檔案。</span><span class="sxs-lookup"><span data-stu-id="1393a-114">Three-dimensional models created in Discreet's 3ds max or Alias\|Wavefront's Maya applications can be converted to .x files with the DirectX Extensions for Alias Maya.</span></span>

<span data-ttu-id="1393a-115">本節說明. x 檔案的結構，以及如何在您的應用程式中使用它們。</span><span class="sxs-lookup"><span data-stu-id="1393a-115">This section describes the structure of .x files and how to use them in your applications.</span></span> <span data-ttu-id="1393a-116">資訊分成下列主題。</span><span class="sxs-lookup"><span data-stu-id="1393a-116">Information is divided into the following topics.</span></span>

-   [<span data-ttu-id="1393a-117">載入 X 檔案 (舊版)  (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1393a-117">Loading an X File (Legacy) (Direct3D 9)</span></span>](loading-an-x-file--legacy-.md)
-   [<span data-ttu-id="1393a-118">儲存至 X 檔案 (舊版)  (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1393a-118">Saving to an X File (Legacy) (Direct3D 9)</span></span>](saving-to-an-x-file--legacy-.md)
-   [<span data-ttu-id="1393a-119">定義簡單的 Cube (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1393a-119">Defining a Simple Cube (Direct3D 9)</span></span>](defining-a-simple-cube.md)
-   [<span data-ttu-id="1393a-120">將材質新增 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="1393a-120">Adding Textures (Direct3D 9)</span></span>](adding-textures.md)
-   [<span data-ttu-id="1393a-121"> (Direct3D 9) 加入框架和動畫 </span><span class="sxs-lookup"><span data-stu-id="1393a-121">Adding Frames and Animations (Direct3D 9)</span></span>](adding-frames-and-animations.md)

<span data-ttu-id="1393a-122">如需有關. x 檔案格式的詳細資訊，請參閱 [x 檔案參考](dx9-graphics-reference-d3dx-x-file.md)。</span><span class="sxs-lookup"><span data-stu-id="1393a-122">For more information about the .x file format, see [X File Reference](dx9-graphics-reference-d3dx-x-file.md).</span></span>

<span data-ttu-id="1393a-123">如需有關. x 檔案 API 的詳細資訊，請參閱 [ (舊版) 的 x 檔案參考 ](dx9-graphics-reference-x-file.md)。</span><span class="sxs-lookup"><span data-stu-id="1393a-123">For more information about the .x file API, see [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1393a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="1393a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1393a-125">快速入門</span><span class="sxs-lookup"><span data-stu-id="1393a-125">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



