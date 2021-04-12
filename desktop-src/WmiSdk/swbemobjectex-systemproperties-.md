---
description: 傳回內含物件，其中包含適用于物件的 WMI 系統屬性集合。
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: 'SWbemObjectEx.SystemProperties_ 屬性 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.SystemProperties_
- ISWbemObjectEx.SystemProperties_
- ISWbemObjectEx.get_SystemProperties_
- ISWbemObjectEx.put_SystemProperties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cf8b7e15536c0d4e3116f0583662b3cd0b7d0887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194912"
---
# <a name="swbemobjectexsystemproperties_-property"></a><span data-ttu-id="d95e6-103">SWbemObjectEx.SystemProperties \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="d95e6-103">SWbemObjectEx.SystemProperties\_ property</span></span>

<span data-ttu-id="d95e6-104">[**SWbemObjectEx**](swbemobjectex.md)物件的 **SystemProperties \_** 屬性會傳回 [**內含**](swbempropertyset.md)物件，其中包含適用于物件的 [WMI 系統屬性](wmi-system-properties.md)集合。</span><span class="sxs-lookup"><span data-stu-id="d95e6-104">The **SystemProperties\_** property of the [**SWbemObjectEx**](swbemobjectex.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that contains the collection of [WMI System Properties](wmi-system-properties.md) that apply to the object.</span></span>

<span data-ttu-id="d95e6-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d95e6-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d95e6-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d95e6-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d95e6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d95e6-107">Syntax</span></span>


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="d95e6-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="d95e6-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="d95e6-109">範例</span><span class="sxs-lookup"><span data-stu-id="d95e6-109">Examples</span></span>

<span data-ttu-id="d95e6-110">下列程式碼範例會抓取 Win32 進程類別的屬性值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d95e6-110">The following code sample retrieves the property values for the Win32\_Process class.</span></span>


```VB
Set objWmi = GetObject ("winmgmts:root\cimv2")
Set objClass = objWmi.Get("Win32_Process")

' SWbemObjectEx.SystemProperties_ returns 
' an SWbemPropertySet object that contains the collection
' of sytem properties for Win32_Process class

For Each objProperty In objClass.SystemProperties_

    WScript.Echo vbCrLf & objProperty.Name & ":"

    ' Have to take into account that
    ' __Derivation is an array

    If Not objProperty.IsArray Then
        WScript.Echo vbTab & objProperty.Value
    Else
        For Each strValue In objProperty.Value
            WScript.Echo vbTab & strValue
        Next
    End If

Next
```



## <a name="requirements"></a><span data-ttu-id="d95e6-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d95e6-111">Requirements</span></span>



| <span data-ttu-id="d95e6-112">需求</span><span class="sxs-lookup"><span data-stu-id="d95e6-112">Requirement</span></span> | <span data-ttu-id="d95e6-113">值</span><span class="sxs-lookup"><span data-stu-id="d95e6-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d95e6-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d95e6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d95e6-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d95e6-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d95e6-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d95e6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d95e6-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d95e6-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d95e6-118">標頭</span><span class="sxs-lookup"><span data-stu-id="d95e6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d95e6-119"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d95e6-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d95e6-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d95e6-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d95e6-121"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d95e6-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d95e6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d95e6-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d95e6-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d95e6-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d95e6-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="d95e6-124">CLSID</span></span><br/>                    | <span data-ttu-id="d95e6-125">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="d95e6-125">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="d95e6-126">IID</span><span class="sxs-lookup"><span data-stu-id="d95e6-126">IID</span></span><br/>                      | <span data-ttu-id="d95e6-127">IID \_ ISWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="d95e6-127">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d95e6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d95e6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d95e6-129">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="d95e6-129">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> </dl>

 

 




