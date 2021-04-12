---
description: 指定編解碼器輸出中主要畫面格之間的最長時間（以毫秒為單位）。
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: 'MFPKEY_KEYDIST 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848808"
---
# <a name="mfpkey_keydist-property"></a><span data-ttu-id="9109a-103">MFPKEY \_ KEYDIST 屬性</span><span class="sxs-lookup"><span data-stu-id="9109a-103">MFPKEY\_KEYDIST Property</span></span>

<span data-ttu-id="9109a-104">指定編解碼器輸出中主要畫面格之間的最長時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9109a-104">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9109a-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="9109a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9109a-106">g \_ wszWMVCKeyframeDistance</span><span class="sxs-lookup"><span data-stu-id="9109a-106">g\_wszWMVCKeyframeDistance</span></span>

## <a name="data-type"></a><span data-ttu-id="9109a-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="9109a-107">Data Type</span></span>

<span data-ttu-id="9109a-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9109a-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="9109a-109">預設值</span><span class="sxs-lookup"><span data-stu-id="9109a-109">Default Value</span></span>

<span data-ttu-id="9109a-110">預設值取決於正在執行的 Windows 版本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="9109a-110">The default value depends on which version of Windows is running, as shown in the following table.</span></span>



| <span data-ttu-id="9109a-111">作業系統</span><span class="sxs-lookup"><span data-stu-id="9109a-111">Operating system</span></span> | <span data-ttu-id="9109a-112">預設值</span><span class="sxs-lookup"><span data-stu-id="9109a-112">Default value</span></span> |
|------------------|---------------|
| <span data-ttu-id="9109a-113">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9109a-113">Windows XP</span></span>       | <span data-ttu-id="9109a-114">8000</span><span class="sxs-lookup"><span data-stu-id="9109a-114">8000</span></span>          |
| <span data-ttu-id="9109a-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9109a-115">Windows Vista</span></span>    | <span data-ttu-id="9109a-116">8000</span><span class="sxs-lookup"><span data-stu-id="9109a-116">8000</span></span>          |
| <span data-ttu-id="9109a-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9109a-117">Windows 7</span></span>        | <span data-ttu-id="9109a-118">2000</span><span class="sxs-lookup"><span data-stu-id="9109a-118">2000</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="9109a-119">備註</span><span class="sxs-lookup"><span data-stu-id="9109a-119">Remarks</span></span>

<span data-ttu-id="9109a-120">編解碼器的內部邏輯會決定每個主要畫面格的實際位置。</span><span class="sxs-lookup"><span data-stu-id="9109a-120">The internal logic of the codec determines the actual location of each key frame.</span></span> <span data-ttu-id="9109a-121">任何兩個主要畫面格之間的距離可能小於這個屬性的值，不過，它永遠不會大於。</span><span class="sxs-lookup"><span data-stu-id="9109a-121">The distance between any two key frames may be less than the value of this property, however, it will never be greater.</span></span>

## <a name="requirements"></a><span data-ttu-id="9109a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9109a-122">Requirements</span></span>



| <span data-ttu-id="9109a-123">需求</span><span class="sxs-lookup"><span data-stu-id="9109a-123">Requirement</span></span> | <span data-ttu-id="9109a-124">值</span><span class="sxs-lookup"><span data-stu-id="9109a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9109a-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9109a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9109a-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9109a-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9109a-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9109a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9109a-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9109a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9109a-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9109a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9109a-130"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9109a-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9109a-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9109a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9109a-132">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="9109a-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




