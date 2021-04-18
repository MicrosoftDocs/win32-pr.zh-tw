---
description: 寫入捕獲篩選器
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: 寫入捕獲篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989458"
---
# <a name="writing-capture-filters"></a><span data-ttu-id="b6580-103">寫入捕獲篩選器</span><span class="sxs-lookup"><span data-stu-id="b6580-103">Writing Capture Filters</span></span>

<span data-ttu-id="b6580-104">不建議為 DirectShow 撰寫音訊或影片捕獲篩選。</span><span class="sxs-lookup"><span data-stu-id="b6580-104">Writing an audio or video capture filter for DirectShow is not recommended.</span></span> <span data-ttu-id="b6580-105">相反地，DirectShow 會使用包裝函式篩選和 [系統裝置列舉](system-device-enumerator.md)值，為音訊和影片捕獲裝置提供自動支援。</span><span class="sxs-lookup"><span data-stu-id="b6580-105">Instead, DirectShow provides automatic support for audio and video capture devices, using wrapper filters and the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="b6580-106">如需有關如何執行設備磁碟機的詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 檔。</span><span class="sxs-lookup"><span data-stu-id="b6580-106">For more information about implementing a device driver, refer to the Windows Driver Kit (WDK) documentation.</span></span>

<span data-ttu-id="b6580-107">這一節僅適用于需要從不尋常的硬體裝置捕獲某種自訂資料的開發人員。</span><span class="sxs-lookup"><span data-stu-id="b6580-107">This section is intended only for developers who need to capture some kind of custom data from an unusual hardware device.</span></span>

<span data-ttu-id="b6580-108">本文包含下列各節：</span><span class="sxs-lookup"><span data-stu-id="b6580-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="b6580-109">捕獲篩選準則的 Pin 需求</span><span class="sxs-lookup"><span data-stu-id="b6580-109">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
-   [<span data-ttu-id="b6580-110"> (選用) 來執行預覽 Pin </span><span class="sxs-lookup"><span data-stu-id="b6580-110">Implementing a Preview Pin (Optional)</span></span>](implementing-a-preview-pin--optional.md)
-   [<span data-ttu-id="b6580-111">在 Capture 篩選器中產生資料</span><span class="sxs-lookup"><span data-stu-id="b6580-111">Producing Data in a Capture Filter</span></span>](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a><span data-ttu-id="b6580-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="b6580-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6580-113">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="b6580-113">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



