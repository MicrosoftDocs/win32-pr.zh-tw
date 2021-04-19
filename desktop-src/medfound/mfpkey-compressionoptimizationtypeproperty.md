---
description: 指定要用於 Windows Media 視訊 9 Advanced Profile 編碼器的最佳視覺品質設定。
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: 'MFPKEY_COMPRESSIONOPTIMIZATIONTYPE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974228"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a><span data-ttu-id="18c2a-103">MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE 屬性</span><span class="sxs-lookup"><span data-stu-id="18c2a-103">MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE Property</span></span>

<span data-ttu-id="18c2a-104">指定要用於 Windows Media 視訊 9 Advanced Profile 編碼器的最佳視覺品質設定。</span><span class="sxs-lookup"><span data-stu-id="18c2a-104">Specifies the optimal visual quality settings to use for the Windows Media Video 9 Advanced Profile encoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="18c2a-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="18c2a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="18c2a-106">g \_ wszWMVCCompressionOptimizationType</span><span class="sxs-lookup"><span data-stu-id="18c2a-106">g\_wszWMVCCompressionOptimizationType</span></span>

## <a name="data-type"></a><span data-ttu-id="18c2a-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="18c2a-107">Data Type</span></span>

<span data-ttu-id="18c2a-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="18c2a-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="18c2a-109">預設值</span><span class="sxs-lookup"><span data-stu-id="18c2a-109">Default Value</span></span>

<span data-ttu-id="18c2a-110">0</span><span class="sxs-lookup"><span data-stu-id="18c2a-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="18c2a-111">備註</span><span class="sxs-lookup"><span data-stu-id="18c2a-111">Remarks</span></span>

<span data-ttu-id="18c2a-112">這個屬性可讓您快速地設定數種影片編碼選項。</span><span class="sxs-lookup"><span data-stu-id="18c2a-112">This property provides a quick way to configure a number of video encoding options.</span></span> <span data-ttu-id="18c2a-113">它可能會設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="18c2a-113">It may be set to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18c2a-114">值</span><span class="sxs-lookup"><span data-stu-id="18c2a-114">Value</span></span></th>
<th><span data-ttu-id="18c2a-115">描述</span><span class="sxs-lookup"><span data-stu-id="18c2a-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18c2a-116">0</span><span class="sxs-lookup"><span data-stu-id="18c2a-116">0</span></span></td>
<td><span data-ttu-id="18c2a-117">編解碼器不會強制優化，而且會使用其他屬性指定的任何功能。</span><span class="sxs-lookup"><span data-stu-id="18c2a-117">The codec will not force optimization and will use whatever features are specified by other properties.</span></span> <span data-ttu-id="18c2a-118">在許多情況下，編解碼器將會使用內部邏輯來判斷未指定的設定。</span><span class="sxs-lookup"><span data-stu-id="18c2a-118">In many cases, the codec will use internal logic to determine settings if they are not specified.</span></span> <span data-ttu-id="18c2a-119">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="18c2a-119">This is the default value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18c2a-120">1</span><span class="sxs-lookup"><span data-stu-id="18c2a-120">1</span></span></td>
<td><span data-ttu-id="18c2a-121">啟用將產生最佳視覺品質的功能。使用此值會設定編解碼器，就如同您已設定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="18c2a-121">Enables the features that will produce the best visual quality.Using this value configures the codec as if you had set the following properties:</span></span><br/>
<ul>
<li><span data-ttu-id="18c2a-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span><span class="sxs-lookup"><span data-stu-id="18c2a-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span></span></li>
<li><span data-ttu-id="18c2a-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span><span class="sxs-lookup"><span data-stu-id="18c2a-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span></span></li>
<li><span data-ttu-id="18c2a-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span><span class="sxs-lookup"><span data-stu-id="18c2a-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span></span></li>
<li><span data-ttu-id="18c2a-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</span><span class="sxs-lookup"><span data-stu-id="18c2a-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</span></span></li>
<li><span data-ttu-id="18c2a-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span><span class="sxs-lookup"><span data-stu-id="18c2a-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span></span></li>
<li><span data-ttu-id="18c2a-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</span><span class="sxs-lookup"><span data-stu-id="18c2a-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</span></span></li>
<li><span data-ttu-id="18c2a-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span><span class="sxs-lookup"><span data-stu-id="18c2a-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span></span></li>
</ul>
<span data-ttu-id="18c2a-129">如果您在上一個清單中設定任何屬性，您設定的值會覆寫與此設定相關聯的值，但 <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>除外。</span><span class="sxs-lookup"><span data-stu-id="18c2a-129">If you set any of the properties in the previous list, the value you set overrides the values associated with this setting, except for <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="18c2a-130">將 MFPKEY COMPRESSIONOPTIMIZATIONTYPE 屬性的值設定 \_ 為1，也有將 Dquant 選項登錄設定設定為2，以及將「動作向量成本」方法登錄設定為1的效果。</span><span class="sxs-lookup"><span data-stu-id="18c2a-130">Setting the value of the MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE property to 1 also has the effect of setting the Dquant Option registry setting to 2, and the Motion Vector Cost Method registry setting to 1.</span></span> <span data-ttu-id="18c2a-131">如需詳細資訊，請參閱 [使用 Windows Media 視訊 9 Advanced Profile 編解碼器的 Advanced 設定](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)的 web 文章。</span><span class="sxs-lookup"><span data-stu-id="18c2a-131">For more information, see the web article [Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="18c2a-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="18c2a-132">Requirements</span></span>



| <span data-ttu-id="18c2a-133">需求</span><span class="sxs-lookup"><span data-stu-id="18c2a-133">Requirement</span></span> | <span data-ttu-id="18c2a-134">值</span><span class="sxs-lookup"><span data-stu-id="18c2a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18c2a-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18c2a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="18c2a-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18c2a-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="18c2a-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18c2a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="18c2a-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18c2a-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18c2a-139">標頭</span><span class="sxs-lookup"><span data-stu-id="18c2a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="18c2a-140"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="18c2a-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18c2a-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18c2a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18c2a-142">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="18c2a-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




