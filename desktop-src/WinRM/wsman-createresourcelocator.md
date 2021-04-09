---
title: 'CreateResourceLocator 方法 (WSManDisp .h) '
description: 建立可使用的 ResourceLocator 物件，而不是在會話物件作業中指定資源 URI，例如 Session. Get、Session. Put 或 Session。列舉。
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- CreateResourceLocator 方法 Windows 遠端管理
- CreateResourceLocator 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，CreateResourceLocator 方法
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934289"
---
# <a name="wsmancreateresourcelocator-method"></a><span data-ttu-id="e68f1-106">WSMan. CreateResourceLocator 方法</span><span class="sxs-lookup"><span data-stu-id="e68f1-106">WSMan.CreateResourceLocator method</span></span>

<span data-ttu-id="e68f1-107">建立可使用的 [**ResourceLocator**](resourcelocator.md) 物件，而不 [**是在會話物件作業中**](session.md) 指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**session。列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="e68f1-107">Creates a [**ResourceLocator**](resourcelocator.md) object that can be used instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e68f1-108">語法</span><span class="sxs-lookup"><span data-stu-id="e68f1-108">Syntax</span></span>


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e68f1-109">參數</span><span class="sxs-lookup"><span data-stu-id="e68f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e68f1-110">*uri* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e68f1-110">*uri* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f1-111">資源的資源 URI。</span><span class="sxs-lookup"><span data-stu-id="e68f1-111">The resource URI for the resource.</span></span> <span data-ttu-id="e68f1-112">如需 URI 字串的詳細資訊，請參閱 [資源 uri](resource-uris.md)。</span><span class="sxs-lookup"><span data-stu-id="e68f1-112">For more information about URI strings, see [Resource URIs](resource-uris.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e68f1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e68f1-113">Return value</span></span>

<span data-ttu-id="e68f1-114">之後可以用來執行本機或遠端 WinRM 作業的 [**ResourceLocator**](resourcelocator.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e68f1-114">A [**ResourceLocator**](resourcelocator.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="e68f1-115">備註</span><span class="sxs-lookup"><span data-stu-id="e68f1-115">Remarks</span></span>

<span data-ttu-id="e68f1-116">如果未在 [**ResourceLocator**](resourcelocator.md)物件中指定 **FragmentDialect** 屬性，則預設值為 XPath 1.0 規格。</span><span class="sxs-lookup"><span data-stu-id="e68f1-116">If the **FragmentDialect** property is not specified in the [**ResourceLocator**](resourcelocator.md) object, the default is the XPath 1.0 specification.</span></span> <span data-ttu-id="e68f1-117">如需詳細資訊，請參閱 [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath)。</span><span class="sxs-lookup"><span data-stu-id="e68f1-117">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="examples"></a><span data-ttu-id="e68f1-118">範例</span><span class="sxs-lookup"><span data-stu-id="e68f1-118">Examples</span></span>

<span data-ttu-id="e68f1-119">下列 VBScript 程式碼範例會建立 [**ResourceLocator**](resourcelocator.md)物件，並從索引為 "1" 的 [**Win32 \_ >networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)實例取得網路介面卡 **描述** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="e68f1-119">The following VBScript code example creates a [**ResourceLocator**](resourcelocator.md) object and gets the network adapter **Description** property value from the instance of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) with an Index of "1".</span></span>


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a><span data-ttu-id="e68f1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e68f1-120">Requirements</span></span>



| <span data-ttu-id="e68f1-121">需求</span><span class="sxs-lookup"><span data-stu-id="e68f1-121">Requirement</span></span> | <span data-ttu-id="e68f1-122">值</span><span class="sxs-lookup"><span data-stu-id="e68f1-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e68f1-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e68f1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e68f1-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e68f1-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e68f1-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e68f1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e68f1-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e68f1-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e68f1-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e68f1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e68f1-128"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e68f1-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e68f1-129">Idl</span><span class="sxs-lookup"><span data-stu-id="e68f1-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e68f1-130"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e68f1-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e68f1-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="e68f1-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e68f1-132"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e68f1-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e68f1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e68f1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e68f1-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e68f1-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e68f1-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e68f1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e68f1-136">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="e68f1-136">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="e68f1-137">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="e68f1-137">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="e68f1-138">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="e68f1-138">**Session**</span></span>](session.md)
</dt> </dl>

 

