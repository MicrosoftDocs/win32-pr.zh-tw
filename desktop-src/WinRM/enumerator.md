---
title: '列舉值物件 (WSManDisp) '
description: 表示從作業傳回的結果資料流程，例如提取作業。
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- 列舉值物件 Windows 遠端管理
- 列舉值物件 Windows 遠端管理，描述
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025414"
---
# <a name="enumerator-object"></a><span data-ttu-id="306ed-105">Enumerator 物件</span><span class="sxs-lookup"><span data-stu-id="306ed-105">Enumerator object</span></span>

<span data-ttu-id="306ed-106">表示從作業傳回的結果資料流程，例如提取作業。</span><span class="sxs-lookup"><span data-stu-id="306ed-106">Represents a stream of results returned from operations, such as a Pull operation.</span></span> <span data-ttu-id="306ed-107">例如， [**Session 列舉**](session-enumerate.md) 方法會傳回多個結果。</span><span class="sxs-lookup"><span data-stu-id="306ed-107">For example, the [**Session.Enumerate**](session-enumerate.md) method returns multiple results.</span></span>

## <a name="members"></a><span data-ttu-id="306ed-108">成員</span><span class="sxs-lookup"><span data-stu-id="306ed-108">Members</span></span>

<span data-ttu-id="306ed-109">**列舉** 值物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="306ed-109">The **Enumerator** object has these types of members:</span></span>

-   [<span data-ttu-id="306ed-110">方法</span><span class="sxs-lookup"><span data-stu-id="306ed-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="306ed-111">屬性</span><span class="sxs-lookup"><span data-stu-id="306ed-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="306ed-112">方法</span><span class="sxs-lookup"><span data-stu-id="306ed-112">Methods</span></span>

<span data-ttu-id="306ed-113">**列舉** 值物件具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="306ed-113">The **Enumerator** object has these methods.</span></span>



| <span data-ttu-id="306ed-114">方法</span><span class="sxs-lookup"><span data-stu-id="306ed-114">Method</span></span>                                  | <span data-ttu-id="306ed-115">描述</span><span class="sxs-lookup"><span data-stu-id="306ed-115">Description</span></span>                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="306ed-116">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="306ed-116">**ReadItem**</span></span>](enumerator-readitem.md) | <span data-ttu-id="306ed-117">從資源抓取專案，並傳回專案的 XML 表示。</span><span class="sxs-lookup"><span data-stu-id="306ed-117">Retrieves an item from the resource and returns an XML representation of the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="306ed-118">屬性</span><span class="sxs-lookup"><span data-stu-id="306ed-118">Properties</span></span>

<span data-ttu-id="306ed-119">**列舉** 值物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="306ed-119">The **Enumerator** object has these properties.</span></span>



| <span data-ttu-id="306ed-120">屬性</span><span class="sxs-lookup"><span data-stu-id="306ed-120">Property</span></span>                                                     | <span data-ttu-id="306ed-121">描述</span><span class="sxs-lookup"><span data-stu-id="306ed-121">Description</span></span>                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="306ed-122">**AtEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="306ed-122">**AtEndOfStream**</span></span>](enumerator-atendofstream.md)<br/> | <span data-ttu-id="306ed-123">取得布林值，指出集合中是否有更多專案。</span><span class="sxs-lookup"><span data-stu-id="306ed-123">Gets a Boolean value that indicates whether there are more items in the collection.</span></span><br/> |
| [<span data-ttu-id="306ed-124">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="306ed-124">**Error**</span></span>](enumerator-error.md)<br/>                 | <span data-ttu-id="306ed-125">取得其他錯誤資訊的 XML 表示。</span><span class="sxs-lookup"><span data-stu-id="306ed-125">Gets an XML representation of additional error information.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="306ed-126">備註</span><span class="sxs-lookup"><span data-stu-id="306ed-126">Remarks</span></span>

<span data-ttu-id="306ed-127">若要啟動列舉，請使用 [**Session. 列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="306ed-127">To start an enumeration, use [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="306ed-128">若要執行 [*WS-列舉：*](windows-remote-management-glossary.md)繼續讀取列舉中專案的 [*提取*](windows-remote-management-glossary.md)作業，請使用 [**ReadItem**](enumerator-readitem.md)。</span><span class="sxs-lookup"><span data-stu-id="306ed-128">To do a [*WS-Enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) operation that continues reading items in the enumeration, use [**Enumerator.ReadItem**](enumerator-readitem.md).</span></span>

<span data-ttu-id="306ed-129">**列舉** 值物件會對應至 [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)介面。</span><span class="sxs-lookup"><span data-stu-id="306ed-129">The **Enumerator** object corresponds to the [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="306ed-130">範例</span><span class="sxs-lookup"><span data-stu-id="306ed-130">Examples</span></span>

<span data-ttu-id="306ed-131">下列 VBScript 程式碼範例會列舉 (servername.domain.com) 的完整功能變數名稱所指定的遠端電腦上的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="306ed-131">The following VBScript code example enumerates all the disks on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="306ed-132">DisplayOutput 副程式會以和 WinRM 工具相同的方式來格式化資料輸出。</span><span class="sxs-lookup"><span data-stu-id="306ed-132">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


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



## <a name="requirements"></a><span data-ttu-id="306ed-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="306ed-133">Requirements</span></span>



| <span data-ttu-id="306ed-134">需求</span><span class="sxs-lookup"><span data-stu-id="306ed-134">Requirement</span></span> | <span data-ttu-id="306ed-135">值</span><span class="sxs-lookup"><span data-stu-id="306ed-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="306ed-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="306ed-136">Minimum supported client</span></span><br/> | <span data-ttu-id="306ed-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="306ed-137">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="306ed-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="306ed-138">Minimum supported server</span></span><br/> | <span data-ttu-id="306ed-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="306ed-139">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="306ed-140">標頭</span><span class="sxs-lookup"><span data-stu-id="306ed-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="306ed-141"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="306ed-141"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="306ed-142">Idl</span><span class="sxs-lookup"><span data-stu-id="306ed-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="306ed-143"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="306ed-143"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="306ed-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="306ed-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="306ed-145"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="306ed-145"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="306ed-146">DLL</span><span class="sxs-lookup"><span data-stu-id="306ed-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="306ed-147"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="306ed-147"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="306ed-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="306ed-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="306ed-149">WinRM 腳本 API</span><span class="sxs-lookup"><span data-stu-id="306ed-149">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="306ed-150">列舉或列出資源的所有實例</span><span class="sxs-lookup"><span data-stu-id="306ed-150">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="306ed-151">Windows 遠端管理中的腳本</span><span class="sxs-lookup"><span data-stu-id="306ed-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





