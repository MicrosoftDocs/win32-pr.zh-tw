---
title: " (WSManDisp 的列舉常數) "
description: 列舉包含下列清單所列的常數，會透過呼叫 Session. 列舉和 Iwsmansession.invoke 列舉來用於旗標參數中。
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422f688fea992ee2d9b1d0d25af00a1d24ad798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384266"
---
# <a name="enumeration-constants"></a><span data-ttu-id="c1b6b-103">列舉常數</span><span class="sxs-lookup"><span data-stu-id="c1b6b-103">Enumeration Constants</span></span>

<span data-ttu-id="c1b6b-104">**\_ \_ WSManEnumFlags** 列舉包含下列清單中所列的常數，會透過呼叫 [**Session. 列舉**](session-enumerate.md)和 [**iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)來用於 *旗標* 參數中。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-104">The **\_\_WSManEnumFlags** enumeration contains constants, as listed in the following list, used in the *flags* parameter by calls to [**Session.Enumerate**](session-enumerate.md) and [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

<span data-ttu-id="c1b6b-105">請注意，如果未指定 *flags* 參數， **WSManFlagReturnObject** 和 **WSManFlagHierarchyDeep** 是預設值。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-105">Be aware that **WSManFlagReturnObject** and **WSManFlagHierarchyDeep** are the default if the *flags* parameter is not specified.</span></span>

<dl> <dt>

<span data-ttu-id="c1b6b-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span><span class="sxs-lookup"><span data-stu-id="c1b6b-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1b6b-107">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="c1b6b-107">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="c1b6b-108">批次包含要求的 XML 實例。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-108">Batches contain the requested XML instances.</span></span> <span data-ttu-id="c1b6b-109">這是旗標參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-109">This is the default value for the flag parameter.</span></span>

<span data-ttu-id="c1b6b-110">相關聯的腳本方法是 [**WSMan. EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject)。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-110">The associated scripting method is [**WSMan.EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1b6b-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span><span class="sxs-lookup"><span data-stu-id="c1b6b-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1b6b-112">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="c1b6b-112">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="c1b6b-113">此旗標會控制對 Session 呼叫中 *篩選* 參數的方式。由 WinRM 來解讀 [**列舉**](session-enumerate.md) 。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-113">This flag controls how the *filter* parameter in the call to [**Session.Enumerate**](session-enumerate.md) is interpreted by WinRM.</span></span>

<span data-ttu-id="c1b6b-114">篩選的格式可以是 XML 片段或純文字字串。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-114">The format of the filter may be an XML fragment or a string of plain text.</span></span> <span data-ttu-id="c1b6b-115">格式取決於呼叫 [**Session. 列舉**](session-enumerate.md)或 [**Iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)中所使用之 [*篩選*](windows-remote-management-glossary.md)條件的 [*篩選方言*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-115">The format is determined by the [*filter dialect*](windows-remote-management-glossary.md) of the [*filter*](windows-remote-management-glossary.md) used in the call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), which is specific to the operation performed.</span></span>

<span data-ttu-id="c1b6b-116">如果未指定 *方言* 參數，WinRM 會嘗試根據篩選準則的第一個字元來決定方言。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-116">If the *dialect* parameter is not specified, WinRM attempts to determine the dialect based on the first character of the filter.</span></span> <span data-ttu-id="c1b6b-117">如果 < 第一個字元，但篩選並不是 XML 片段，則應該設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-117">If the first character is <, but the filter is not actually an XML fragment, then this flag should be set.</span></span> <span data-ttu-id="c1b6b-118">例如，下列格式的篩選準則需要您設定 **WSManFlagNonXmlText** ，才能正確地解讀篩選：</span><span class="sxs-lookup"><span data-stu-id="c1b6b-118">For example, a filter in the following format requires that you set **WSManFlagNonXmlText** so that the filter is correctly interpreted:</span></span>

`<25 && > 1`

<span data-ttu-id="c1b6b-119">如果篩選是 XML 片段，則不需要此旗標，因為片段會以 < （WinRM 正確地解讀為 XML）開頭。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-119">If the filter is an XML fragment, then this flag is not required because the fragment starts with <, which WinRM correctly interprets as XML.</span></span> <span data-ttu-id="c1b6b-120">例如，</span><span class="sxs-lookup"><span data-stu-id="c1b6b-120">For example,</span></span>

`<filter>select * from aDataStructure</filter>`

