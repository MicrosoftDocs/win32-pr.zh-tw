---
description: SWbemObjectPath 物件的 SetAsClass 方法會強制路徑定址 WMI 類別。
ms.assetid: d341b980-bac9-4db4-a55f-eb971fb385da
ms.tgt_platform: multiple
title: 'SWbemObjectPath. SetAsClass 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsClass
- ISWbemObjectPath.SetAsClass
- ISWbemObjectPath.put_SetAsClass
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 371fe95c3a7152767c45849191658c4bcb661750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988720"
---
# <a name="swbemobjectpathsetasclass-property"></a><span data-ttu-id="5c806-103">SWbemObjectPath. SetAsClass 屬性</span><span class="sxs-lookup"><span data-stu-id="5c806-103">SWbemObjectPath.SetAsClass property</span></span>

<span data-ttu-id="5c806-104">[**SWbemObjectPath**](swbemobjectpath.md)物件的 **SetAsClass** 方法會強制路徑定址 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="5c806-104">The **SetAsClass** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a WMI class.</span></span>

<span data-ttu-id="5c806-105">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="5c806-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c806-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c806-106">Syntax</span></span>


```VB
SWbemObjectPath.SetAsClass
```



## <a name="property-value"></a><span data-ttu-id="5c806-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="5c806-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c806-108">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5c806-108">Error codes</span></span>

<span data-ttu-id="5c806-109">取得或設定 **SetAsClass** 屬性之後， **Err** 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5c806-109">After you get or set the **SetAsClass** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="5c806-110">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="5c806-110">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5c806-111">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5c806-111">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c806-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c806-112">Requirements</span></span>



| <span data-ttu-id="5c806-113">需求</span><span class="sxs-lookup"><span data-stu-id="5c806-113">Requirement</span></span> | <span data-ttu-id="5c806-114">值</span><span class="sxs-lookup"><span data-stu-id="5c806-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c806-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c806-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5c806-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c806-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c806-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c806-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5c806-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c806-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c806-119">標頭</span><span class="sxs-lookup"><span data-stu-id="5c806-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c806-120"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c806-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c806-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5c806-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c806-122"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5c806-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5c806-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5c806-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c806-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c806-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c806-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="5c806-125">CLSID</span></span><br/>                    | <span data-ttu-id="5c806-126">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="5c806-126">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="5c806-127">IID</span><span class="sxs-lookup"><span data-stu-id="5c806-127">IID</span></span><br/>                      | <span data-ttu-id="5c806-128">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="5c806-128">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




