---
description: Windows 映像取得 (WIA) 提供自動化物件，以用於指令碼語言，例如 Microsoft JScript 和 Microsoft Visual Basic Scripting Edition (VBScript) 開發軟體，以及高階程式設計語言，例如 Microsoft Visual Basic 開發系統。
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: WIA 腳本模型
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e70863e60e0d7aa6172bd9c93240f38cac27c6be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971006"
---
# <a name="wia-scripting-model"></a><span data-ttu-id="90784-103">WIA 腳本模型</span><span class="sxs-lookup"><span data-stu-id="90784-103">WIA Scripting Model</span></span>

<span data-ttu-id="90784-104">Windows 映像取得 (WIA) 提供自動化物件，以用於指令碼語言，例如 Microsoft JScript 和 Microsoft Visual Basic Scripting Edition (VBScript) 開發軟體，以及高階程式設計語言，例如 Microsoft Visual Basic 開發系統。</span><span class="sxs-lookup"><span data-stu-id="90784-104">Windows Image Acquisition (WIA) provides automation objects for use in scripting languages, such as Microsoft JScript and Microsoft Visual Basic Scripting Edition (VBScript) development software, and high-level programming languages such as Microsoft Visual Basic development system.</span></span>

> [!Note]  
> <span data-ttu-id="90784-105">此腳本系統已取代為 Windows 映像取得 (WIA) Automation 層。</span><span class="sxs-lookup"><span data-stu-id="90784-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="90784-106">請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。</span><span class="sxs-lookup"><span data-stu-id="90784-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="90784-107">下表說明 WIA 腳本物件和其使用方式。</span><span class="sxs-lookup"><span data-stu-id="90784-107">The following table describes WIA scripting objects and how they are used.</span></span> 

| <span data-ttu-id="90784-108">Object</span><span class="sxs-lookup"><span data-stu-id="90784-108">Object</span></span>                                | <span data-ttu-id="90784-109">描述</span><span class="sxs-lookup"><span data-stu-id="90784-109">Description</span></span>                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90784-110">**Wia**</span><span class="sxs-lookup"><span data-stu-id="90784-110">**Wia**</span></span>](-wia-wia.md)               | <span data-ttu-id="90784-111">最上層的 WIA 腳本物件。</span><span class="sxs-lookup"><span data-stu-id="90784-111">The top-level WIA scripting object.</span></span> <span data-ttu-id="90784-112">使用 [**Wia**](-wia-wia.md) 物件來列舉和連接至裝置，以及處理硬體裝置事件。</span><span class="sxs-lookup"><span data-stu-id="90784-112">Use the [**Wia**](-wia-wia.md) object to enumerate and connect to devices, and to handle hardware device events.</span></span>                                        |
| [<span data-ttu-id="90784-113">**DeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="90784-113">**DeviceInfo**</span></span>](-wia-deviceinfo.md) | <span data-ttu-id="90784-114">[**DeviceInfo**](-wia-deviceinfo.md)物件可讓您存取裝置屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="90784-114">The [**DeviceInfo**](-wia-deviceinfo.md) object provides access to information about device properties.</span></span>                                                                                     |
| [<span data-ttu-id="90784-115">**項目**</span><span class="sxs-lookup"><span data-stu-id="90784-115">**Item**</span></span>](-wia-item.md)             | <span data-ttu-id="90784-116">此物件代表 WIA 裝置、檔案和資料夾專案。</span><span class="sxs-lookup"><span data-stu-id="90784-116">This object represents WIA device, file, and folder items.</span></span> <span data-ttu-id="90784-117">WIA 硬體裝置及其影像或掃描張床會以 [**專案**](-wia-item.md) 物件的階層式樹狀結構來表示。</span><span class="sxs-lookup"><span data-stu-id="90784-117">A WIA hardware device and its images or scanning beds is represented as a hierarchical tree of [**Item**](-wia-item.md) objects.</span></span> |



 

<span data-ttu-id="90784-118">[**DeviceInfo**](-wia-deviceinfo.md)物件和 [**Item**](-wia-item.md)物件都與集合物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="90784-118">Both the [**DeviceInfo**](-wia-deviceinfo.md) object and the [**Item**](-wia-item.md) object are associated with collection objects.</span></span> <span data-ttu-id="90784-119">如需使用集合物件的詳細資訊，請參閱使用 WIA 集合物件。</span><span class="sxs-lookup"><span data-stu-id="90784-119">For information about using collection objects, see Using WIA Collection Objects.</span></span>

<span data-ttu-id="90784-120">下列主題涵蓋使用 WIA 腳本模型的一般資訊：</span><span class="sxs-lookup"><span data-stu-id="90784-120">The following topics cover general information about using the WIA scripting model:</span></span>

-   [<span data-ttu-id="90784-121">語法慣例</span><span class="sxs-lookup"><span data-stu-id="90784-121">Syntax Conventions</span></span>](-wia-syntax-conventions.md)
-   [<span data-ttu-id="90784-122">使用 WIA 集合物件</span><span class="sxs-lookup"><span data-stu-id="90784-122">Using WIA Collection Objects</span></span>](-wia-using-wia-collection-objects.md)
-   [<span data-ttu-id="90784-123">WIA 屬性常數定義</span><span class="sxs-lookup"><span data-stu-id="90784-123">WIA Property Constant Definitions</span></span>](-wia-wia-property-constant-definitions.md)

 

 
