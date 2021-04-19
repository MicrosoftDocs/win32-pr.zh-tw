---
description: 提供 SWbemObject 的擴充功能。 如同 SWbemObject，所有的 WMI 物件都可以使用此擴充物件的方法。
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.tgt_platform: multiple
title: 'SWbemObjectEx 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx
- SetFromText_
- ISWbemObjectEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: abed8c1d58687203aaeb32918cf15b2785b92622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997110"
---
# <a name="swbemobjectex-object"></a><span data-ttu-id="f081b-104">SWbemObjectEx 物件</span><span class="sxs-lookup"><span data-stu-id="f081b-104">SWbemObjectEx object</span></span>

<span data-ttu-id="f081b-105">**SWbemObjectEx** 物件提供 [**SWbemObject**](swbemobject.md)的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="f081b-105">The **SWbemObjectEx** object provides extended functionality for [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="f081b-106">如同 **SWbemObject**，所有的 WMI 物件都可以使用此擴充物件的方法。</span><span class="sxs-lookup"><span data-stu-id="f081b-106">Like **SWbemObject**, the methods of this extended object can be used by all WMI objects.</span></span> <span data-ttu-id="f081b-107">VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="f081b-107">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="f081b-108">成員</span><span class="sxs-lookup"><span data-stu-id="f081b-108">Members</span></span>

<span data-ttu-id="f081b-109">**SWbemObjectEx** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f081b-109">The **SWbemObjectEx** object has these types of members:</span></span>

-   [<span data-ttu-id="f081b-110">方法</span><span class="sxs-lookup"><span data-stu-id="f081b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f081b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f081b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f081b-112">方法</span><span class="sxs-lookup"><span data-stu-id="f081b-112">Methods</span></span>

<span data-ttu-id="f081b-113">**SWbemObjectEx** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f081b-113">The **SWbemObjectEx** object has these methods.</span></span>



| <span data-ttu-id="f081b-114">方法</span><span class="sxs-lookup"><span data-stu-id="f081b-114">Method</span></span>                                      | <span data-ttu-id="f081b-115">描述</span><span class="sxs-lookup"><span data-stu-id="f081b-115">Description</span></span>                                                              |
|:--------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="f081b-116">**GetText\_**</span><span class="sxs-lookup"><span data-stu-id="f081b-116">**GetText\_**</span></span>](swbemobjectex-gettext-.md) | <span data-ttu-id="f081b-117">傳回文字檔，此文字檔會以 XML 顯示物件的內容。</span><span class="sxs-lookup"><span data-stu-id="f081b-117">Returns a text file showing the contents of an object in XML.</span></span><br/> |
| [<span data-ttu-id="f081b-118">**重新整理\_**</span><span class="sxs-lookup"><span data-stu-id="f081b-118">**Refresh\_**</span></span>](swbemobjectex-refresh-.md) | <span data-ttu-id="f081b-119">重新整理物件中的資料。</span><span class="sxs-lookup"><span data-stu-id="f081b-119">Refreshes data in an object.</span></span><br/>                                  |
| <span data-ttu-id="f081b-120">**SetFromText\_**</span><span class="sxs-lookup"><span data-stu-id="f081b-120">**SetFromText\_**</span></span>                           | <span data-ttu-id="f081b-121">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="f081b-121">Reserved for future use.</span></span><br/>                                      |



 

### <a name="properties"></a><span data-ttu-id="f081b-122">屬性</span><span class="sxs-lookup"><span data-stu-id="f081b-122">Properties</span></span>

<span data-ttu-id="f081b-123">**SWbemObjectEx** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f081b-123">The **SWbemObjectEx** object has these properties.</span></span>



| <span data-ttu-id="f081b-124">屬性</span><span class="sxs-lookup"><span data-stu-id="f081b-124">Property</span></span>                                                                 | <span data-ttu-id="f081b-125">存取類型</span><span class="sxs-lookup"><span data-stu-id="f081b-125">Access type</span></span>           | <span data-ttu-id="f081b-126">Description</span><span class="sxs-lookup"><span data-stu-id="f081b-126">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f081b-127">**SystemProperties\_**</span><span class="sxs-lookup"><span data-stu-id="f081b-127">**SystemProperties\_**</span></span>](swbemobjectex-systemproperties-.md)<br/> | <span data-ttu-id="f081b-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f081b-128">Read/write</span></span><br/> | <span data-ttu-id="f081b-129">[**內含**](swbempropertyset.md)物件，其中包含適用于 **SWbemObjectEx** 的系統屬性集合。</span><span class="sxs-lookup"><span data-stu-id="f081b-129">An [**SWbemPropertySet**](swbempropertyset.md) object that contains the collection of system properties that apply to the **SWbemObjectEx**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f081b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f081b-130">Requirements</span></span>



| <span data-ttu-id="f081b-131">需求</span><span class="sxs-lookup"><span data-stu-id="f081b-131">Requirement</span></span> | <span data-ttu-id="f081b-132">值</span><span class="sxs-lookup"><span data-stu-id="f081b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f081b-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f081b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f081b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f081b-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f081b-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f081b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f081b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f081b-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f081b-137">標頭</span><span class="sxs-lookup"><span data-stu-id="f081b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f081b-138"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="f081b-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f081b-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f081b-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="f081b-140"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f081b-140"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f081b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f081b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f081b-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f081b-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f081b-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="f081b-143">CLSID</span></span><br/>                    | <span data-ttu-id="f081b-144">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="f081b-144">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="f081b-145">IID</span><span class="sxs-lookup"><span data-stu-id="f081b-145">IID</span></span><br/>                      | <span data-ttu-id="f081b-146">IID \_ ISWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="f081b-146">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f081b-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f081b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f081b-148">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="f081b-148">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="f081b-149">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="f081b-149">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="f081b-150">WbemObjectTextFormatEnum</span><span class="sxs-lookup"><span data-stu-id="f081b-150">WbemObjectTextFormatEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> </dl>

 

