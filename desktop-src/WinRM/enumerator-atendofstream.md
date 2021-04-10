---
title: 'AtEndOfStream 屬性 (WSManDisp .h) '
description: 取得布林值，指出集合中是否有其他專案。
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- AtEndOfStream 屬性 Windows 遠端管理
- AtEndOfStream 屬性 Windows 遠端管理，列舉值物件
- 列舉值物件 Windows 遠端管理，AtEndOfStream 屬性
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023798f6c868e434218dd1a4dbdf1928bf4526a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094215"
---
# <a name="enumeratoratendofstream-property"></a><span data-ttu-id="915dd-106">AtEndOfStream 屬性</span><span class="sxs-lookup"><span data-stu-id="915dd-106">Enumerator.AtEndOfStream property</span></span>

<span data-ttu-id="915dd-107">取得布林值，指出集合中是否有其他專案。</span><span class="sxs-lookup"><span data-stu-id="915dd-107">Gets a Boolean value that indicates whether there are any more items in the collection.</span></span>

<span data-ttu-id="915dd-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="915dd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="915dd-109">語法</span><span class="sxs-lookup"><span data-stu-id="915dd-109">Syntax</span></span>


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="915dd-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="915dd-110">Property value</span></span>

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="915dd-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**真**</span><span class="sxs-lookup"><span data-stu-id="915dd-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</span></span>


</dt> <dd>

<span data-ttu-id="915dd-112">集合中不再有任何專案。</span><span class="sxs-lookup"><span data-stu-id="915dd-112">No more items are in the collection.</span></span>

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="915dd-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**假**</span><span class="sxs-lookup"><span data-stu-id="915dd-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</span></span>


</dt> <dd>

<span data-ttu-id="915dd-114">有更多專案可供使用。</span><span class="sxs-lookup"><span data-stu-id="915dd-114">More items are available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="915dd-115">備註</span><span class="sxs-lookup"><span data-stu-id="915dd-115">Remarks</span></span>

<span data-ttu-id="915dd-116">如果您在取得所需的所有資料之後釋放 [**列舉**](enumerator.md) 值物件，則會移除任何暫止的列舉要求。</span><span class="sxs-lookup"><span data-stu-id="915dd-116">If you free the [**Enumerator**](enumerator.md) object after you have obtained all the data required, then any pending enumeration requests are removed.</span></span> <span data-ttu-id="915dd-117">如需詳細資訊，請參閱 [列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)。</span><span class="sxs-lookup"><span data-stu-id="915dd-117">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="examples"></a><span data-ttu-id="915dd-118">範例</span><span class="sxs-lookup"><span data-stu-id="915dd-118">Examples</span></span>

<span data-ttu-id="915dd-119">下列 VBScript 範例會列舉作業系統實例。</span><span class="sxs-lookup"><span data-stu-id="915dd-119">The following VBScript example enumerates operating system instances.</span></span> <span data-ttu-id="915dd-120">請注意，釋出列舉物件會清除任何暫止的列舉要求。</span><span class="sxs-lookup"><span data-stu-id="915dd-120">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span> <span data-ttu-id="915dd-121">DisplayOutput 副程式會以和 WinRM 工具相同的方式來格式化資料輸出。</span><span class="sxs-lookup"><span data-stu-id="915dd-121">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

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



## <a name="requirements"></a><span data-ttu-id="915dd-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="915dd-122">Requirements</span></span>



| <span data-ttu-id="915dd-123">需求</span><span class="sxs-lookup"><span data-stu-id="915dd-123">Requirement</span></span> | <span data-ttu-id="915dd-124">值</span><span class="sxs-lookup"><span data-stu-id="915dd-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="915dd-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="915dd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="915dd-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="915dd-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="915dd-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="915dd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="915dd-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="915dd-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="915dd-129">標頭</span><span class="sxs-lookup"><span data-stu-id="915dd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="915dd-130"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="915dd-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="915dd-131">Idl</span><span class="sxs-lookup"><span data-stu-id="915dd-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="915dd-132"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="915dd-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="915dd-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="915dd-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="915dd-134"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="915dd-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="915dd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="915dd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="915dd-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="915dd-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="915dd-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="915dd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="915dd-138">**列舉值**</span><span class="sxs-lookup"><span data-stu-id="915dd-138">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="915dd-139">列舉或列出資源的所有實例</span><span class="sxs-lookup"><span data-stu-id="915dd-139">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





