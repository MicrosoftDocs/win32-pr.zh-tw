---
title: 'DRV_CLOSE 訊息 (Mmsystem .h) '
description: 指示驅動程式關閉指定的實例。 如果沒有開啟其他實例，驅動程式應該準備好從記憶體進行後續的發行。
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- DRV_CLOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a205b7e6edb4a427b0e80d32cc711d9bf2b052c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965949"
---
# <a name="drv_close-message"></a><span data-ttu-id="8b8e3-105">WINSPOOL.DRV \_ 關閉訊息</span><span class="sxs-lookup"><span data-stu-id="8b8e3-105">DRV\_CLOSE message</span></span>

<span data-ttu-id="8b8e3-106">指示驅動程式關閉指定的實例。</span><span class="sxs-lookup"><span data-stu-id="8b8e3-106">Directs the driver to close the given instance.</span></span> <span data-ttu-id="8b8e3-107">如果沒有開啟其他實例，驅動程式應該準備好從記憶體進行後續的發行。</span><span class="sxs-lookup"><span data-stu-id="8b8e3-107">If no other instances are open, the driver should prepare for subsequent release from memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b8e3-108">參數</span><span class="sxs-lookup"><span data-stu-id="8b8e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b8e3-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="8b8e3-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="8b8e3-110">可安裝驅動程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b8e3-110">Identifier of the installable driver.</span></span> <span data-ttu-id="8b8e3-111">這與先前 [**Winspool.drv \_ 開啟**](drv-open.md) 訊息中的驅動程式所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="8b8e3-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="8b8e3-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="8b8e3-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="8b8e3-113">可安裝的驅動程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b8e3-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="8b8e3-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8b8e3-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8b8e3-115">在 **DriverClose** 函數的呼叫中，指定為 *lParam1* 參數的32位值。</span><span class="sxs-lookup"><span data-stu-id="8b8e3-115">32-bit value specified as the *lParam1* parameter in a call to the **DriverClose** function.</span></span>

</dd> <dt>

<span data-ttu-id="8b8e3-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8b8e3-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8b8e3-117">在 **DriverClose** 函數的呼叫中，指定為 *lParam2* 參數的32位值。</span><span class="sxs-lookup"><span data-stu-id="8b8e3-117">32-bit value specified as the *lParam2* parameter in a call to the **DriverClose** function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b8e3-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b8e3-118">Return Value</span></span>

<span data-ttu-id="8b8e3-119">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="8b8e3-119">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b8e3-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b8e3-120">Requirements</span></span>



| <span data-ttu-id="8b8e3-121">需求</span><span class="sxs-lookup"><span data-stu-id="8b8e3-121">Requirement</span></span> | <span data-ttu-id="8b8e3-122">值</span><span class="sxs-lookup"><span data-stu-id="8b8e3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b8e3-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b8e3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8b8e3-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b8e3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8b8e3-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b8e3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8b8e3-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b8e3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8b8e3-127">標頭</span><span class="sxs-lookup"><span data-stu-id="8b8e3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b8e3-128"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8b8e3-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b8e3-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b8e3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b8e3-130">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="8b8e3-130">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="8b8e3-131">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="8b8e3-131">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





