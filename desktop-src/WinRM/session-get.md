---
title: Session (WSManDisp) 的 Get 方法
description: 抓取 URI 所指定的資源，並傳回目前資源實例的 XML 標記法。
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Get 方法 Windows 遠端管理
- Get 方法 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，Get 方法
topic_type:
- apiref
api_name:
- Session.Get
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4ee84cc711db312389151d1dd95fb890474dcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317384"
---
# <a name="sessionget-method"></a><span data-ttu-id="50697-106">Session. Get 方法</span><span class="sxs-lookup"><span data-stu-id="50697-106">Session.Get method</span></span>

<span data-ttu-id="50697-107">抓取 [*URI*](windows-remote-management-glossary.md) 所指定的資源，並傳回目前資源實例的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="50697-107">Retrieves the resource specified by the [*URI*](windows-remote-management-glossary.md) and returns an XML representation of the current instance of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="50697-108">語法</span><span class="sxs-lookup"><span data-stu-id="50697-108">Syntax</span></span>


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="50697-109">參數</span><span class="sxs-lookup"><span data-stu-id="50697-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50697-110">*resourceUri* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50697-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50697-111">要抓取之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="50697-111">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="50697-112">此參數可包含下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="50697-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="50697-113">具有或不含 [*選取器*](windows-remote-management-glossary.md)的 URI。</span><span class="sxs-lookup"><span data-stu-id="50697-113">A URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="50697-114">使用選取器來呼叫 **Get** 方法以取得 WMI 資源時，請使用物件的索引鍵屬性或屬性。</span><span class="sxs-lookup"><span data-stu-id="50697-114">When calling the **Get** method with a selector to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="50697-115">例如，在下列 Visual Basic Scripting Edition 中 (VBScript) 程式碼範例，則是由指定索引鍵 `Win32_Service?Name=winmgmt` 。</span><span class="sxs-lookup"><span data-stu-id="50697-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span> <span data-ttu-id="50697-116">針對單一類別（例如 [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)），您無法使用選取器。</span><span class="sxs-lookup"><span data-stu-id="50697-116">For singleton classes, such as [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), you cannot use a selector.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   <span data-ttu-id="50697-117">可能包含選取器、[*片段*](windows-remote-management-glossary.md)或 [*選項*](windows-remote-management-glossary.md)的 [**ResourceLocator**](resourcelocator.md)物件。</span><span class="sxs-lookup"><span data-stu-id="50697-117">A [**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="50697-118">[*Ws-addressing*](windows-remote-management-glossary.md)端點參考，如 WS-Management 通訊協定標準中所述。</span><span class="sxs-lookup"><span data-stu-id="50697-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="50697-119">如需 [WS-Management 通訊協定](ws-management-protocol.md)公用規格的詳細資訊，請參閱 [管理規格索引頁面](/previous-versions/dotnet/articles/ms951267(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="50697-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="50697-120">*旗標* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="50697-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50697-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="50697-121">Reserved.</span></span> <span data-ttu-id="50697-122">必須設定為 0。</span><span class="sxs-lookup"><span data-stu-id="50697-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50697-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="50697-123">Return value</span></span>

<span data-ttu-id="50697-124">資源的 XML 表示。</span><span class="sxs-lookup"><span data-stu-id="50697-124">An XML representation of the resource.</span></span>

## <a name="examples"></a><span data-ttu-id="50697-125">範例</span><span class="sxs-lookup"><span data-stu-id="50697-125">Examples</span></span>

<span data-ttu-id="50697-126">下列 VBScript 程式碼範例會抓取代表本機電腦上 WMI Winmgmt 服務之 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 實例的 XML 標記法。</span><span class="sxs-lookup"><span data-stu-id="50697-126">The following VBScript code example retrieves the XML representation of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) instance that represents the WMI Winmgmt service on the local computer.</span></span>


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


strResourceUri = "http://schemas.microsoft.com/" _ 
    & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub

```



<span data-ttu-id="50697-127">下列 VBScript 程式碼範例會從遠端電腦抓取 WMI Winmgmt 服務實例。</span><span class="sxs-lookup"><span data-stu-id="50697-127">The following VBScript code example retrieves the WMI Winmgmt service instance from a remote computer.</span></span> <span data-ttu-id="50697-128">遠端電腦是以完整功能變數名稱 (servername.domain.com) 來識別。</span><span class="sxs-lookup"><span data-stu-id="50697-128">The remote computer is identified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="50697-129">本機和遠端版本之間唯一的差異是 [**CreateSession**](wsman-createsession.md)呼叫中的遠端電腦規格。</span><span class="sxs-lookup"><span data-stu-id="50697-129">The only difference between the local and remote version is the specification of the remote computer in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Dim objSession
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/" _ 
    & "Win32_Service?Name=winmgmt"


On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub
```



## <a name="requirements"></a><span data-ttu-id="50697-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="50697-130">Requirements</span></span>



| <span data-ttu-id="50697-131">需求</span><span class="sxs-lookup"><span data-stu-id="50697-131">Requirement</span></span> | <span data-ttu-id="50697-132">值</span><span class="sxs-lookup"><span data-stu-id="50697-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50697-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50697-133">Minimum supported client</span></span><br/> | <span data-ttu-id="50697-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50697-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="50697-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50697-135">Minimum supported server</span></span><br/> | <span data-ttu-id="50697-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50697-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="50697-137">標頭</span><span class="sxs-lookup"><span data-stu-id="50697-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="50697-138"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="50697-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="50697-139">Idl</span><span class="sxs-lookup"><span data-stu-id="50697-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50697-140"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="50697-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="50697-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="50697-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="50697-142"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="50697-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="50697-143">DLL</span><span class="sxs-lookup"><span data-stu-id="50697-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50697-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50697-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50697-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50697-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50697-146">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="50697-146">**Session**</span></span>](session.md)
</dt> </dl>

 

