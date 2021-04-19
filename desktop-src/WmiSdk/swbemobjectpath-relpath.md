---
description: SWbemObjectPath 物件的 Relpath 屬性包含來自完整路徑的相對路徑。
ms.assetid: 9a4363ae-b6b3-4e8c-a7ca-a9e48c28e19b
ms.tgt_platform: multiple
title: 'SWbemObjectPath. Relpath 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Relpath
- ISWbemObjectPath.Relpath
- ISWbemObjectPath.get_Relpath
- ISWbemObjectPath.put_Relpath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8330d1cdc65e818acd4fda63b223303b779b5472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975255"
---
# <a name="swbemobjectpathrelpath-property"></a><span data-ttu-id="87da5-103">SWbemObjectPath. Relpath 屬性</span><span class="sxs-lookup"><span data-stu-id="87da5-103">SWbemObjectPath.Relpath property</span></span>

<span data-ttu-id="87da5-104">[**SWbemObjectPath**](swbemobjectpath.md)物件的 **Relpath** 屬性包含來自完整路徑的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="87da5-104">The **Relpath** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the relative path from the complete path.</span></span>

<span data-ttu-id="87da5-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="87da5-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="87da5-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="87da5-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="87da5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="87da5-107">Syntax</span></span>


```VB
SWbemObjectPath.Relpath As String
```



## <a name="property-value"></a><span data-ttu-id="87da5-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="87da5-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="87da5-109">範例</span><span class="sxs-lookup"><span data-stu-id="87da5-109">Examples</span></span>

<span data-ttu-id="87da5-110">下列 VBScript 程式碼範例顯示從 [**SWbemObject \_**](swbemobject-path-.md)取得的資料與 **SWbemObjectPath. Relpath** 之間的差異。</span><span class="sxs-lookup"><span data-stu-id="87da5-110">The following VBScript code example shows the difference between the data obtained from [**SWbemObject.Path\_**](swbemobject-path-.md) and **SWbemObjectPath.Relpath**.</span></span>


```VB
set objWMIService = GetObject ("winmgmts:root/cimv2")

set Processes = objWMIService.ExecQuery( _
    "Select * from win32_process")

For Each Process in Processes
 WScript.Echo Process.Path_ 
 WScript.Echo Process.Path_.Relpath
Next
```



## <a name="requirements"></a><span data-ttu-id="87da5-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="87da5-111">Requirements</span></span>



| <span data-ttu-id="87da5-112">需求</span><span class="sxs-lookup"><span data-stu-id="87da5-112">Requirement</span></span> | <span data-ttu-id="87da5-113">值</span><span class="sxs-lookup"><span data-stu-id="87da5-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87da5-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87da5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="87da5-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87da5-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87da5-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87da5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="87da5-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87da5-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87da5-118">標頭</span><span class="sxs-lookup"><span data-stu-id="87da5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="87da5-119"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="87da5-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="87da5-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="87da5-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="87da5-121"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="87da5-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="87da5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="87da5-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87da5-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87da5-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="87da5-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="87da5-124">CLSID</span></span><br/>                    | <span data-ttu-id="87da5-125">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="87da5-125">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="87da5-126">IID</span><span class="sxs-lookup"><span data-stu-id="87da5-126">IID</span></span><br/>                      | <span data-ttu-id="87da5-127">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="87da5-127">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




