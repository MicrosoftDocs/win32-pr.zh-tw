---
title: 瞭解 Direct3D 12
description: 若要撰寫適用于 Windows 10 和 Windows 10 行動裝置版的3D 遊戲和應用程式，您必須瞭解 Direct3D 12 技術的基本概念，以及如何準備在您的遊戲和應用程式中使用它。
ms.assetid: DED7A434-FCD4-4F41-8B2C-E5AE6E48430F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1353c8c66fd401e364b9db302463f164f757c9ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548461"
---
# <a name="understanding-direct3d-12"></a><span data-ttu-id="7debf-103">瞭解 Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7debf-103">Understanding Direct3D 12</span></span>

<span data-ttu-id="7debf-104">若要撰寫適用于 Windows 10 和 Windows 10 行動裝置版的3D 遊戲和應用程式，您必須瞭解 Direct3D 12 技術的基本概念，以及如何準備在您的遊戲和應用程式中使用它。</span><span class="sxs-lookup"><span data-stu-id="7debf-104">To write 3D games and apps for Windows 10 and Windows 10 Mobile, you must understand the basics of the Direct3D 12 technology, and how to prepare to use it in your games and apps.</span></span>

<span data-ttu-id="7debf-105">使用本節中的主題來設定和瞭解您將使用 Direct3D 12 來設計應用程式和遊戲的環境。</span><span class="sxs-lookup"><span data-stu-id="7debf-105">Use the topics in this section to set up and learn about the environment in which you will program your apps and games with Direct3D 12.</span></span> <span data-ttu-id="7debf-106">此內容也可協助您將 Direct3D 11 應用程式和遊戲移植到 Direct3D 12，讓您可以利用 Direct3D 12 的功能和效率。</span><span class="sxs-lookup"><span data-stu-id="7debf-106">This content will also help you to port your Direct3D 11 apps and games to Direct3D 12, so you can take advantage of Direct3D 12 features and efficiencies.</span></span>

<span data-ttu-id="7debf-107">若要使用 Direct3D 12 進行程式設計，您需要下列元件：</span><span class="sxs-lookup"><span data-stu-id="7debf-107">To program with Direct3D 12, you need these components:</span></span>

-   <span data-ttu-id="7debf-108">具有 Direct3D 12 相容 GPU 的硬體平臺</span><span class="sxs-lookup"><span data-stu-id="7debf-108">A hardware platform with a Direct3D 12-compatible GPU</span></span>
-   <span data-ttu-id="7debf-109">顯示支援 Windows 顯示驅動程式模型的[驅動程式](/previous-versions//ff569172(v=vs.85)) (WDDM) 2。0</span><span class="sxs-lookup"><span data-stu-id="7debf-109">[Display drivers](/previous-versions//ff569172(v=vs.85)) that support the Windows Display Driver Model (WDDM) 2.0</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7debf-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="7debf-110">In this section</span></span>



| <span data-ttu-id="7debf-111">主題</span><span class="sxs-lookup"><span data-stu-id="7debf-111">Topic</span></span>                                                                                                               | <span data-ttu-id="7debf-112">描述</span><span class="sxs-lookup"><span data-stu-id="7debf-112">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7debf-113">Direct3D 12 程式設計環境設定</span><span class="sxs-lookup"><span data-stu-id="7debf-113">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)<br/>               | <span data-ttu-id="7debf-114">描述組成具生產力之 Direct3D 12 開發環境的安裝、工具和支援的程式庫。</span><span class="sxs-lookup"><span data-stu-id="7debf-114">Describes the installation, tools and supported libraries that make up a productive Direct3D 12 development environment.</span></span> <br/>                              |
| [<span data-ttu-id="7debf-115">建立基本的 Direct3D 12 元件</span><span class="sxs-lookup"><span data-stu-id="7debf-115">Creating a Basic Direct3D 12 Component</span></span>](creating-a-basic-direct3d-12-component.md)<br/>                     | <span data-ttu-id="7debf-116">本主題說明建立基本 Direct3D 12 元件的呼叫流程。</span><span class="sxs-lookup"><span data-stu-id="7debf-116">This topic describes the call flow to create a basic Direct3D 12 component.</span></span><br/>                                                                            |
| [<span data-ttu-id="7debf-117">從 Direct3D 11 到 Direct3D 12 的重要變更</span><span class="sxs-lookup"><span data-stu-id="7debf-117">Important Changes from Direct3D 11 to Direct3D 12</span></span>](important-changes-from-directx-11-to-directx-12.md)<br/> | <span data-ttu-id="7debf-118">Direct3D 12 代表來自 Direct3D 11 程式設計模型的重大起飛。</span><span class="sxs-lookup"><span data-stu-id="7debf-118">Direct3D 12 represents a significant departure from the Direct3D 11 programming model.</span></span> <span data-ttu-id="7debf-119">Direct3D 12 讓應用程式比以往更接近硬體。</span><span class="sxs-lookup"><span data-stu-id="7debf-119">Direct3D 12 lets apps get closer to hardware than ever before.</span></span> <br/> |
| [<span data-ttu-id="7debf-120">硬體功能等級</span><span class="sxs-lookup"><span data-stu-id="7debf-120">Hardware Feature Levels</span></span>](hardware-feature-levels.md)<br/>                                                   | <span data-ttu-id="7debf-121">描述 11 \_ 0 至 12 \_ 1 硬體功能層級的功能。</span><span class="sxs-lookup"><span data-stu-id="7debf-121">Describes the functionality of the 11\_0 through 12\_1 hardware feature levels.</span></span><br/>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="7debf-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="7debf-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7debf-123">Direct3D 12 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="7debf-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

