---
title: Session (WSManDisp) 的列舉方法
description: 列舉資料表、資料收集或記錄資源。
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- 列舉方法 Windows 遠端管理
- 列舉方法 Windows 遠端管理，會話物件
- Session 物件 Windows 遠端管理，列舉方法
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca6b66b910251c641832cde3ddd93d6479f66be7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024867"
---
# <a name="sessionenumerate-method"></a><span data-ttu-id="35a1f-106">Session. 列舉方法</span><span class="sxs-lookup"><span data-stu-id="35a1f-106">Session.Enumerate method</span></span>

<span data-ttu-id="35a1f-107">列舉資料表、資料收集或記錄資源。</span><span class="sxs-lookup"><span data-stu-id="35a1f-107">Enumerates a table, data collection, or log resource.</span></span> <span data-ttu-id="35a1f-108">若要建立查詢，請在列舉中包含 *篩選* 參數和 *方言* 參數。</span><span class="sxs-lookup"><span data-stu-id="35a1f-108">To create a query, include a *filter* parameter and a *dialect* parameter in an enumeration.</span></span> <span data-ttu-id="35a1f-109">您也可以使用 [**ResourceLocator**](resourcelocator.md) 物件來建立查詢。</span><span class="sxs-lookup"><span data-stu-id="35a1f-109">You can also use a [**ResourceLocator**](resourcelocator.md) object to create queries.</span></span> <span data-ttu-id="35a1f-110">如需詳細資訊，請參閱 [列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)。</span><span class="sxs-lookup"><span data-stu-id="35a1f-110">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="35a1f-111">語法</span><span class="sxs-lookup"><span data-stu-id="35a1f-111">Syntax</span></span>


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="35a1f-112">參數</span><span class="sxs-lookup"><span data-stu-id="35a1f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a1f-113">*resourceUri* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35a1f-113">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a1f-114">要抓取之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="35a1f-114">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="35a1f-115">此參數可包含下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="35a1f-115">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="35a1f-116">資源的 URI。</span><span class="sxs-lookup"><span data-stu-id="35a1f-116">The URI of the resource.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   <span data-ttu-id="35a1f-117">[**ResourceLocator**](resourcelocator.md)物件。</span><span class="sxs-lookup"><span data-stu-id="35a1f-117">A [**ResourceLocator**](resourcelocator.md) object.</span></span>
-   <span data-ttu-id="35a1f-118">[*Ws-addressing*](windows-remote-management-glossary.md)端點參考，如 WS-Management 通訊協定標準中所述。</span><span class="sxs-lookup"><span data-stu-id="35a1f-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="35a1f-119">如需 [WS-Management 通訊協定](ws-management-protocol.md)公用規格的詳細資訊，請參閱 [管理規格索引頁面](/previous-versions/dotnet/articles/ms951267(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="35a1f-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="35a1f-120">*篩選* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="35a1f-120">*filter* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35a1f-121">定義列舉傳回資源中專案的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="35a1f-121">A filter that defines what items in the resource are returned by the enumeration.</span></span> <span data-ttu-id="35a1f-122">列舉資源時，只會傳回符合篩選準則的專案。</span><span class="sxs-lookup"><span data-stu-id="35a1f-122">When the resource is enumerated, only those items that match the filter criteria are returned.</span></span> <span data-ttu-id="35a1f-123">在列舉中包含 *篩選* 參數和 *方言* 參數，會將列舉轉換成查詢。</span><span class="sxs-lookup"><span data-stu-id="35a1f-123">Including a *filter* parameter and a *dialect* parameter in an enumeration converts the enumeration into a query.</span></span> <span data-ttu-id="35a1f-124">如需範例，請參閱 [查詢資源的特定實例](querying-for-specific-instances-of-a-resource.md)。</span><span class="sxs-lookup"><span data-stu-id="35a1f-124">For an example, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

<span data-ttu-id="35a1f-125">如果您有 *resourceURI* 參數的 [**ResourceLocator**](resourcelocator.md)物件，則不應使用此參數。</span><span class="sxs-lookup"><span data-stu-id="35a1f-125">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="35a1f-126">*方言* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="35a1f-126">*dialect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35a1f-127">篩選所使用的語言。</span><span class="sxs-lookup"><span data-stu-id="35a1f-127">The language used by the filter.</span></span> <span data-ttu-id="35a1f-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi)（WMI 所使用的 SQL 子集）是唯一支援的語言。</span><span class="sxs-lookup"><span data-stu-id="35a1f-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), a subset of SQL used by WMI, is the only language supported.</span></span>

<span data-ttu-id="35a1f-129">如果您有 *resourceURI* 參數的 [**ResourceLocator**](resourcelocator.md)物件，則不應使用此參數。</span><span class="sxs-lookup"><span data-stu-id="35a1f-129">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="35a1f-130">*旗標* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="35a1f-130">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35a1f-131">必須在 **\_ \_ WSManEnumFlags** 列舉中包含旗標的參數。</span><span class="sxs-lookup"><span data-stu-id="35a1f-131">A parameter that must contain a flag in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="35a1f-132">如需詳細資訊，請參閱 [列舉常數](enumeration-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="35a1f-132">For more information, see [Enumeration Constants](enumeration-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a1f-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="35a1f-133">Return value</span></span>

