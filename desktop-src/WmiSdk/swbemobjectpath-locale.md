---
description: SWbemObjectPath 物件的 Locale 屬性包含物件路徑的地區設定。
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: 'SWbemObjectPath： Locale 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990328"
---
# <a name="swbemobjectpathlocale-property"></a><span data-ttu-id="008ac-103">SWbemObjectPath。 Locale 屬性</span><span class="sxs-lookup"><span data-stu-id="008ac-103">SWbemObjectPath.Locale property</span></span>

<span data-ttu-id="008ac-104">[**SWbemObjectPath**](swbemobjectpath.md)物件的 **locale** 屬性包含物件路徑的地區設定。</span><span class="sxs-lookup"><span data-stu-id="008ac-104">The **Locale** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the locale of object path.</span></span>

<span data-ttu-id="008ac-105">當 **SWbemObjectPath. Locale** 屬性是獨立 [**SWbemObjectPath**](swbemobjectpath.md) 物件的一部分時，就會讀取/寫入，而且可以用來設定該標記的地區設定元件。</span><span class="sxs-lookup"><span data-stu-id="008ac-105">When the **SWbemObjectPath.Locale** property is part of a standalone [**SWbemObjectPath**](swbemobjectpath.md) object, it is read/write and can be used to set the locale component of the moniker.</span></span>

<span data-ttu-id="008ac-106">當 **SWbemObjectPath. Locale** 屬性當做 [**\_ SWbemObject. Path**](swbemobject-path-.md)屬性的一部分來存取時，它會是唯讀的，而且會報告用來系結至從中取得物件之命名空間的地區設定值。</span><span class="sxs-lookup"><span data-stu-id="008ac-106">When the **SWbemObjectPath.Locale** property is accessed as part of a [**SWbemObject.Path\_**](swbemobject-path-.md) property, it is read-only and reports the value of the locale used in binding to the namespace from which the object was obtained.</span></span>

<span data-ttu-id="008ac-107">若為 Microsoft 地區設定識別碼，則字串的格式為 "MS \_ xxxx"，其中 xxxx 是十六進位格式的字串，表示 LCID。</span><span class="sxs-lookup"><span data-stu-id="008ac-107">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="008ac-108">例如，美式英文地區設定識別碼是「MS \_ 409」。</span><span class="sxs-lookup"><span data-stu-id="008ac-108">For example, the American English locale identifier is "MS\_409".</span></span>

<span data-ttu-id="008ac-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="008ac-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="008ac-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="008ac-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="008ac-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="008ac-111">Syntax</span></span>


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a><span data-ttu-id="008ac-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="008ac-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="008ac-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="008ac-113">Requirements</span></span>



| <span data-ttu-id="008ac-114">需求</span><span class="sxs-lookup"><span data-stu-id="008ac-114">Requirement</span></span> | <span data-ttu-id="008ac-115">值</span><span class="sxs-lookup"><span data-stu-id="008ac-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="008ac-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="008ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="008ac-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="008ac-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="008ac-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="008ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="008ac-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="008ac-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="008ac-120">標頭</span><span class="sxs-lookup"><span data-stu-id="008ac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="008ac-121"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="008ac-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="008ac-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="008ac-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="008ac-123"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="008ac-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="008ac-124">DLL</span><span class="sxs-lookup"><span data-stu-id="008ac-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="008ac-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="008ac-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="008ac-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="008ac-126">CLSID</span></span><br/>                    | <span data-ttu-id="008ac-127">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="008ac-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="008ac-128">IID</span><span class="sxs-lookup"><span data-stu-id="008ac-128">IID</span></span><br/>                      | <span data-ttu-id="008ac-129">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="008ac-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




