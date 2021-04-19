---
description: SWbemObjectPath 物件的 Path 屬性包含絕對路徑。 這與 \_ \_ COM API 中的 Path 屬性相同。 這是此物件的預設屬性。
ms.assetid: cc0d2c56-bb69-4008-8688-0166714ea5fd
ms.tgt_platform: multiple
title: 'SWbemObjectPath： Path 屬性 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Path
- ISWbemObjectPath.Path
- ISWbemObjectPath.get_Path
- ISWbemObjectPath.put_Path
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02a3dfbf6dbc24434ad4d9807ab5e39dbc121043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988868"
---
# <a name="swbemobjectpathpath-property"></a><span data-ttu-id="60a09-105">SWbemObjectPath 路徑屬性</span><span class="sxs-lookup"><span data-stu-id="60a09-105">SWbemObjectPath.Path property</span></span>

<span data-ttu-id="60a09-106">[**SWbemObjectPath**](swbemobjectpath.md)物件的 **path** 屬性包含絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="60a09-106">The **Path** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the absolute path.</span></span> <span data-ttu-id="60a09-107">這與 COM API 中的[ \_ \_ Path](wmi-system-properties.md)屬性相同。</span><span class="sxs-lookup"><span data-stu-id="60a09-107">This is the same as the [\_\_Path](wmi-system-properties.md) property in the COM API.</span></span> <span data-ttu-id="60a09-108">這是此物件的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="60a09-108">This is the default property of this object.</span></span>

<span data-ttu-id="60a09-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="60a09-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="60a09-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="60a09-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="60a09-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="60a09-111">Syntax</span></span>


```VB
SWbemObjectPath.Path As String
```



## <a name="property-value"></a><span data-ttu-id="60a09-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="60a09-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="60a09-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="60a09-113">Requirements</span></span>



| <span data-ttu-id="60a09-114">需求</span><span class="sxs-lookup"><span data-stu-id="60a09-114">Requirement</span></span> | <span data-ttu-id="60a09-115">值</span><span class="sxs-lookup"><span data-stu-id="60a09-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60a09-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60a09-116">Minimum supported client</span></span><br/> | <span data-ttu-id="60a09-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60a09-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60a09-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60a09-118">Minimum supported server</span></span><br/> | <span data-ttu-id="60a09-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60a09-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60a09-120">標頭</span><span class="sxs-lookup"><span data-stu-id="60a09-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="60a09-121"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="60a09-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="60a09-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="60a09-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="60a09-123"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="60a09-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="60a09-124">DLL</span><span class="sxs-lookup"><span data-stu-id="60a09-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60a09-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60a09-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="60a09-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="60a09-126">CLSID</span></span><br/>                    | <span data-ttu-id="60a09-127">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="60a09-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="60a09-128">IID</span><span class="sxs-lookup"><span data-stu-id="60a09-128">IID</span></span><br/>                      | <span data-ttu-id="60a09-129">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="60a09-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




