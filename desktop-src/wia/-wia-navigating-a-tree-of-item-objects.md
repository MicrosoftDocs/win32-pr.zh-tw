---
description: 深入瞭解：導覽專案物件的樹狀結構
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: 流覽專案物件的樹狀結構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971011"
---
# <a name="navigating-a-tree-of-item-objects"></a><span data-ttu-id="c37a9-103">流覽專案物件的樹狀結構</span><span class="sxs-lookup"><span data-stu-id="c37a9-103">Navigating a Tree of Item Objects</span></span>

> [!Note]  
> <span data-ttu-id="c37a9-104">此腳本系統已取代為 Windows 映像取得 (WIA) Automation 層。</span><span class="sxs-lookup"><span data-stu-id="c37a9-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="c37a9-105">請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。</span><span class="sxs-lookup"><span data-stu-id="c37a9-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="c37a9-106">應用程式或腳本會流覽 Windows 映像取得 (WIA) 裝置的專案樹狀結構，以尋找並選取該裝置上的影像。</span><span class="sxs-lookup"><span data-stu-id="c37a9-106">An application or script navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="c37a9-107">應用程式會使用這項技術，在不使用對話方塊的情況下，選取並取得影像。</span><span class="sxs-lookup"><span data-stu-id="c37a9-107">Using this technique, an application selects and acquires an image without the use of a dialog box.</span></span>

<span data-ttu-id="c37a9-108">WIA 裝置會以 [**專案**](-wia-item.md) 物件樹狀結構中的根專案表示。</span><span class="sxs-lookup"><span data-stu-id="c37a9-108">A WIA device is represented as the root item in a tree of [**Item**](-wia-item.md) objects.</span></span> <span data-ttu-id="c37a9-109">樹狀結構中的子專案代表掃描器的資料夾和影像，或是掃描器的掃描張床。</span><span class="sxs-lookup"><span data-stu-id="c37a9-109">The child items in the tree represent folders and images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="c37a9-110">連線到裝置之後，請在樹狀結構的根項目 (呼叫代表裝置的 [**專案**](-wia-item.md)物件的 [**子**](-wia-iwiadispatchitem-children.md)屬性，) 取得子專案的集合 (影像或掃描裝置的張床) 。</span><span class="sxs-lookup"><span data-stu-id="c37a9-110">After connecting to a device, call the [**Children**](-wia-iwiadispatchitem-children.md) property of the [**Item**](-wia-item.md) object that represents the device (the root item of the tree) to obtain a collection of the child items (the images or scan beds) of the device.</span></span>

<span data-ttu-id="c37a9-111">如果需要) 流覽專案樹狀結構，請以遞迴方式列舉此集合 (。</span><span class="sxs-lookup"><span data-stu-id="c37a9-111">Enumerate this collection (recursively, if necessary) to navigate item tree.</span></span>

 

 
