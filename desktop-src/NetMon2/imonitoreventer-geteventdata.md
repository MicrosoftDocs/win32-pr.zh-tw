---
description: GetEventData 方法會為 NMEVENTDATA 和 NMCOLUMNINFO 結構配置空間。
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'IMonitorEventer：： GetEventData 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191276"
---
# <a name="imonitoreventergeteventdata-method"></a><span data-ttu-id="02656-103">IMonitorEventer：： GetEventData 方法</span><span class="sxs-lookup"><span data-stu-id="02656-103">IMonitorEventer::GetEventData method</span></span>

<span data-ttu-id="02656-104">**GetEventData** 方法會為 [NMEVENTDATA](nmeventdata.md)和 [NMCOLUMNINFO](nmcolumninfo.md)結構配置空間。</span><span class="sxs-lookup"><span data-stu-id="02656-104">The **GetEventData** method allocates space for the [NMEVENTDATA](nmeventdata.md) and [NMCOLUMNINFO](nmcolumninfo.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="02656-105">語法</span><span class="sxs-lookup"><span data-stu-id="02656-105">Syntax</span></span>


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="02656-106">參數</span><span class="sxs-lookup"><span data-stu-id="02656-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02656-107">*bNumColumns* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02656-107">*bNumColumns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02656-108">所需的 **NMCOLUMNINFO** 結構數目。</span><span class="sxs-lookup"><span data-stu-id="02656-108">Number of **NMCOLUMNINFO** structures needed.</span></span>

</dd> <dt>

<span data-ttu-id="02656-109">*ppNMEventData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="02656-109">*ppNMEventData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02656-110">傳回之 **NMEVENTDATA** 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="02656-110">Address of the **NMEVENTDATA** structure that is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02656-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="02656-111">Return value</span></span>

<span data-ttu-id="02656-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="02656-112">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="02656-113">如果此方法不成功，傳回值就會 \_ 從記憶體中 NMERR 出來 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="02656-113">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="02656-114">備註</span><span class="sxs-lookup"><span data-stu-id="02656-114">Remarks</span></span>

<span data-ttu-id="02656-115">監視器會呼叫這個方法，以配置事件資料和資料行資訊結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="02656-115">Monitors call this method to allocate memory for the event data and column information structures.</span></span> <span data-ttu-id="02656-116">若要釋放配置給 **NMEVENTDATA** 結構的記憶體，請參閱 [IMonitorEventer：： FreeEventData](imonitoreventer-freeeventdata.md)。</span><span class="sxs-lookup"><span data-stu-id="02656-116">To free memory allocated for an **NMEVENTDATA** structure, see [IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02656-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="02656-117">Requirements</span></span>



| <span data-ttu-id="02656-118">需求</span><span class="sxs-lookup"><span data-stu-id="02656-118">Requirement</span></span> | <span data-ttu-id="02656-119">值</span><span class="sxs-lookup"><span data-stu-id="02656-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="02656-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02656-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02656-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02656-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="02656-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02656-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02656-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02656-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="02656-124">標頭</span><span class="sxs-lookup"><span data-stu-id="02656-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="02656-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="02656-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02656-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02656-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02656-127">IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="02656-127">IMonitorEventer</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="02656-128">IMonitorEventer::FreeEventData</span><span class="sxs-lookup"><span data-stu-id="02656-128">IMonitorEventer::FreeEventData</span></span>](imonitoreventer-freeeventdata.md)
</dt> <dt>

[<span data-ttu-id="02656-129">NMEVENTDATA</span><span class="sxs-lookup"><span data-stu-id="02656-129">NMEVENTDATA</span></span>](nmeventdata.md)
</dt> <dt>

[<span data-ttu-id="02656-130">NMCOLUMNINFO</span><span class="sxs-lookup"><span data-stu-id="02656-130">NMCOLUMNINFO</span></span>](nmcolumninfo.md)
</dt> </dl>

 

 




