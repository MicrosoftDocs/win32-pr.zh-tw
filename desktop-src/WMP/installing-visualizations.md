---
title: 安裝視覺效果
description: 安裝視覺效果
ms.assetid: ca391e38-def5-47da-81f7-94aa96530387
keywords:
- Windows Media Player 外掛程式、視覺效果
- 外掛程式，視覺效果
- 視覺效果，安裝
- 自訂視覺效果，安裝
- 安裝視覺效果
- 視覺效果，註冊
- 自訂視覺效果，註冊
- 登錄，視覺效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1dc8f33d7b5f5b938bee6c89d946955509ab34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965376"
---
# <a name="installing-visualizations"></a><span data-ttu-id="03569-111">安裝視覺效果</span><span class="sxs-lookup"><span data-stu-id="03569-111">Installing Visualizations</span></span>

<span data-ttu-id="03569-112">您必須為視覺效果的使用者提供安裝程式。</span><span class="sxs-lookup"><span data-stu-id="03569-112">You must provide an installation process for the user of your visualization.</span></span> <span data-ttu-id="03569-113">您也必須為使用者提供卸載進程。</span><span class="sxs-lookup"><span data-stu-id="03569-113">You must also provide an uninstall process for the user.</span></span> <span data-ttu-id="03569-114">目前版本的 Windows Media Player 不會從使用者介面安裝視覺效果。</span><span class="sxs-lookup"><span data-stu-id="03569-114">The current version of Windows Media Player does not install visualizations from the user interface.</span></span>

## <a name="installing-to-the-visualization-folder"></a><span data-ttu-id="03569-115">安裝至視覺效果資料夾</span><span class="sxs-lookup"><span data-stu-id="03569-115">Installing to the Visualization Folder</span></span>

<span data-ttu-id="03569-116">建議您在安裝 Windows Media Player 的資料夾的 [視覺效果] 子資料夾中安裝所有視覺效果。</span><span class="sxs-lookup"><span data-stu-id="03569-116">It is recommended that you install all visualizations in the Visualizations subfolder of the folder where Windows Media Player is installed.</span></span>

## <a name="registering-your-visualization"></a><span data-ttu-id="03569-117">註冊您的視覺效果</span><span class="sxs-lookup"><span data-stu-id="03569-117">Registering Your Visualization</span></span>

<span data-ttu-id="03569-118">視覺效果是 COM Dll，並遵循所有安裝和移除的一般規則。</span><span class="sxs-lookup"><span data-stu-id="03569-118">Visualizations are COM DLLs and follow all the normal rules of installation and removal.</span></span> <span data-ttu-id="03569-119">您可以使用 regsvr32.exe 或其他安裝工具來註冊您的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="03569-119">You can use regsvr32.exe or other installation tools to register your visualization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03569-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="03569-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03569-121">**關於自訂視覺效果**</span><span class="sxs-lookup"><span data-stu-id="03569-121">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




