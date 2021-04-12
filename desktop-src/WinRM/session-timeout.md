---
title: 'Session. Timeout 屬性 (WSManDisp .h) '
description: 設定並取得用戶端應用程式等候 Windows 遠端管理完成其作業的最大時間量（以毫秒為單位）。
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Timeout 屬性 Windows 遠端管理
- Timeout 屬性 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，Timeout 屬性
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c28b5284d9061e1c80fb3c66193d394c347a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317520"
---
# <a name="sessiontimeout-property"></a><span data-ttu-id="bbf1b-106">Session. Timeout 屬性</span><span class="sxs-lookup"><span data-stu-id="bbf1b-106">Session.Timeout property</span></span>

<span data-ttu-id="bbf1b-107">設定並取得用戶端應用程式等候 Windows 遠端管理完成其作業的最大時間量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="bbf1b-107">Sets and gets the maximum amount of time, in milliseconds, that the client application waits for Windows Remote Management to complete its operations.</span></span>

<span data-ttu-id="bbf1b-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bbf1b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbf1b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbf1b-109">Syntax</span></span>


```VB
Session.Timeout As long
```



## <a name="property-value"></a><span data-ttu-id="bbf1b-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="bbf1b-110">Property value</span></span>

<span data-ttu-id="bbf1b-111">超時值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="bbf1b-111">Time-out value, in milliseconds.</span></span> <span data-ttu-id="bbf1b-112">當超過超時值時，就會發生執行階段錯誤。</span><span class="sxs-lookup"><span data-stu-id="bbf1b-112">When the time-out value is exceeded, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf1b-113">備註</span><span class="sxs-lookup"><span data-stu-id="bbf1b-113">Remarks</span></span>

<span data-ttu-id="bbf1b-114">您可以在代理程式執行的每個作業之前設定超時值。</span><span class="sxs-lookup"><span data-stu-id="bbf1b-114">The time-out value can be set before each operation performed by the agent.</span></span> <span data-ttu-id="bbf1b-115">如果未指定超時值，代理程式會設定超時值。</span><span class="sxs-lookup"><span data-stu-id="bbf1b-115">If a time-out value is not specified, the agent sets the time-out value.</span></span>

<span data-ttu-id="bbf1b-116">在列舉作業期間，當列舉資源時，無法重設超時值。</span><span class="sxs-lookup"><span data-stu-id="bbf1b-116">During an enumerate operation, the time-out value cannot be reset while the resource is being enumerated.</span></span>

## <a name="examples"></a><span data-ttu-id="bbf1b-117">範例</span><span class="sxs-lookup"><span data-stu-id="bbf1b-117">Examples</span></span>

<span data-ttu-id="bbf1b-118">下列 VBScript 程式碼範例會使用 WMI [**Win32 \_ process**](/windows/desktop/CIMWin32Prov/win32-process)類別的 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法來啟動 Calc.exe 進程。</span><span class="sxs-lookup"><span data-stu-id="bbf1b-118">The following VBScript code example starts a Calc.exe process using the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span> <span data-ttu-id="bbf1b-119">*StrInputParameters* 參數包含 XML 格式的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="bbf1b-119">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="bbf1b-120">腳本會指定會話的超時時間。</span><span class="sxs-lookup"><span data-stu-id="bbf1b-120">The script specifies a time-out for the session.</span></span>


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

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

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



## <a name="requirements"></a><span data-ttu-id="bbf1b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbf1b-121">Requirements</span></span>



| <span data-ttu-id="bbf1b-122">需求</span><span class="sxs-lookup"><span data-stu-id="bbf1b-122">Requirement</span></span> | <span data-ttu-id="bbf1b-123">值</span><span class="sxs-lookup"><span data-stu-id="bbf1b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf1b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbf1b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf1b-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbf1b-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="bbf1b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbf1b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf1b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbf1b-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bbf1b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="bbf1b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbf1b-129"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="bbf1b-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbf1b-130">Idl</span><span class="sxs-lookup"><span data-stu-id="bbf1b-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bbf1b-131"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bbf1b-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="bbf1b-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="bbf1b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="bbf1b-133"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bbf1b-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bbf1b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bbf1b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbf1b-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbf1b-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bbf1b-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbf1b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf1b-137">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="bbf1b-137">**Session**</span></span>](session.md)
</dt> </dl>

 

