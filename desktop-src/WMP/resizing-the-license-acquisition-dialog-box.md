---
title: 調整授權取得對話方塊的大小
description: 調整授權取得對話方塊的大小
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Windows Media Player，重設授權取得的大小對話方塊
- Windows Media Player，授權取得對話方塊
- Windows Media Player，DRM_LicenseAcqURL 屬性
- 調整授權取得大小對話方塊
- 取得授權對話方塊
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372390"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a><span data-ttu-id="93a4f-109">調整授權取得對話方塊的大小</span><span class="sxs-lookup"><span data-stu-id="93a4f-109">Resizing the License Acquisition Dialog Box</span></span>

<span data-ttu-id="93a4f-110">您可以將查詢字串參數附加至您為 **DRM \_ LicenseAcqURL** 屬性提供的 URL，以指定 Windows Media Player 10 或更新版本的授權取得對話方塊的大小。</span><span class="sxs-lookup"><span data-stu-id="93a4f-110">You can append query string parameters to the URL you provide for the **DRM\_LicenseAcqURL** attribute to specify a size for the Windows Media Player 10 or later license acquisition dialog box.</span></span> <span data-ttu-id="93a4f-111">下表列出參數。</span><span class="sxs-lookup"><span data-stu-id="93a4f-111">The following table lists the parameters.</span></span>



| <span data-ttu-id="93a4f-112">參數</span><span class="sxs-lookup"><span data-stu-id="93a4f-112">Parameter</span></span> | <span data-ttu-id="93a4f-113">Description</span><span class="sxs-lookup"><span data-stu-id="93a4f-113">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="93a4f-114">*DlgX*</span><span class="sxs-lookup"><span data-stu-id="93a4f-114">*DlgX*</span></span>    | <span data-ttu-id="93a4f-115">指定對話方塊的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="93a4f-115">Specifies the width of the dialog box, in pixels.</span></span>  |
| <span data-ttu-id="93a4f-116">*DlgY*</span><span class="sxs-lookup"><span data-stu-id="93a4f-116">*DlgY*</span></span>    | <span data-ttu-id="93a4f-117">指定對話方塊的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="93a4f-117">Specifies the height of the dialog box, in pixels.</span></span> |



 

<span data-ttu-id="93a4f-118">例如，下列授權取得 URL 會導致 [授權取得] 對話方塊開啟，大小為800乘以600圖元：</span><span class="sxs-lookup"><span data-stu-id="93a4f-118">For example, the following license acquisition URL would cause the license acquisition dialog box to open with a size of 800 by 600 pixels:</span></span>


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



<span data-ttu-id="93a4f-119">對話方塊的大小上限絕不會超過目前的螢幕尺寸減去20圖元。</span><span class="sxs-lookup"><span data-stu-id="93a4f-119">The maximum size for the dialog box will never exceed the current screen dimensions minus 20 pixels.</span></span> <span data-ttu-id="93a4f-120">大小下限為 333 x 210 圖元 (預設大小) 。</span><span class="sxs-lookup"><span data-stu-id="93a4f-120">The minimum size is 333 x 210 pixels (the default size).</span></span>

<span data-ttu-id="93a4f-121">這項功能需要 Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="93a4f-121">This feature requires Windows Media Player 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93a4f-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="93a4f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93a4f-123">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="93a4f-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




