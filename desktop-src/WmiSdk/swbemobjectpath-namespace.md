---
description: SWbemObjectPath 物件的 Namespace 屬性包含屬於物件路徑的命名空間名稱。
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: 'SWbemObjectPath： Namespace 屬性 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Namespace
- ISWbemObjectPath.Namespace
- ISWbemObjectPath.get_Namespace
- ISWbemObjectPath.put_Namespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 885f7069e901d1d4a490ad7539077463f6c1838c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193261"
---
# <a name="swbemobjectpathnamespace-property"></a><span data-ttu-id="cb101-103">SWbemObjectPath 命名空間屬性</span><span class="sxs-lookup"><span data-stu-id="cb101-103">SWbemObjectPath.Namespace property</span></span>

<span data-ttu-id="cb101-104">[**SWbemObjectPath**](swbemobjectpath.md)物件的 **namespace** 屬性包含屬於物件路徑的命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="cb101-104">The **Namespace** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the name of the namespace that is part of the object path.</span></span> <span data-ttu-id="cb101-105">例如，下列路徑顯示的命名空間屬性會傳回根 \\ cimv2：</span><span class="sxs-lookup"><span data-stu-id="cb101-105">For example, the following path shows the namespace property that returns root\\cimv2:</span></span>

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

<span data-ttu-id="cb101-106">如需語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="cb101-106">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="cb101-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb101-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb101-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb101-108">Syntax</span></span>


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a><span data-ttu-id="cb101-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="cb101-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="cb101-110">範例</span><span class="sxs-lookup"><span data-stu-id="cb101-110">Examples</span></span>

<span data-ttu-id="cb101-111">下列範例說明如何從屬於硬碟的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例取得命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="cb101-111">The following example shows you how to obtain the namespace name from instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) that are hard disks.</span></span> <span data-ttu-id="cb101-112">腳本會連接到預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="cb101-112">The script connects to the default namespace.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer)

Set colDisks = objWMIService.ExecQuery _
    ("Select * from Win32_LogicalDisk " _
    & "Where DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
    Set objpath = objDisk.path_
    Wscript.Echo "Path of Win32_Logical disk instance " _
    & objDisk.DeviceID & " = " & objpath.Namespace   
Next
```



## <a name="requirements"></a><span data-ttu-id="cb101-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb101-113">Requirements</span></span>



| <span data-ttu-id="cb101-114">需求</span><span class="sxs-lookup"><span data-stu-id="cb101-114">Requirement</span></span> | <span data-ttu-id="cb101-115">值</span><span class="sxs-lookup"><span data-stu-id="cb101-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb101-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb101-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cb101-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb101-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb101-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb101-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cb101-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb101-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb101-120">標頭</span><span class="sxs-lookup"><span data-stu-id="cb101-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb101-121"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb101-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb101-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="cb101-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="cb101-123"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cb101-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cb101-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cb101-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb101-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb101-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cb101-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="cb101-126">CLSID</span></span><br/>                    | <span data-ttu-id="cb101-127">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="cb101-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="cb101-128">IID</span><span class="sxs-lookup"><span data-stu-id="cb101-128">IID</span></span><br/>                      | <span data-ttu-id="cb101-129">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="cb101-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

