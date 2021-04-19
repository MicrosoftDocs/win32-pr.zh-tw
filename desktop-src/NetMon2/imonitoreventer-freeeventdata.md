---
description: FreeEventData 方法會釋出配置給 NMEVENTDATA 結構的空間。
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'IMonitorEventer：： FreeEventData 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973011"
---
# <a name="imonitoreventerfreeeventdata-method"></a><span data-ttu-id="ba82a-103">IMonitorEventer：： FreeEventData 方法</span><span class="sxs-lookup"><span data-stu-id="ba82a-103">IMonitorEventer::FreeEventData method</span></span>

<span data-ttu-id="ba82a-104">**FreeEventData** 方法會釋出配置給 [**NMEVENTDATA**](nmeventdata.md)結構的空間。</span><span class="sxs-lookup"><span data-stu-id="ba82a-104">The **FreeEventData** method frees space allocated for the [**NMEVENTDATA**](nmeventdata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba82a-105">語法</span><span class="sxs-lookup"><span data-stu-id="ba82a-105">Syntax</span></span>


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="ba82a-106">參數</span><span class="sxs-lookup"><span data-stu-id="ba82a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba82a-107">*pNMEventData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ba82a-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba82a-108">[**NMEVENTDATA**](nmeventdata.md)結構的位址，也就是釋放的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ba82a-108">Address of the [**NMEVENTDATA**](nmeventdata.md) structure, the memory of which is freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba82a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba82a-109">Return value</span></span>

<span data-ttu-id="ba82a-110">這個方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ba82a-110">This method returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba82a-111">備註</span><span class="sxs-lookup"><span data-stu-id="ba82a-111">Remarks</span></span>

<span data-ttu-id="ba82a-112">監視器會呼叫這個方法來釋放它們配置給事件資料結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ba82a-112">Monitors call this method to free the memory they allocate for the event data structure.</span></span> <span data-ttu-id="ba82a-113">請注意，雖然監視器仍具有已配置之 [**NMEVENTDATA**](nmeventdata.md) 結構中字串的指標，但是在呼叫 **FreeEventData** 方法之前，必須先釋放這些字串的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ba82a-113">Be aware that while the monitor still has a pointer to strings in an allocated [**NMEVENTDATA**](nmeventdata.md) structure, the memory for these strings must be freed before the **FreeEventData** method is called.</span></span>

<span data-ttu-id="ba82a-114">如需有關如何為 [**NMEVENTDATA**](nmeventdata.md) 結構配置記憶體的詳細資訊，請參閱 [**IMonitorEventer：： GetEventData**](imonitoreventer-geteventdata.md)。</span><span class="sxs-lookup"><span data-stu-id="ba82a-114">For more information about how to allocate memory for an [**NMEVENTDATA**](nmeventdata.md) structure, see [**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba82a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba82a-115">Requirements</span></span>



| <span data-ttu-id="ba82a-116">需求</span><span class="sxs-lookup"><span data-stu-id="ba82a-116">Requirement</span></span> | <span data-ttu-id="ba82a-117">值</span><span class="sxs-lookup"><span data-stu-id="ba82a-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ba82a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba82a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ba82a-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba82a-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ba82a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba82a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ba82a-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba82a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ba82a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ba82a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba82a-123"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="ba82a-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba82a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba82a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba82a-125">**IMonitorEventer**</span><span class="sxs-lookup"><span data-stu-id="ba82a-125">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="ba82a-126">**IMonitorEventer::GetEventData**</span><span class="sxs-lookup"><span data-stu-id="ba82a-126">**IMonitorEventer::GetEventData**</span></span>](imonitoreventer-geteventdata.md)
</dt> <dt>

[<span data-ttu-id="ba82a-127">**NMEVENTDATA**</span><span class="sxs-lookup"><span data-stu-id="ba82a-127">**NMEVENTDATA**</span></span>](nmeventdata.md)
</dt> </dl>

 

 