<span data-ttu-id="c1b6b-121">如果篩選是不是以 < 開頭的純文字，則不需要此旗標。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-121">If the filter is in plain text that does not start with <, then this flag is not required.</span></span> <span data-ttu-id="c1b6b-122">例如，</span><span class="sxs-lookup"><span data-stu-id="c1b6b-122">For example,</span></span>

`select * from aDataStructure`

<span data-ttu-id="c1b6b-123">相關聯的腳本方法是 [**WSMan. EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext)。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-123">The associated scripting method is [**WSMan.EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) and the C++ method is [**IWSManEx.EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1b6b-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span><span class="sxs-lookup"><span data-stu-id="c1b6b-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1b6b-125">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="c1b6b-125">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="c1b6b-126">批次包含對應 XML 實例 (EPRs) 的端點參考，但不包含實際實例。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-126">Batches contain endpoint references (EPRs) for the corresponding XML instances, but not the actual instances.</span></span>

<span data-ttu-id="c1b6b-127">相關聯的腳本方法是 [**WSMan. EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr)。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-127">The associated scripting method is [**WSMan.EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1b6b-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span><span class="sxs-lookup"><span data-stu-id="c1b6b-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1b6b-129">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="c1b6b-129">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="c1b6b-130">批次包含所要求的 XML 實例，以及 [*wsman： Items*](windows-remote-management-glossary.md) 元素中包含的對應 EPRs。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-130">Batches contain both the requested XML instances and the corresponding EPRs contained in a [*wsman:Items*](windows-remote-management-glossary.md) element.</span></span>

<span data-ttu-id="c1b6b-131">相關聯的腳本方法是 [**WSMan. EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr)。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-131">The associated scripting method is [**WSMan.EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1b6b-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span><span class="sxs-lookup"><span data-stu-id="c1b6b-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1b6b-133">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="c1b6b-133">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="c1b6b-134">系統會包含衍生類別實例，並根據其實際的架構來表示。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-134">Derived class instances are included and are represented according to their actual schemas.</span></span>

<span data-ttu-id="c1b6b-135">相關聯的腳本方法是 [**WSMan. EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep)。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-135">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1b6b-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span><span class="sxs-lookup"><span data-stu-id="c1b6b-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1b6b-137">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="c1b6b-137">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="c1b6b-138">排除衍生類別實例。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-138">Derived class instances are excluded.</span></span> <span data-ttu-id="c1b6b-139">只會顯示所要求之類型的實例。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-139">Only instances of the requested type are shown.</span></span>

<span data-ttu-id="c1b6b-140">相關聯的腳本方法是 [**WSMan. EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow)。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-140">The associated scripting method is [**WSMan.EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c1b6b-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span><span class="sxs-lookup"><span data-stu-id="c1b6b-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1b6b-142">64 (0x40) </span><span class="sxs-lookup"><span data-stu-id="c1b6b-142">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="c1b6b-143">系統會包含衍生類別實例，並根據基類架構來表示。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-143">Derived class instances are included and are represented according to the base class schema.</span></span> <span data-ttu-id="c1b6b-144">不會顯示衍生類別中定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-144">Properties defined in the derived class are not shown.</span></span>

<span data-ttu-id="c1b6b-145">相關聯的腳本方法是 [**WSMan. EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) ，而 c + + 方法是 [**IWSManEx. EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly)。</span><span class="sxs-lookup"><span data-stu-id="c1b6b-145">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1b6b-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1b6b-146">Requirements</span></span>



| <span data-ttu-id="c1b6b-147">需求</span><span class="sxs-lookup"><span data-stu-id="c1b6b-147">Requirement</span></span> | <span data-ttu-id="c1b6b-148">值</span><span class="sxs-lookup"><span data-stu-id="c1b6b-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b6b-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1b6b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c1b6b-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1b6b-150">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c1b6b-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1b6b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c1b6b-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1b6b-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c1b6b-153">標頭</span><span class="sxs-lookup"><span data-stu-id="c1b6b-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1b6b-154"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1b6b-154"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1b6b-155">Idl</span><span class="sxs-lookup"><span data-stu-id="c1b6b-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c1b6b-156"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c1b6b-156"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1b6b-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1b6b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b6b-158">WinRM 常數和列舉</span><span class="sxs-lookup"><span data-stu-id="c1b6b-158">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="c1b6b-159">列舉或列出資源的所有實例</span><span class="sxs-lookup"><span data-stu-id="c1b6b-159">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="c1b6b-160">查詢資源的特定實例</span><span class="sxs-lookup"><span data-stu-id="c1b6b-160">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





