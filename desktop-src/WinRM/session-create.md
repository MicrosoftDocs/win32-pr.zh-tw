---
title: Session (WSManDisp) 的 Create 方法
description: 建立資源的新實例，並傳回新物件 (EPR) 的端點參考。
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- 建立方法 Windows 遠端管理
- Create method Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，Create 方法
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eacdbdffb9e2dac219e3922cabfc5615de34e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465953"
---
# <a name="sessioncreate-method"></a><span data-ttu-id="70edb-106">Session. Create 方法</span><span class="sxs-lookup"><span data-stu-id="70edb-106">Session.Create method</span></span>

<span data-ttu-id="70edb-107">建立資源的新實例，並傳回新物件 [*(EPR) 的端點參考*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="70edb-107">Creates a new instance of a resource and returns the [*endpoint reference (EPR)*](windows-remote-management-glossary.md) of the new object.</span></span>

## <a name="syntax"></a><span data-ttu-id="70edb-108">語法</span><span class="sxs-lookup"><span data-stu-id="70edb-108">Syntax</span></span>


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="70edb-109">參數</span><span class="sxs-lookup"><span data-stu-id="70edb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70edb-110">*resourceUri* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70edb-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70edb-111">要建立之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="70edb-111">Identifier of the resource to create.</span></span>

<span data-ttu-id="70edb-112">此參數可包含下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="70edb-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="70edb-113">具有一或多個 [*選取器*](windows-remote-management-glossary.md)的 URI。</span><span class="sxs-lookup"><span data-stu-id="70edb-113">URI with one or more [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="70edb-114">請注意， [*WMI 外掛程式*](windows-remote-management-glossary.md) 不支援建立 [WS-Management 通訊協定](ws-management-protocol.md) 接聽程式以外的任何資源。</span><span class="sxs-lookup"><span data-stu-id="70edb-114">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a [WS-Management Protocol](ws-management-protocol.md) listener.</span></span>
-   <span data-ttu-id="70edb-115">可能包含選取器、[*片段*](windows-remote-management-glossary.md)或 [*選項*](windows-remote-management-glossary.md)的 [**ResourceLocator**](resourcelocator.md)物件。</span><span class="sxs-lookup"><span data-stu-id="70edb-115">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="70edb-116">[*Ws-addressing*](windows-remote-management-glossary.md) 端點參考，如 WS-Management 通訊協定標準中所述。</span><span class="sxs-lookup"><span data-stu-id="70edb-116">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="70edb-117">如需 WS-Management 通訊協定之公用規格的詳細資訊，請參閱 [管理規格索引頁面](/previous-versions/dotnet/articles/ms951267(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="70edb-117">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="70edb-118">*資源*</span><span class="sxs-lookup"><span data-stu-id="70edb-118">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="70edb-119">包含資源內容的 XML。</span><span class="sxs-lookup"><span data-stu-id="70edb-119">The XML that contains resource content.</span></span>

</dd> <dt>

<span data-ttu-id="70edb-120">*旗標* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="70edb-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70edb-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="70edb-121">Reserved.</span></span> <span data-ttu-id="70edb-122">必須設定為 0。</span><span class="sxs-lookup"><span data-stu-id="70edb-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70edb-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="70edb-123">Return value</span></span>

<span data-ttu-id="70edb-124">新資源的 EPR。</span><span class="sxs-lookup"><span data-stu-id="70edb-124">The EPR of the new resource.</span></span>

## <a name="remarks"></a><span data-ttu-id="70edb-125">備註</span><span class="sxs-lookup"><span data-stu-id="70edb-125">Remarks</span></span>

<span data-ttu-id="70edb-126">**Session。 Create** 只能用來建立資源的新實例。</span><span class="sxs-lookup"><span data-stu-id="70edb-126">**Session.Create** is only used for creating new instances of a resource.</span></span> <span data-ttu-id="70edb-127">使用 [**Session. Put**](session-put.md) 方法來更新資源的現有實例。</span><span class="sxs-lookup"><span data-stu-id="70edb-127">Use the [**Session.Put**](session-put.md) method to update existing instances of a resource.</span></span> <span data-ttu-id="70edb-128">取得新的資源 URI 之後，您就可以呼叫 [**Session。 Get**](session-get.md) 會取得新的物件。</span><span class="sxs-lookup"><span data-stu-id="70edb-128">After you obtain the new resource URI, you can call [**Session.Get**](session-get.md) to retrieve the new object.</span></span> <span data-ttu-id="70edb-129">新物件包含資源提供者在建立新物件時所指派的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="70edb-129">The new object contains any properties that the resource provider assigns when creating the new object.</span></span> <span data-ttu-id="70edb-130">例如，如果您建立新的 [*WS-Management 通訊協定*](windows-remote-management-glossary.md) 接聽程式，並使用 **Session** 取出接聽程式物件，則您也會取得 **Port**、 **Enabled** 和 **ListeningOn** 屬性。</span><span class="sxs-lookup"><span data-stu-id="70edb-130">For example, if you create a new WS-Management protocol [*listener*](windows-remote-management-glossary.md) and retrieve the listener object using **Session.Get**, then you also obtain the **Port**, **Enabled**, and **ListeningOn** properties.</span></span>

<span data-ttu-id="70edb-131">請注意， [*WMI 外掛程式*](windows-remote-management-glossary.md) 不支援建立 WS-Management 通訊協定接聽程式以外的任何資源。</span><span class="sxs-lookup"><span data-stu-id="70edb-131">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a WS-Management protocol listener.</span></span>

<span data-ttu-id="70edb-132">下列語法用來呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="70edb-132">The following syntax is used to call this method.</span></span>


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a><span data-ttu-id="70edb-133">範例</span><span class="sxs-lookup"><span data-stu-id="70edb-133">Examples</span></span>

<span data-ttu-id="70edb-134">下列 VBScript 程式碼範例會呼叫 **Session** ，在本機電腦上建立接聽程式。</span><span class="sxs-lookup"><span data-stu-id="70edb-134">The following VBScript code example calls **Session.Create** to create a listener on the local computer.</span></span>


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
```



## <a name="requirements"></a><span data-ttu-id="70edb-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="70edb-135">Requirements</span></span>



| <span data-ttu-id="70edb-136">需求</span><span class="sxs-lookup"><span data-stu-id="70edb-136">Requirement</span></span> | <span data-ttu-id="70edb-137">值</span><span class="sxs-lookup"><span data-stu-id="70edb-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="70edb-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70edb-138">Minimum supported client</span></span><br/> | <span data-ttu-id="70edb-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70edb-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="70edb-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70edb-140">Minimum supported server</span></span><br/> | <span data-ttu-id="70edb-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70edb-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="70edb-142">標頭</span><span class="sxs-lookup"><span data-stu-id="70edb-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="70edb-143"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="70edb-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="70edb-144">Idl</span><span class="sxs-lookup"><span data-stu-id="70edb-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="70edb-145"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="70edb-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="70edb-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="70edb-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="70edb-147"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="70edb-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="70edb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="70edb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70edb-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70edb-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70edb-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70edb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70edb-151">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="70edb-151">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="70edb-152">WS-Management 通訊協定</span><span class="sxs-lookup"><span data-stu-id="70edb-152">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

