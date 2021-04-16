---
description: 指定用來對動作向量資訊進行編碼的方法。
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: 'MFPKEY_DELTAMVRANGEINDEX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513112"
---
# <a name="mfpkey_deltamvrangeindex-property"></a><span data-ttu-id="72d9c-103">MFPKEY \_ DELTAMVRANGEINDEX 屬性</span><span class="sxs-lookup"><span data-stu-id="72d9c-103">MFPKEY\_DELTAMVRANGEINDEX Property</span></span>

<span data-ttu-id="72d9c-104">指定用來對動作向量資訊進行編碼的方法。</span><span class="sxs-lookup"><span data-stu-id="72d9c-104">Specifies the method used to encode the motion vector information.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="72d9c-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="72d9c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="72d9c-106">g \_ wszWMVCDeltaMVRangeIndex</span><span class="sxs-lookup"><span data-stu-id="72d9c-106">g\_wszWMVCDeltaMVRangeIndex</span></span>

## <a name="data-type"></a><span data-ttu-id="72d9c-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="72d9c-107">Data Type</span></span>

<span data-ttu-id="72d9c-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="72d9c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="72d9c-109">預設值</span><span class="sxs-lookup"><span data-stu-id="72d9c-109">Default Value</span></span>

<span data-ttu-id="72d9c-110">0</span><span class="sxs-lookup"><span data-stu-id="72d9c-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="72d9c-111">備註</span><span class="sxs-lookup"><span data-stu-id="72d9c-111">Remarks</span></span>

<span data-ttu-id="72d9c-112">如果設定此屬性，則編碼器會在欄位中增加差異動作向量範圍。</span><span class="sxs-lookup"><span data-stu-id="72d9c-112">If this property is set, the encoder increases the delta motion vector range in fields.</span></span> <span data-ttu-id="72d9c-113">動作向量資訊只對交錯式欄位有效。</span><span class="sxs-lookup"><span data-stu-id="72d9c-113">Motion vector information is valid only for interlaced fields.</span></span>

<span data-ttu-id="72d9c-114">這個屬性可以設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="72d9c-114">This property may be set to one of the following values:</span></span>



| <span data-ttu-id="72d9c-115">值</span><span class="sxs-lookup"><span data-stu-id="72d9c-115">Value</span></span> | <span data-ttu-id="72d9c-116">描述</span><span class="sxs-lookup"><span data-stu-id="72d9c-116">Description</span></span>                                                                          |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="72d9c-117">0</span><span class="sxs-lookup"><span data-stu-id="72d9c-117">0</span></span>     | <span data-ttu-id="72d9c-118">使用現有的 delta 動作向量範圍。</span><span class="sxs-lookup"><span data-stu-id="72d9c-118">Use the existing delta motion vector range.</span></span>                                          |
| <span data-ttu-id="72d9c-119">1</span><span class="sxs-lookup"><span data-stu-id="72d9c-119">1</span></span>     | <span data-ttu-id="72d9c-120">以水準方向按兩下差異動作向量範圍。</span><span class="sxs-lookup"><span data-stu-id="72d9c-120">Double the delta motion vector range in the horizontal direction.</span></span>                    |
| <span data-ttu-id="72d9c-121">2</span><span class="sxs-lookup"><span data-stu-id="72d9c-121">2</span></span>     | <span data-ttu-id="72d9c-122">以垂直方向按兩下差異動作向量範圍。</span><span class="sxs-lookup"><span data-stu-id="72d9c-122">Double the delta motion vector range in the vertical direction.</span></span>                      |
| <span data-ttu-id="72d9c-123">3</span><span class="sxs-lookup"><span data-stu-id="72d9c-123">3</span></span>     | <span data-ttu-id="72d9c-124">以水準和垂直方向，將差異動作向量範圍加倍。</span><span class="sxs-lookup"><span data-stu-id="72d9c-124">Double the delta motion vector range in both the horizontal and vertical directions.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="72d9c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="72d9c-125">Requirements</span></span>



| <span data-ttu-id="72d9c-126">需求</span><span class="sxs-lookup"><span data-stu-id="72d9c-126">Requirement</span></span> | <span data-ttu-id="72d9c-127">值</span><span class="sxs-lookup"><span data-stu-id="72d9c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72d9c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72d9c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="72d9c-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72d9c-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="72d9c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72d9c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="72d9c-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72d9c-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72d9c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="72d9c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="72d9c-133"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="72d9c-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72d9c-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72d9c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d9c-135">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="72d9c-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




