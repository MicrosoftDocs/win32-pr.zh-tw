---
title: 'Invoke 方法 (WSManDisp) '
description: 叫用方法並傳回方法呼叫的結果。
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Invoke 方法 Windows 遠端管理
- Invoke 方法 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，Invoke 方法
topic_type:
- apiref
api_name:
- Session.Invoke
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117c688b616f377730524a09234b1dc38a4996c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686338"
---
# <a name="sessioninvoke-method"></a><span data-ttu-id="83906-106">Invoke 方法</span><span class="sxs-lookup"><span data-stu-id="83906-106">Session.Invoke method</span></span>

<span data-ttu-id="83906-107">叫用方法並傳回方法呼叫的結果。</span><span class="sxs-lookup"><span data-stu-id="83906-107">Invokes a method and returns the results of the method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="83906-108">語法</span><span class="sxs-lookup"><span data-stu-id="83906-108">Syntax</span></span>


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="83906-109">參數</span><span class="sxs-lookup"><span data-stu-id="83906-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83906-110">*actionUri* \[在\]</span><span class="sxs-lookup"><span data-stu-id="83906-110">*actionUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83906-111">要叫用之方法的 URI。</span><span class="sxs-lookup"><span data-stu-id="83906-111">The URI of the method to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="83906-112">*resourceUri* \[在\]</span><span class="sxs-lookup"><span data-stu-id="83906-112">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83906-113">要取出的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="83906-113">The identifier of the resource to retrieve.</span></span>

<span data-ttu-id="83906-114">此參數可包含下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="83906-114">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="83906-115">具有或不含 [*選取器*](windows-remote-management-glossary.md)的 URI。</span><span class="sxs-lookup"><span data-stu-id="83906-115">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="83906-116">在下列 Visual Basic Scripting Edition (VBScript) 範例中，是由指定索引鍵 `Win32_Service?Name=winmgmt` 。</span><span class="sxs-lookup"><span data-stu-id="83906-116">In the following Visual Basic Scripting Edition (VBScript) example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="83906-117">可能包含選取器、[*片段*](windows-remote-management-glossary.md)或 [*選項*](windows-remote-management-glossary.md)的 [**ResourceLocator**](resourcelocator.md)物件。</span><span class="sxs-lookup"><span data-stu-id="83906-117">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="83906-118">[*Ws-addressing*](windows-remote-management-glossary.md) 端點參考，如 [WS-Management 通訊協定](ws-management-protocol.md) standard 所述。</span><span class="sxs-lookup"><span data-stu-id="83906-118">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="83906-119">如需 WS-Management 通訊協定之公用規格的詳細資訊，請參閱 [管理規格索引頁面](/previous-versions/dotnet/articles/ms951267(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="83906-119">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="83906-120">*參數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="83906-120">*parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83906-121">方法之輸入的 XML 表示。</span><span class="sxs-lookup"><span data-stu-id="83906-121">The XML representation of the input for the method.</span></span> <span data-ttu-id="83906-122">必須提供這個字串，否則這個方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="83906-122">This string must be supplied or this method will fail.</span></span>

</dd> <dt>

<span data-ttu-id="83906-123">*旗標* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="83906-123">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83906-124">保留的。</span><span class="sxs-lookup"><span data-stu-id="83906-124">Reserved.</span></span> <span data-ttu-id="83906-125">必須設定為 0。</span><span class="sxs-lookup"><span data-stu-id="83906-125">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83906-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="83906-126">Return value</span></span>

<span data-ttu-id="83906-127">方法輸出的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="83906-127">The XML representation of the method output.</span></span>

## <a name="examples"></a><span data-ttu-id="83906-128">範例</span><span class="sxs-lookup"><span data-stu-id="83906-128">Examples</span></span>

<span data-ttu-id="83906-129">下列 VBScript 程式碼範例會啟動 Calc.exe 進程。</span><span class="sxs-lookup"><span data-stu-id="83906-129">The following VBScript code example starts a Calc.exe process.</span></span> <span data-ttu-id="83906-130">*StrInputParameters* 參數包含 XML 格式的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="83906-130">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="83906-131">WMI [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)類別的 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法唯一必要的輸入參數是要執行的命令列。</span><span class="sxs-lookup"><span data-stu-id="83906-131">The only required input parameter for the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is the command line to execute.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
    "wmi/root/cimv2/Win32_Process"

strInputParameters = "<p:Create_INPUT " & _
    "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Process"">" & _
    "<p:CommandLine>" & "calc.exe" & _
    "</p:CommandLine>" & _
    "</p:Create_INPUT>"

strOutputParameters = objSession.Invoke( "Create", _
    strResource, strInputParameters )

DisplayOutput( strOutputParameters )

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



<span data-ttu-id="83906-132">下列 VBScript 程式碼範例會呼叫 **Session （Invoke** ）方法來執行 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)的 [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)方法。</span><span class="sxs-lookup"><span data-stu-id="83906-132">The following VBScript code example calls the **Session.Invoke** method to execute the [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) method of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="83906-133">**StopService** 方法沒有輸入參數。</span><span class="sxs-lookup"><span data-stu-id="83906-133">The **StopService** method does not have input parameters.</span></span> <span data-ttu-id="83906-134">不過， **Invoke** 方法需要 *parameters* 參數中的 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="83906-134">However, the **Invoke** method requires an XML string in the *parameters* parameter.</span></span>


```VB
Option Explicit

Dim objWsman
Dim objSession
Dim strResponse
Dim strActionURI
Dim strInputXml
Dim strResourceURI
Dim strMethodName

set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession
strResourceURI = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=w32time"
strMethodName = "StopService"
strActionURI = strMethodName                                      

strInputXml = "<p:StopService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"

strResponse = objSession.Invoke(strMethodName, strResourceURI, strInputXml)

call DisplayOutput(strResponse)
 
strMethodName = "StartService" 
strActionURI = strResourceURI & "/" & strMethodName  
strInputXml = "<p:StartService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"
strResponse = objSession.Invoke(strMethodName, _
    strResourceURI, strInputXml)

call DisplayOutput(strResponse)

 
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



## <a name="requirements"></a><span data-ttu-id="83906-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="83906-135">Requirements</span></span>



| <span data-ttu-id="83906-136">需求</span><span class="sxs-lookup"><span data-stu-id="83906-136">Requirement</span></span> | <span data-ttu-id="83906-137">值</span><span class="sxs-lookup"><span data-stu-id="83906-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="83906-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83906-138">Minimum supported client</span></span><br/> | <span data-ttu-id="83906-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83906-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="83906-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83906-140">Minimum supported server</span></span><br/> | <span data-ttu-id="83906-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83906-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="83906-142">標頭</span><span class="sxs-lookup"><span data-stu-id="83906-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="83906-143"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="83906-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="83906-144">Idl</span><span class="sxs-lookup"><span data-stu-id="83906-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="83906-145"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="83906-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="83906-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="83906-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="83906-147"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="83906-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="83906-148">DLL</span><span class="sxs-lookup"><span data-stu-id="83906-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83906-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83906-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83906-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83906-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83906-151">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="83906-151">**Session**</span></span>](session.md)
</dt> </dl>

 

