---
description: 若要將專案新增至 [程式] 子功能表，請遵循下列步驟。
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: 如何在 [開始] 功能表中新增快捷方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115513"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a><span data-ttu-id="2917b-103">如何在 [開始] 功能表中新增快捷方式</span><span class="sxs-lookup"><span data-stu-id="2917b-103">How to Add Shortcuts to the Start Menu</span></span>

<span data-ttu-id="2917b-104">若要將專案新增至 [ **程式** ] 子功能表，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="2917b-104">To add an item to the **Programs** submenu, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="2917b-105">指示</span><span class="sxs-lookup"><span data-stu-id="2917b-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="2917b-106">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="2917b-106">Step 1:</span></span>

<span data-ttu-id="2917b-107">使用 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)介面建立 [shell 連結](./links.md)。</span><span class="sxs-lookup"><span data-stu-id="2917b-107">Create a [shell link](./links.md) by using the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="2917b-108">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="2917b-108">Step 2:</span></span>

<span data-ttu-id="2917b-109">使用 [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) 函式，傳遞 [**FOLDERID \_ 程式**](knownfolderid.md)來取得程式資料夾的位置。</span><span class="sxs-lookup"><span data-stu-id="2917b-109">Obtain the location of the Programs folder by using the [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function, passing [**FOLDERID\_Programs**](knownfolderid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="2917b-110">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="2917b-110">Step 3:</span></span>

<span data-ttu-id="2917b-111">將 Shell 連結新增至 [程式] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="2917b-111">Add the Shell link to the Programs folder.</span></span> <span data-ttu-id="2917b-112">您也可以在 [程式] 資料夾中建立資料夾，並將連結新增至該資料夾。</span><span class="sxs-lookup"><span data-stu-id="2917b-112">You can also create a folder in the Programs folder and add the link to that folder.</span></span>

 

 
