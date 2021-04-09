---
title: 記錄檔。 Item 屬性
description: 從集合中抓取指定的 LogFileItem 實例。
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- 專案屬性 SysMon
- Item 屬性 SysMon，記錄檔類別
- 記錄檔類別 SysMon，專案屬性
topic_type:
- apiref
api_name:
- LogFiles.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85af003cd6c0291ec90d17906f249726dfd526f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024828"
---
# <a name="logfilesitem-property"></a><span data-ttu-id="2d94d-106">記錄檔。 Item 屬性</span><span class="sxs-lookup"><span data-stu-id="2d94d-106">LogFiles.Item property</span></span>

<span data-ttu-id="2d94d-107">從集合中抓取指定的 [**LogFileItem**](logfileitem.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="2d94d-107">Retrieves the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span>

<span data-ttu-id="2d94d-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2d94d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d94d-109">語法</span><span class="sxs-lookup"><span data-stu-id="2d94d-109">Syntax</span></span>


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a><span data-ttu-id="2d94d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="2d94d-110">Property value</span></span>

<span data-ttu-id="2d94d-111">對應至指定之索引值的 [**LogFileItem**](logfileitem.md)實例。</span><span class="sxs-lookup"><span data-stu-id="2d94d-111">[**LogFileItem**](logfileitem.md) instance that corresponds to the specified index value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d94d-112">備註</span><span class="sxs-lookup"><span data-stu-id="2d94d-112">Remarks</span></span>

<span data-ttu-id="2d94d-113">這是記錄 [**檔物件的**](systemmonitor-logfiles.md) 預設屬性。</span><span class="sxs-lookup"><span data-stu-id="2d94d-113">This is the default property of the [**LogFiles**](systemmonitor-logfiles.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d94d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d94d-114">Requirements</span></span>



| <span data-ttu-id="2d94d-115">需求</span><span class="sxs-lookup"><span data-stu-id="2d94d-115">Requirement</span></span> | <span data-ttu-id="2d94d-116">值</span><span class="sxs-lookup"><span data-stu-id="2d94d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d94d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d94d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2d94d-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d94d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2d94d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d94d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2d94d-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d94d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d94d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2d94d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d94d-122"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2d94d-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d94d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d94d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d94d-124">LogFiles</span><span class="sxs-lookup"><span data-stu-id="2d94d-124">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="2d94d-125">**LogFileItem**</span><span class="sxs-lookup"><span data-stu-id="2d94d-125">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="2d94d-126">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="2d94d-126">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





