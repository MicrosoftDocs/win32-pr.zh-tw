---
title: AmbientAttributes。已啟用
description: Enabled 屬性會指定或抓取值，指出控制項是否已啟用或停用。
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- AmbientAttributes 已啟用 Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988659"
---
# <a name="ambientattributesenabled"></a><span data-ttu-id="cb40d-104">AmbientAttributes。已啟用</span><span class="sxs-lookup"><span data-stu-id="cb40d-104">AmbientAttributes.enabled</span></span>

<span data-ttu-id="cb40d-105">**Enabled** 屬性會指定或抓取值，指出控制項是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="cb40d-105">The **enabled** attribute specifies or retrieves a value indicating whether the control is enabled or disabled.</span></span>

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a><span data-ttu-id="cb40d-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="cb40d-106">Possible Values</span></span>

<span data-ttu-id="cb40d-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="cb40d-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="cb40d-108">值</span><span class="sxs-lookup"><span data-stu-id="cb40d-108">Value</span></span> | <span data-ttu-id="cb40d-109">描述</span><span class="sxs-lookup"><span data-stu-id="cb40d-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="cb40d-110">true</span><span class="sxs-lookup"><span data-stu-id="cb40d-110">true</span></span>  | <span data-ttu-id="cb40d-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="cb40d-111">Default.</span></span> <span data-ttu-id="cb40d-112">控制項已啟用。</span><span class="sxs-lookup"><span data-stu-id="cb40d-112">Control enabled.</span></span> |
| <span data-ttu-id="cb40d-113">false</span><span class="sxs-lookup"><span data-stu-id="cb40d-113">false</span></span> | <span data-ttu-id="cb40d-114">控制項已停用。</span><span class="sxs-lookup"><span data-stu-id="cb40d-114">Control disabled.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="cb40d-115">備註</span><span class="sxs-lookup"><span data-stu-id="cb40d-115">Remarks</span></span>

<span data-ttu-id="cb40d-116">如果已啟用控制項，它可能會有索引標籤停止，並會接收所有環境事件。</span><span class="sxs-lookup"><span data-stu-id="cb40d-116">If the control is enabled, it can have a tab stop, and will receive all ambient events.</span></span> <span data-ttu-id="cb40d-117">停用時，控制項就不會有索引標籤停止，而且不會收到任何對它引發的環境滑鼠或鍵盤事件。</span><span class="sxs-lookup"><span data-stu-id="cb40d-117">When disabled, the control does not have a tab stop, and does not receive any ambient mouse or keyboard events fired to it.</span></span> <span data-ttu-id="cb40d-118">不過 (，它將會繼續接收所有其他引發的環境事件。 ) </span><span class="sxs-lookup"><span data-stu-id="cb40d-118">(However, it will continue to receive all other ambient events fired to it.)</span></span>

<span data-ttu-id="cb40d-119">子 **視圖** 元素不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="cb40d-119">This attribute is not supported for the **SUBVIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb40d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb40d-120">Requirements</span></span>



| <span data-ttu-id="cb40d-121">需求</span><span class="sxs-lookup"><span data-stu-id="cb40d-121">Requirement</span></span> | <span data-ttu-id="cb40d-122">值</span><span class="sxs-lookup"><span data-stu-id="cb40d-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cb40d-123">版本</span><span class="sxs-lookup"><span data-stu-id="cb40d-123">Version</span></span><br/> | <span data-ttu-id="cb40d-124">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="cb40d-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cb40d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb40d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb40d-126">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="cb40d-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





