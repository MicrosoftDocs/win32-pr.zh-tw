---
title: AmbientAttributes 底部
description: 底部屬性會指定或抓取控制項的底部座標。
ms.assetid: a07af5b0-154d-4c3f-be8b-39aeb52a6f1e
keywords:
- AmbientAttributes Windows Media Player 底部
topic_type:
- apiref
api_name:
- AmbientAttributes.bottom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed707dbd821119963a46c5ac9a8301c20f4d39e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993602"
---
# <a name="ambientattributesbottom"></a><span data-ttu-id="625e3-104">AmbientAttributes 底部</span><span class="sxs-lookup"><span data-stu-id="625e3-104">AmbientAttributes.bottom</span></span>

<span data-ttu-id="625e3-105">**底部** 屬性會指定或抓取控制項的底部座標。</span><span class="sxs-lookup"><span data-stu-id="625e3-105">The **bottom** attribute specifies or retrieves the bottom coordinate of the control.</span></span>

``` syntax
        elementID.bottom
```

## <a name="possible-values"></a><span data-ttu-id="625e3-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="625e3-106">Possible Values</span></span>

<span data-ttu-id="625e3-107">此屬性是讀取/寫入 **號碼** (**long**) 代表從控制項到父 **視圖\*\*\*\*或子視圖下** 邊緣的距離（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="625e3-107">This attribute is a read/write **Number** (**long**) representing the distance in pixels from the control to the bottom edge of the parent **VIEW** or **SUBVIEW**.</span></span> <span data-ttu-id="625e3-108">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="625e3-108">It has a default value of zero.</span></span> <span data-ttu-id="625e3-109">負數值的行為，或未指定 [AmbientAttributes](ambientattributes-height.md) 時，是未定義的。</span><span class="sxs-lookup"><span data-stu-id="625e3-109">The behavior for negative values, or when [AmbientAttributes.height](ambientattributes-height.md) is not specified, is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="625e3-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="625e3-110">Requirements</span></span>



| <span data-ttu-id="625e3-111">需求</span><span class="sxs-lookup"><span data-stu-id="625e3-111">Requirement</span></span> | <span data-ttu-id="625e3-112">值</span><span class="sxs-lookup"><span data-stu-id="625e3-112">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="625e3-113">版本</span><span class="sxs-lookup"><span data-stu-id="625e3-113">Version</span></span><br/> | <span data-ttu-id="625e3-114">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="625e3-114">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="625e3-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="625e3-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="625e3-116">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="625e3-116">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="625e3-117">**AmbientAttributes.id**</span><span class="sxs-lookup"><span data-stu-id="625e3-117">**AmbientAttributes.id**</span></span>](ambientattributes-id.md)
</dt> </dl>

 

 





