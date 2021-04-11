---
title: Session (WSManDisp) 的 Put 方法
description: 更新資源。
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Put 方法 Windows 遠端管理
- Put 方法 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，Put 方法
topic_type:
- apiref
api_name:
- Session.Put
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0f09b0a0f8de4e7f7d06cb84753e6b708841f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384949"
---
# <a name="sessionput-method"></a><span data-ttu-id="9b55e-106">Session. Put 方法</span><span class="sxs-lookup"><span data-stu-id="9b55e-106">Session.Put method</span></span>

<span data-ttu-id="9b55e-107">更新資源。</span><span class="sxs-lookup"><span data-stu-id="9b55e-107">Updates a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b55e-108">語法</span><span class="sxs-lookup"><span data-stu-id="9b55e-108">Syntax</span></span>


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9b55e-109">參數</span><span class="sxs-lookup"><span data-stu-id="9b55e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b55e-110">*resourceUri* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b55e-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b55e-111">要更新之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b55e-111">The identifier of the resource to be updated.</span></span>

<span data-ttu-id="9b55e-112">此參數可包含下列清單中包含的其中一個元素：</span><span class="sxs-lookup"><span data-stu-id="9b55e-112">This parameter can contain one of elements contained in the following list:</span></span>

-   <span data-ttu-id="9b55e-113">具有或不含 [*選取器*](windows-remote-management-glossary.md)的 URI。</span><span class="sxs-lookup"><span data-stu-id="9b55e-113">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="9b55e-114">當呼叫 **Put** 方法來取得 WMI 資源時，請使用物件的索引鍵屬性（property）或屬性（property）。</span><span class="sxs-lookup"><span data-stu-id="9b55e-114">When calling the **Put** method to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="9b55e-115">例如，在下列 Visual Basic Scripting Edition 中 (VBScript) 程式碼範例，則是由指定索引鍵 `Win32_Service?Name=winmgmt` 。</span><span class="sxs-lookup"><span data-stu-id="9b55e-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="9b55e-116">可能包含選取器、[*片段*](windows-remote-management-glossary.md)或 [*選項*](windows-remote-management-glossary.md)的 [**ResourceLocator**](resourcelocator.md)物件。</span><span class="sxs-lookup"><span data-stu-id="9b55e-116">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="9b55e-117">[*Ws-addressing*](windows-remote-management-glossary.md) 端點參考，如 [WS-Management 通訊協定](ws-management-protocol.md) standard 所述。</span><span class="sxs-lookup"><span data-stu-id="9b55e-117">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="9b55e-118">如需 WS-Management 通訊協定之公用規格的詳細資訊，請參閱 [管理規格索引頁面](/previous-versions/dotnet/articles/ms951267(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="9b55e-118">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="9b55e-119">*資源* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b55e-119">*resource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b55e-120">更新的資源內容。</span><span class="sxs-lookup"><span data-stu-id="9b55e-120">The updated resource content.</span></span>

</dd> <dt>

<span data-ttu-id="9b55e-121">*旗標* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9b55e-121">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b55e-122">保留的。</span><span class="sxs-lookup"><span data-stu-id="9b55e-122">Reserved.</span></span> <span data-ttu-id="9b55e-123">必須設定為 0。</span><span class="sxs-lookup"><span data-stu-id="9b55e-123">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b55e-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b55e-124">Return value</span></span>

<span data-ttu-id="9b55e-125">包含已更新資源內容的 XML。</span><span class="sxs-lookup"><span data-stu-id="9b55e-125">The XML that contains the updated resource content.</span></span>

## <a name="examples"></a><span data-ttu-id="9b55e-126">範例</span><span class="sxs-lookup"><span data-stu-id="9b55e-126">Examples</span></span>

<span data-ttu-id="9b55e-127">下列 VBScript 程式碼範例會將資料寫入 [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) 物件。</span><span class="sxs-lookup"><span data-stu-id="9b55e-127">The following VBScript code example writes data to the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) object.</span></span> <span data-ttu-id="9b55e-128">您必須在 *資源* 參數的 XML 中包含物件的所有非陣列屬性。</span><span class="sxs-lookup"><span data-stu-id="9b55e-128">You must include all non-array properties of the object in the XML of the *Resource* parameter.</span></span> <span data-ttu-id="9b55e-129">屬性的順序並不重要。</span><span class="sxs-lookup"><span data-stu-id="9b55e-129">The order of the properties is not significant.</span></span>


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

'Change the property value by putting
'the new XML content into the resource.
Dim strResourceUri, strReturnedResourceUri, newXmlContent
strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
  & "wmi/root/cimv2/Win32_WMISetting"
newXmlContent = _
  "<p:Win32_WMISetting xmlns:p=""http://schemas.microsoft.com/" & _
  "wbem/wsman/1/wmi/root/cimv2/Win32_WMISetting"">" & _
  "<p:LoggingLevel>2</p:LoggingLevel></p:Win32_WMISetting>" 

On Error Resume Next
strReturnedResourceUri = objSession.Put(reourceUri, newXmlContent)
WScript.Echo "Returned resource Uri:" & Chr(10) & _
  strReturnedResourceUri
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



## <a name="requirements"></a><span data-ttu-id="9b55e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b55e-130">Requirements</span></span>



| <span data-ttu-id="9b55e-131">需求</span><span class="sxs-lookup"><span data-stu-id="9b55e-131">Requirement</span></span> | <span data-ttu-id="9b55e-132">值</span><span class="sxs-lookup"><span data-stu-id="9b55e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b55e-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b55e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9b55e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b55e-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9b55e-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b55e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9b55e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b55e-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9b55e-137">標頭</span><span class="sxs-lookup"><span data-stu-id="9b55e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b55e-138"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b55e-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b55e-139">Idl</span><span class="sxs-lookup"><span data-stu-id="9b55e-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9b55e-140"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9b55e-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9b55e-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="9b55e-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b55e-142"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9b55e-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9b55e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9b55e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b55e-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b55e-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b55e-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b55e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b55e-146">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="9b55e-146">**Session**</span></span>](session.md)
</dt> </dl>

 

