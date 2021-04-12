---
description: 定義值，這些值會指定辨識替代項的屬性。  (API) 的 Tablet PC 應用程式開發介面，會使用全域唯一識別碼 (Guid) 來識別封包屬性（在自動化中是常數位符串）。
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: 'RecognitionProperty 常數 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62971276b6348af3d8ac971851d70b03f7b003c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320431"
---
# <a name="recognitionproperty-constants"></a><span data-ttu-id="f3fd1-104">RecognitionProperty 常數</span><span class="sxs-lookup"><span data-stu-id="f3fd1-104">RecognitionProperty Constants</span></span>

<span data-ttu-id="f3fd1-105">定義值，這些值會指定辨識替代項的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-105">Defines values that specify the properties of a recognition alternate.</span></span> <span data-ttu-id="f3fd1-106"> (API) 的 Tablet PC 應用程式開發介面，會使用全域唯一識別碼 (Guid) 來識別封包屬性（在自動化中是常數位符串）。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-106">The Tablet PC application programming interface (API) uses globally unique identifiers (GUIDs) to identify packet properties, which in Automation are constant strings.</span></span>

<span data-ttu-id="f3fd1-107">下表列出可用的辨識替代屬性全域唯一識別碼 (GUID) 欄位。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-107">The following table lists the available recognition alternate property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="f3fd1-108">藉由呼叫 [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue)方法，使用這些 guid 來存取 [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate)物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-108">Use these GUIDs to access properties of an [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object by calling the [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) method.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f3fd1-109">常數名稱</span><span class="sxs-lookup"><span data-stu-id="f3fd1-109">Constant Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f3fd1-110">Description</span><span class="sxs-lookup"><span data-stu-id="f3fd1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <span data-ttu-id="f3fd1-111"><dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f3fd1-111"><dt> <strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f3fd1-112">識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件行號屬性的 GUID。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-112">The GUID that identifies the property for the line number of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="f3fd1-113">LineNumber 指定具有特定行號的替代項。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-113">LineNumber specifies the alternates with a particular line number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3fd1-114">東亞字元的辨識器不支援此欄位。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-114">This field is not supported for recognizers of East Asian characters.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <span data-ttu-id="f3fd1-115"><dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f3fd1-115"><dt> <strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f3fd1-116">識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件之分割屬性的 GUID。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-116">The GUID that identifies the property for the segmentation of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/> <span data-ttu-id="f3fd1-117">分割會指定辨識器用來產生辨識結果的基本筆墨片段或單位。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-117">Segmentation specifies the basic ink fragment or unit that the recognizer uses to produce a recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3fd1-118">未實作。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-118">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <span data-ttu-id="f3fd1-119"><dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f3fd1-119"><dt> <strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f3fd1-120">識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件之辨識作用點屬性的 GUID。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-120">The GUID that identifies the property for the recognition hot point of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <span data-ttu-id="f3fd1-121"><dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f3fd1-121"><dt> <strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f3fd1-122">GUID，識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件之辨識結果的最大筆觸計數的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-122">The GUID that identifies the property for the maximum stroke count of the recognition result for the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3fd1-123">未實作。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-123">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <span data-ttu-id="f3fd1-124"><dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f3fd1-124"><dt> <strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f3fd1-125">GUID，可識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件之每英寸點的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-125">The GUID that identifies the property for the points-per-inch metric of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3fd1-126">未實作。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-126">Not implemented.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <span data-ttu-id="f3fd1-127"><dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f3fd1-127"><dt> <strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f3fd1-128">GUID，可識別辨識器在辨識結果中的信賴層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-128">The GUID that identifies the property for the level of confidence that the recognizer has in the recognition result.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f3fd1-129">信賴評估版僅適用于 Microsoft Windows XP Tablet PC Edition 和 Windows Vista 中的美國英文和所有手勢辨識器。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-129">Confidence evaluation is available only for United States English and all gesture recognizers in Microsoft Windows XP Tablet PC Edition and Windows Vista.</span></span> <span data-ttu-id="f3fd1-130">為任何其他辨識器提供信賴屬性的方法會傳回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-130">Methods that provide the confidence property for any other recognizer return E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <span data-ttu-id="f3fd1-131"><dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f3fd1-131"><dt> <strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f3fd1-132">識別 <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> 物件之線條度量屬性的 GUID，這是用來取得度量的行。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-132">The GUID that identifies the property for the line metrics of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> object, which is the line for which to retrieve metrics.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="f3fd1-133">備註</span><span class="sxs-lookup"><span data-stu-id="f3fd1-133">Remarks</span></span>

<span data-ttu-id="f3fd1-134">在 c + + 中，您可以在 Msinkaut .h 標頭檔中存取這些常數， <systemdrive> \\ \\ \\ \\ \\ 如果您將 SDK 安裝在預設位置，該檔案位於： Program Files Microsoft sdk Windows 6.0 Include 目錄。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-134">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="f3fd1-135">在 c + + 中，這些常數是 WCHARs，而不是 Bstr。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-135">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="f3fd1-136">使用之前，請先將它們轉換成 Bstr。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-136">Convert them into BSTRs before use.</span></span> <span data-ttu-id="f3fd1-137">如需 BSTR 資料類型的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="f3fd1-137">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f3fd1-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3fd1-138">Requirements</span></span>



| <span data-ttu-id="f3fd1-139">需求</span><span class="sxs-lookup"><span data-stu-id="f3fd1-139">Requirement</span></span> | <span data-ttu-id="f3fd1-140">值</span><span class="sxs-lookup"><span data-stu-id="f3fd1-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3fd1-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3fd1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f3fd1-142">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3fd1-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f3fd1-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3fd1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f3fd1-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="f3fd1-144">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f3fd1-145">標頭</span><span class="sxs-lookup"><span data-stu-id="f3fd1-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3fd1-146"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="f3fd1-146"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3fd1-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3fd1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3fd1-148">**AlternatesWithConstantPropertyValues 方法**</span><span class="sxs-lookup"><span data-stu-id="f3fd1-148">**AlternatesWithConstantPropertyValues Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[<span data-ttu-id="f3fd1-149">**ConfidenceAlternates 屬性**</span><span class="sxs-lookup"><span data-stu-id="f3fd1-149">**ConfidenceAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[<span data-ttu-id="f3fd1-150">**LineAlternates 屬性**</span><span class="sxs-lookup"><span data-stu-id="f3fd1-150">**LineAlternates Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[<span data-ttu-id="f3fd1-151">**IInkRecognitionAlternates 介面**</span><span class="sxs-lookup"><span data-stu-id="f3fd1-151">**IInkRecognitionAlternates Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




