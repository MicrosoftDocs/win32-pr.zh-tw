---
title: 'ResourceLocator 物件 (WSManDisp) '
description: 提供資源的路徑。 您可以使用 ResourceLocator 物件，而不是會話物件作業中的資源 URI，例如 Session. Get、Session. Put 或 Session。列舉。
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- ResourceLocator 物件 Windows 遠端管理
- ResourceLocator 物件 Windows 遠端管理，說明
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094027"
---
# <a name="resourcelocator-object"></a><span data-ttu-id="d1cd3-106">ResourceLocator 物件</span><span class="sxs-lookup"><span data-stu-id="d1cd3-106">ResourceLocator object</span></span>

<span data-ttu-id="d1cd3-107">提供資源路徑的物件。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-107">An object that supplies the path to a resource.</span></span> <span data-ttu-id="d1cd3-108">您可以使用 **ResourceLocator** 物件，而不是 [**會話**](session.md)物件作業中的 [*資源 URI*](windows-remote-management-glossary.md) ，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-108">You can use a **ResourceLocator** object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="d1cd3-109">此物件可讓您：</span><span class="sxs-lookup"><span data-stu-id="d1cd3-109">This object enables you to:</span></span>

-   <span data-ttu-id="d1cd3-110">新增一或多個識別特定資源實例的 [*選取器*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-110">Add one or more [*selectors*](windows-remote-management-glossary.md) that identify a particular instance of a resource.</span></span> <span data-ttu-id="d1cd3-111">這與在使用金鑰的資源的資源 URI 中提供金鑰值相同。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-111">This is the same as supplying a key value in the resource URI for a resource that uses keys.</span></span> <span data-ttu-id="d1cd3-112">如需詳細資訊，請參閱 [**ResourceLocator. AddSelector**](resourcelocator-addselector.md)。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-112">For more information, see [**ResourceLocator.AddSelector**](resourcelocator-addselector.md).</span></span> <span data-ttu-id="d1cd3-113">您可以使用呼叫 [**Session. 列舉**](session-enumerate.md)中的 *filter* 參數來進行類似的作業。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-113">You can do a similar operation using the *filter* parameter in a call to [**Session.Enumerate**](session-enumerate.md).</span></span>
-   <span data-ttu-id="d1cd3-114">指定 [*片段*](windows-remote-management-glossary.md) 路徑和方言，以只取得資源的一個屬性。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-114">Specify a [*fragment*](windows-remote-management-glossary.md) path and dialect to get only one property of a resource.</span></span> <span data-ttu-id="d1cd3-115">您也可以藉由提供陣列索引來指定陣列屬性的一個或所有元素。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-115">You can also specify one or all of the elements of an array property by supplying the array index.</span></span> <span data-ttu-id="d1cd3-116">如需詳細資訊，請參閱 [**ResourceLocator. FragmentPath**](resourcelocator-fragmentpath.md)。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-116">For more information, see [**ResourceLocator.FragmentPath**](resourcelocator-fragmentpath.md).</span></span>
-   <span data-ttu-id="d1cd3-117">加入一個或多個資料來源可能需要用來處理要求的 [*選項*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-117">Add one or more [*options*](windows-remote-management-glossary.md) that a data source may require to process a request.</span></span> <span data-ttu-id="d1cd3-118">如需詳細資訊，請參閱 [**ResourceLocator. AddOption**](resourcelocator-addoption.md)。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-118">For more information, see [**ResourceLocator.AddOption**](resourcelocator-addoption.md).</span></span>

<span data-ttu-id="d1cd3-119">如需詳細資訊，請參閱 [查詢資源的特定實例](querying-for-specific-instances-of-a-resource.md)。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-119">For more information, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

## <a name="members"></a><span data-ttu-id="d1cd3-120">成員</span><span class="sxs-lookup"><span data-stu-id="d1cd3-120">Members</span></span>

<span data-ttu-id="d1cd3-121">**ResourceLocator** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d1cd3-121">The **ResourceLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="d1cd3-122">方法</span><span class="sxs-lookup"><span data-stu-id="d1cd3-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1cd3-123">屬性</span><span class="sxs-lookup"><span data-stu-id="d1cd3-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1cd3-124">方法</span><span class="sxs-lookup"><span data-stu-id="d1cd3-124">Methods</span></span>

<span data-ttu-id="d1cd3-125">**ResourceLocator** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-125">The **ResourceLocator** object has these methods.</span></span>



| <span data-ttu-id="d1cd3-126">方法</span><span class="sxs-lookup"><span data-stu-id="d1cd3-126">Method</span></span>                                                   | <span data-ttu-id="d1cd3-127">描述</span><span class="sxs-lookup"><span data-stu-id="d1cd3-127">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1cd3-128">**AddOption**</span><span class="sxs-lookup"><span data-stu-id="d1cd3-128">**AddOption**</span></span>](resourcelocator-addoption.md)           | <span data-ttu-id="d1cd3-129">新增處理要求所需的其他資料。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-129">Adds additional data required to process the request.</span></span><br/>                                                                   |
| [<span data-ttu-id="d1cd3-130">**AddSelector**</span><span class="sxs-lookup"><span data-stu-id="d1cd3-130">**AddSelector**</span></span>](resourcelocator-addselector.md)       | <span data-ttu-id="d1cd3-131">將 [*選取器*](windows-remote-management-glossary.md) 加入至 **ResourceLocator** 物件。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-131">Adds a [*selector*](windows-remote-management-glossary.md) to the **ResourceLocator** object.</span></span><br/>     |
| [<span data-ttu-id="d1cd3-132">**ClearOptions**</span><span class="sxs-lookup"><span data-stu-id="d1cd3-132">**ClearOptions**</span></span>](resourcelocator-clearoptions.md)     | <span data-ttu-id="d1cd3-133">從 **ResourceLocator** 物件移除任何 [*選項*](windows-remote-management-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-133">Removes any [*options*](windows-remote-management-glossary.md) from the **ResourceLocator** object.</span></span><br/> |
| [<span data-ttu-id="d1cd3-134">**ClearSelectors**</span><span class="sxs-lookup"><span data-stu-id="d1cd3-134">**ClearSelectors**</span></span>](resourcelocator-clearselectors.md) | <span data-ttu-id="d1cd3-135">從 **ResourceLocator** 物件移除所有選取器。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-135">Removes all the selectors from a **ResourceLocator** object.</span></span><br/>                                                            |



 

### <a name="properties"></a><span data-ttu-id="d1cd3-136">屬性</span><span class="sxs-lookup"><span data-stu-id="d1cd3-136">Properties</span></span>

<span data-ttu-id="d1cd3-137">**ResourceLocator** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-137">The **ResourceLocator** object has these properties.</span></span>



| <span data-ttu-id="d1cd3-138">屬性</span><span class="sxs-lookup"><span data-stu-id="d1cd3-138">Property</span></span>                                                                          | <span data-ttu-id="d1cd3-139">存取類型</span><span class="sxs-lookup"><span data-stu-id="d1cd3-139">Access type</span></span>           | <span data-ttu-id="d1cd3-140">Description</span><span class="sxs-lookup"><span data-stu-id="d1cd3-140">Description</span></span>                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1cd3-141">**FragmentDialect**</span><span class="sxs-lookup"><span data-stu-id="d1cd3-141">**FragmentDialect**</span></span>](resourcelocator-fragmentdialect.md)<br/>             | <span data-ttu-id="d1cd3-142">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d1cd3-142">Read/write</span></span><br/> | <span data-ttu-id="d1cd3-143">取得或設定 [*資源*](windows-remote-management-glossary.md)[*片段*](windows-remote-management-glossary.md)的語言方言。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-143">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md).</span></span><br/> |
| [<span data-ttu-id="d1cd3-144">**FragmentPath**</span><span class="sxs-lookup"><span data-stu-id="d1cd3-144">**FragmentPath**</span></span>](resourcelocator-fragmentpath.md)<br/>                   | <span data-ttu-id="d1cd3-145">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d1cd3-145">Read/write</span></span><br/> | <span data-ttu-id="d1cd3-146">取得或設定 [*資源*](windows-remote-management-glossary.md)[*片段*](windows-remote-management-glossary.md)或屬性的路徑。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-146">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property.</span></span><br/> |
| [<span data-ttu-id="d1cd3-147">**MustUnderstandOptions**</span><span class="sxs-lookup"><span data-stu-id="d1cd3-147">**MustUnderstandOptions**</span></span>](resourcelocator-mustunderstandoptions.md)<br/> | <span data-ttu-id="d1cd3-148">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d1cd3-148">Read/write</span></span><br/> | <span data-ttu-id="d1cd3-149">取得或設定 **ResourceLocator** 物件的 **MustUnderstandOptions** 值。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-149">Gets or sets the **MustUnderstandOptions** value for the **ResourceLocator** object.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="d1cd3-150">**ResourceURI**</span><span class="sxs-lookup"><span data-stu-id="d1cd3-150">**ResourceURI**</span></span>](resourcelocator-resourceuri.md)<br/>                     | <span data-ttu-id="d1cd3-151">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d1cd3-151">Read/write</span></span><br/> | <span data-ttu-id="d1cd3-152">取得或設定 **ResourceLocator** 物件中的 [*資源 URI*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-152">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a **ResourceLocator** object.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="d1cd3-153">備註</span><span class="sxs-lookup"><span data-stu-id="d1cd3-153">Remarks</span></span>

<span data-ttu-id="d1cd3-154">**ResourceLocator** 物件會對應至 **IWSManResourceLocator** 介面。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-154">The **ResourceLocator** object corresponds to the **IWSManResourceLocator** interface.</span></span>

## <a name="examples"></a><span data-ttu-id="d1cd3-155">範例</span><span class="sxs-lookup"><span data-stu-id="d1cd3-155">Examples</span></span>

<span data-ttu-id="d1cd3-156">下列 VBScript 程式碼範例會從特定的 [**Win32 \_ 處理器**](/windows/desktop/CIMWin32Prov/win32-processor)實例取得 **NumberOfLogicalProcessors** 和 **NumberOfCores** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d1cd3-156">The following VBScript code example obtains the **NumberOfLogicalProcessors** and **NumberOfCores** properties from a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************

Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" )    
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile )           
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d1cd3-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1cd3-157">Requirements</span></span>



| <span data-ttu-id="d1cd3-158">需求</span><span class="sxs-lookup"><span data-stu-id="d1cd3-158">Requirement</span></span> | <span data-ttu-id="d1cd3-159">值</span><span class="sxs-lookup"><span data-stu-id="d1cd3-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cd3-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1cd3-160">Minimum supported client</span></span><br/> | <span data-ttu-id="d1cd3-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1cd3-161">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d1cd3-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1cd3-162">Minimum supported server</span></span><br/> | <span data-ttu-id="d1cd3-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1cd3-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d1cd3-164">標頭</span><span class="sxs-lookup"><span data-stu-id="d1cd3-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1cd3-165"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1cd3-165"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1cd3-166">Idl</span><span class="sxs-lookup"><span data-stu-id="d1cd3-166">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1cd3-167"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1cd3-167"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d1cd3-168">程式庫</span><span class="sxs-lookup"><span data-stu-id="d1cd3-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1cd3-169"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1cd3-169"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1cd3-170">DLL</span><span class="sxs-lookup"><span data-stu-id="d1cd3-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1cd3-171"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1cd3-171"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d1cd3-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1cd3-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1cd3-173">WinRM 腳本 API</span><span class="sxs-lookup"><span data-stu-id="d1cd3-173">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> </dl>

 

