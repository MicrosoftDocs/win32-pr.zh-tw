---
description: '\_SWbemObject 物件的 properties 屬性會傳回內含物件，該物件為目前類別或實例之屬性的集合。 這是唯讀的屬性。'
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: 'SWbemObject.Properties_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b215abb7a0ca466c8a93fe20f20518f8d7b2ec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977232"
---
# <a name="swbemobjectproperties_-property"></a><span data-ttu-id="46125-104">SWbemObject \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="46125-104">SWbemObject.Properties\_ property</span></span>

<span data-ttu-id="46125-105">[**SWbemObject**](swbemobject.md)物件的 **properties \_** 屬性會傳回 [**內含**](swbempropertyset.md)物件，該物件為目前類別或實例之屬性的集合。</span><span class="sxs-lookup"><span data-stu-id="46125-105">The **Properties\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that is a collection of the properties for the current class or instance.</span></span> <span data-ttu-id="46125-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="46125-106">This property is read-only.</span></span>

<span data-ttu-id="46125-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="46125-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="46125-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="46125-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="46125-109">語法</span><span class="sxs-lookup"><span data-stu-id="46125-109">Syntax</span></span>


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="46125-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="46125-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="46125-111">範例</span><span class="sxs-lookup"><span data-stu-id="46125-111">Examples</span></span>

<span data-ttu-id="46125-112">在 TechNet 資源庫上 [產生 POWERSHELL WMI 類別腳本](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) powershell 程式碼範例會使用 Properties \_ 屬性來為每個 wmi 類別產生腳本，以列出 wmi 類別名稱和屬性。</span><span class="sxs-lookup"><span data-stu-id="46125-112">The [Generate Powershell WMI Class Scripts](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) PowerShell code example on TechNet Gallery uses the Properties\_ property to generate a script for each of the WMI classes that will list the WMI class name and the properties.</span></span>

<span data-ttu-id="46125-113">下列程式碼取自 TechNet 資源庫上 [Wmi 類別 VBScript 程式](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) 代碼範例的所有屬性（property），列出指定之 wmi 類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="46125-113">The following code, taken from the [List All the Properties for a WMI Class](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) VBScript code example on TechNet Gallery, Lists the properties for a specified WMI class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="46125-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="46125-114">Requirements</span></span>



| <span data-ttu-id="46125-115">需求</span><span class="sxs-lookup"><span data-stu-id="46125-115">Requirement</span></span> | <span data-ttu-id="46125-116">值</span><span class="sxs-lookup"><span data-stu-id="46125-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46125-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46125-117">Minimum supported client</span></span><br/> | <span data-ttu-id="46125-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46125-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46125-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46125-119">Minimum supported server</span></span><br/> | <span data-ttu-id="46125-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46125-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46125-121">標頭</span><span class="sxs-lookup"><span data-stu-id="46125-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="46125-122"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="46125-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="46125-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="46125-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="46125-124"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="46125-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="46125-125">DLL</span><span class="sxs-lookup"><span data-stu-id="46125-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46125-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46125-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="46125-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="46125-127">CLSID</span></span><br/>                    | <span data-ttu-id="46125-128">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="46125-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="46125-129">IID</span><span class="sxs-lookup"><span data-stu-id="46125-129">IID</span></span><br/>                      | <span data-ttu-id="46125-130">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="46125-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




