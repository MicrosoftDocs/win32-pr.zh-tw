---
title: 'Session。 Error 屬性 (WSManDisp .h) '
description: 取得 XML 資料流程中的其他錯誤資訊。
ms.assetid: f291c11c-012f-45eb-b851-5661d881ee79
ms.tgt_platform: multiple
keywords:
- Error 屬性 Windows 遠端管理
- Error 屬性 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，Error 屬性
topic_type:
- apiref
api_name:
- Session.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2568fb7f51d6970d3d98f8434357b22efb7793d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106971874"
---
# <a name="sessionerror-property"></a><span data-ttu-id="b7e60-106">Session。 Error 屬性</span><span class="sxs-lookup"><span data-stu-id="b7e60-106">Session.Error property</span></span>

<span data-ttu-id="b7e60-107">取得 XML 資料流程中的其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="b7e60-107">Gets additional error information in an XML stream.</span></span> <span data-ttu-id="b7e60-108">您也可以從 VBScript [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件取得錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="b7e60-108">Error information can also be obtained from the VBScript [Err](/previous-versions//sbf5ze0e(v=vs.85)) object.</span></span>

<span data-ttu-id="b7e60-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b7e60-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e60-110">語法</span><span class="sxs-lookup"><span data-stu-id="b7e60-110">Syntax</span></span>


```VB
Session.Error As BSTR
```



## <a name="property-value"></a><span data-ttu-id="b7e60-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="b7e60-111">Property value</span></span>

<span data-ttu-id="b7e60-112">錯誤資訊的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="b7e60-112">XML representation of error information.</span></span>

## <a name="examples"></a><span data-ttu-id="b7e60-113">範例</span><span class="sxs-lookup"><span data-stu-id="b7e60-113">Examples</span></span>

<span data-ttu-id="b7e60-114">下列 VBScript 程式碼範例顯示在 [*資源 URI*](windows-remote-management-glossary.md)中包含錯誤的腳本。</span><span class="sxs-lookup"><span data-stu-id="b7e60-114">The following VBScript code example shows a script that contains an error in the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="b7e60-115">正確的資源 URI 為 `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_QuotaSetting?VolumePath=c:\\` 。</span><span class="sxs-lookup"><span data-stu-id="b7e60-115">The correct resource URI is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_QuotaSetting?VolumePath=c:\\`.</span></span>


```VB
'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_QuotaSetting"

On Error Resume Next
strResponse = objSession.Get( strResourceUri )
If Err.number <> 0 Then
    DisplayErrorInfo()
    strErrorXML = objSession.Error
    WScript.Echo strErrorXML
Else
    Call DisplayOutput(strResponse)
End If
On Error Goto 0

'*************************************************************
' Displays Error information from Err object and Session.Error
'*************************************************************
Sub DisplayErrorInfo()

    WScript.Echo "An error has occurred."     
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    Err.Clear
End Sub
```



<span data-ttu-id="b7e60-116">以下文字是腳本的錯誤輸出。</span><span class="sxs-lookup"><span data-stu-id="b7e60-116">The following text is the error output from the script.</span></span>

``` syntax
Number      : 0x803380FA
Description : The WinRM client cannot process the request. 
The resource URI is not valid: it does not contain keys, but
the class selected is not a singleton. To access an instance which 
is not a singleton, keys must be provided. Use the following 
command to get more information about how to construct a 
resource URI: "winrm help uris".
Source      : Session
HelpFile    :
HelpContext : 0
<f:WSManFault 
xmlns:f="http://schemas.microsoft.com/wbem/wsman/1/wsmanfault" 
Code="2150859002" Machine="Server1" xml:lang="en-US">
<f:Message>
<f:ProviderFault provider="WMIv1 plugin for Windows Remote Management " 
path="%systemroot%\system32\WsmWmiPl.dll">
<f:WSManFault 
xmlns:f="http://schemas.microsoft.com/wbem/wsman/1/wsmanfault" 
Code="2150859002" Machine="" xml:lang="en-US">
<f:Message>The WinRM client cannot process the request. 
The resource URI is not valid: it does not contain keys, but the 
class selected is not a singleton. To access an instance which is 
not a singleton, keys must be provided. Use the following command 
to get more information in how to construct a resource URI: 
&quot;winrm help uris&quot;. 
</f:Message></f:WSManFault>
</f:ProviderFault>
</f:Message
></f:WSManFault>
```

## <a name="requirements"></a><span data-ttu-id="b7e60-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7e60-117">Requirements</span></span>



| <span data-ttu-id="b7e60-118">需求</span><span class="sxs-lookup"><span data-stu-id="b7e60-118">Requirement</span></span> | <span data-ttu-id="b7e60-119">值</span><span class="sxs-lookup"><span data-stu-id="b7e60-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e60-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7e60-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e60-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7e60-121">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b7e60-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7e60-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e60-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7e60-123">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b7e60-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b7e60-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7e60-125"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e60-125"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7e60-126">Idl</span><span class="sxs-lookup"><span data-stu-id="b7e60-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7e60-127"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7e60-127"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b7e60-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7e60-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7e60-129"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b7e60-129"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b7e60-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b7e60-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7e60-131"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7e60-131"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b7e60-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7e60-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e60-133">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="b7e60-133">**Session**</span></span>](session.md)
</dt> </dl>

 

