---
description: '\_SWbemObject 物件的方法屬性會傳回 SWbemMethodSet 物件，該物件為目前類別或實例的方法集合。 這是唯讀的屬性。'
ms.assetid: ef9abced-5126-4698-b01e-f3e9c871162f
ms.tgt_platform: multiple
title: 'SWbemObject.Methods_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Methods_
- ISWbemObject.Methods_
- ISWbemObject.get_Methods_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6a702f0acf0736810de4d3176f8695fa8008d3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999935"
---
# <a name="swbemobjectmethods_-property"></a><span data-ttu-id="17a8e-104">SWbemObject 方法 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="17a8e-104">SWbemObject.Methods\_ property</span></span>

<span data-ttu-id="17a8e-105">[**SWbemObject**](swbemobject.md)物件的 **方法 \_** 屬性會傳回 [**SWbemMethodSet**](swbemmethodset.md)物件，該物件為目前類別或實例的方法集合。</span><span class="sxs-lookup"><span data-stu-id="17a8e-105">The **Methods\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemMethodSet**](swbemmethodset.md) object that is a collection of the methods for the current class or instance.</span></span> <span data-ttu-id="17a8e-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="17a8e-106">This property is read-only.</span></span>

<span data-ttu-id="17a8e-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="17a8e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="17a8e-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="17a8e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a8e-109">語法</span><span class="sxs-lookup"><span data-stu-id="17a8e-109">Syntax</span></span>


```VB
SWbemObject.Methods_ As Object
```



## <a name="property-value"></a><span data-ttu-id="17a8e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="17a8e-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="17a8e-111">範例</span><span class="sxs-lookup"><span data-stu-id="17a8e-111">Examples</span></span>

<span data-ttu-id="17a8e-112">下列程式 [代碼範例](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1)（取自 TechNet 資源庫）說明如何列出類別的所有方法。</span><span class="sxs-lookup"><span data-stu-id="17a8e-112">The following [code sample](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1), taken from the TechNet Gallery, describes how to list all methods of a class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Methods" 
WScript.Echo "---------------------------" 
  
For Each objClassMethod In objClass.Methods_ 
    WScript.Echo objClassMethod.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="17a8e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="17a8e-113">Requirements</span></span>



| <span data-ttu-id="17a8e-114">需求</span><span class="sxs-lookup"><span data-stu-id="17a8e-114">Requirement</span></span> | <span data-ttu-id="17a8e-115">值</span><span class="sxs-lookup"><span data-stu-id="17a8e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17a8e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17a8e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17a8e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17a8e-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17a8e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17a8e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17a8e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17a8e-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17a8e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="17a8e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="17a8e-121"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="17a8e-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="17a8e-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="17a8e-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="17a8e-123"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="17a8e-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="17a8e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="17a8e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17a8e-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17a8e-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="17a8e-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="17a8e-126">CLSID</span></span><br/>                    | <span data-ttu-id="17a8e-127">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="17a8e-127">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="17a8e-128">IID</span><span class="sxs-lookup"><span data-stu-id="17a8e-128">IID</span></span><br/>                      | <span data-ttu-id="17a8e-129">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="17a8e-129">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