<span data-ttu-id="35a1f-134">列舉 [**值物件，**](enumerator.md) 包含列舉的結果。</span><span class="sxs-lookup"><span data-stu-id="35a1f-134">An [**Enumerator**](enumerator.md) object that contains the results of the enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a1f-135">備註</span><span class="sxs-lookup"><span data-stu-id="35a1f-135">Remarks</span></span>

<span data-ttu-id="35a1f-136">如需有關在列舉期間限制網路呼叫的詳細資訊，請參閱 [**BatchItems**](session-batchitems.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="35a1f-136">For more information about limiting network calls during an enumeration, see the [**BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="35a1f-137">請注意，如果旗標包含 [**列舉常數**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** 或 **WSManFlagHierarchyShallow** ，則 Windows 遠端管理服務會傳回 **\_ \_ \_ \_ 不支援** 的錯誤錯誤碼錯誤的 WSMAN 多型模式。</span><span class="sxs-lookup"><span data-stu-id="35a1f-137">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then Windows Remote Management service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

<span data-ttu-id="35a1f-138">如果指定了篩選，則它必須是與資源架構相關的有效檔。</span><span class="sxs-lookup"><span data-stu-id="35a1f-138">If a filter is specified, it must be a valid document with respect to the schema of the resource.</span></span> <span data-ttu-id="35a1f-139">方言參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="35a1f-139">The dialect parameter is optional.</span></span> <span data-ttu-id="35a1f-140">但是，如果篩選字串的開頭是 <，但不是 XML 片段，則請在 *旗標* 參數中包含 *方言* 參數或設定 **WSManFlagNonXmlText** 旗標。</span><span class="sxs-lookup"><span data-stu-id="35a1f-140">However, if the filter string begins with <, but is not an XML fragment, then either include the *dialect* parameter or set the **WSManFlagNonXmlText** flag in the *flags* parameter.</span></span> <span data-ttu-id="35a1f-141">如需詳細資訊，請參閱 [**列舉常數**](enumeration-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="35a1f-141">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

<span data-ttu-id="35a1f-142">對應的 c + + 方法是 [**iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)。</span><span class="sxs-lookup"><span data-stu-id="35a1f-142">The corresponding C++ method is [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

## <a name="examples"></a><span data-ttu-id="35a1f-143">範例</span><span class="sxs-lookup"><span data-stu-id="35a1f-143">Examples</span></span>

<span data-ttu-id="35a1f-144">下列 VBScript 程式碼範例會列舉完整功能變數名稱所指定的遠端電腦上的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例 (servername.domain.com) 。</span><span class="sxs-lookup"><span data-stu-id="35a1f-144">The following VBScript code example enumerates the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instances on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="35a1f-145">請注意，釋出列舉物件會清除暫止的列舉要求。</span><span class="sxs-lookup"><span data-stu-id="35a1f-145">Be aware that freeing the enumeration object clears pending enumeration requests.</span></span> <span data-ttu-id="35a1f-146">DisplayOutput 副程式使用 Winrm 命令列工具 XML 轉換檔 (WsmTxt. xsl) 以表格格式輸出資料。</span><span class="sxs-lookup"><span data-stu-id="35a1f-146">The DisplayOutput subroutine uses the Winrm command-line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

Set objResultSet = objSession.Enumerate( strResource )

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



## <a name="requirements"></a><span data-ttu-id="35a1f-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="35a1f-147">Requirements</span></span>



| <span data-ttu-id="35a1f-148">需求</span><span class="sxs-lookup"><span data-stu-id="35a1f-148">Requirement</span></span> | <span data-ttu-id="35a1f-149">值</span><span class="sxs-lookup"><span data-stu-id="35a1f-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a1f-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35a1f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="35a1f-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35a1f-151">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="35a1f-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35a1f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="35a1f-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35a1f-153">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="35a1f-154">標頭</span><span class="sxs-lookup"><span data-stu-id="35a1f-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="35a1f-155"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="35a1f-155"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="35a1f-156">Idl</span><span class="sxs-lookup"><span data-stu-id="35a1f-156">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35a1f-157"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="35a1f-157"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="35a1f-158">程式庫</span><span class="sxs-lookup"><span data-stu-id="35a1f-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="35a1f-159"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35a1f-159"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35a1f-160">DLL</span><span class="sxs-lookup"><span data-stu-id="35a1f-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35a1f-161"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35a1f-161"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35a1f-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35a1f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a1f-163">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="35a1f-163">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="35a1f-164">查詢資源的特定實例</span><span class="sxs-lookup"><span data-stu-id="35a1f-164">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="35a1f-165">**BatchItems**</span><span class="sxs-lookup"><span data-stu-id="35a1f-165">**BatchItems**</span></span>](session-batchitems.md)
</dt> <dt>

[<span data-ttu-id="35a1f-166">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="35a1f-166">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

