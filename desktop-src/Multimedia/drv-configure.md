---
title: 'DRV_CONFIGURE 訊息 (Mmsystem .h) '
description: 指示可安裝的驅動程式顯示其設定對話方塊，並讓使用者為指定的可安裝驅動程式實例指定新設定。
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- DRV_CONFIGURE message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935077"
---
# <a name="drv_configure-message"></a><span data-ttu-id="cb254-104">WINSPOOL.DRV \_ 設定訊息</span><span class="sxs-lookup"><span data-stu-id="cb254-104">DRV\_CONFIGURE message</span></span>

<span data-ttu-id="cb254-105">指示可安裝的驅動程式顯示其設定對話方塊，並讓使用者為指定的可安裝驅動程式實例指定新設定。</span><span class="sxs-lookup"><span data-stu-id="cb254-105">Directs the installable driver to display its configuration dialog box and let the user specify new settings for the given installable driver instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb254-106">參數</span><span class="sxs-lookup"><span data-stu-id="cb254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb254-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="cb254-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="cb254-108">可安裝驅動程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb254-108">Identifier of the installable driver.</span></span> <span data-ttu-id="cb254-109">這與先前 [**Winspool.drv \_ 開啟**](drv-open.md) 訊息中的驅動程式所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="cb254-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="cb254-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="cb254-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="cb254-111">可安裝的驅動程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cb254-111">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="cb254-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="cb254-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="cb254-113">父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cb254-113">Handle of the parent window.</span></span> <span data-ttu-id="cb254-114">此視窗會用來做為 [設定] 對話方塊的父視窗。</span><span class="sxs-lookup"><span data-stu-id="cb254-114">This window is used as the parent window for the configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="cb254-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cb254-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cb254-116">[**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)結構的位址或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cb254-116">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="cb254-117">如果指定了結構，它就會包含與驅動程式相關聯的登錄機碼和值的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb254-117">If the structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb254-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb254-118">Return Value</span></span>

<span data-ttu-id="cb254-119">傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="cb254-119">Returns one of these values:</span></span>



| <span data-ttu-id="cb254-120">需求</span><span class="sxs-lookup"><span data-stu-id="cb254-120">Requirement</span></span> | <span data-ttu-id="cb254-121">值</span><span class="sxs-lookup"><span data-stu-id="cb254-121">Value</span></span> |
|-----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb254-122">DRVCNF \_ 確定</span><span class="sxs-lookup"><span data-stu-id="cb254-122">DRVCNF\_OK</span></span>      | <span data-ttu-id="cb254-123">設定成功;不需要採取任何進一步的動作。</span><span class="sxs-lookup"><span data-stu-id="cb254-123">The configuration is successful; no further action is required.</span></span>                                    |
| <span data-ttu-id="cb254-124">DRVCNF \_ 取消</span><span class="sxs-lookup"><span data-stu-id="cb254-124">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="cb254-125">使用者取消了對話方塊;不需要採取任何進一步的動作。</span><span class="sxs-lookup"><span data-stu-id="cb254-125">The user canceled the dialog box; no further action is required.</span></span>                                   |
| <span data-ttu-id="cb254-126">DRVCNF \_ 重新開機</span><span class="sxs-lookup"><span data-stu-id="cb254-126">DRVCNF\_RESTART</span></span> | <span data-ttu-id="cb254-127">設定成功，但在重新開機系統之前，變更不會生效。</span><span class="sxs-lookup"><span data-stu-id="cb254-127">The configuration is successful, but the changes do not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cb254-128">備註</span><span class="sxs-lookup"><span data-stu-id="cb254-128">Remarks</span></span>

<span data-ttu-id="cb254-129">有些可安裝的驅動程式會將設定資訊附加至指派給與驅動程式相關聯之登錄值的值。</span><span class="sxs-lookup"><span data-stu-id="cb254-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

<span data-ttu-id="cb254-130">WINSPOOL.DRV \_ cancel、Winspool.drv \_ OK 和 Winspool.drv \_ 重新開機傳回值已過時; 它們已分別由 DRVCNF \_ CANCEL、DRVCNF \_ OK 和 DRVCNF \_ restart 取代。</span><span class="sxs-lookup"><span data-stu-id="cb254-130">The DRV\_CANCEL, DRV\_OK, and DRV\_RESTART return values are obsolete; they have been replaced by DRVCNF\_CANCEL, DRVCNF\_OK, and DRVCNF\_RESTART, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb254-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb254-131">Requirements</span></span>



| <span data-ttu-id="cb254-132">需求</span><span class="sxs-lookup"><span data-stu-id="cb254-132">Requirement</span></span> | <span data-ttu-id="cb254-133">值</span><span class="sxs-lookup"><span data-stu-id="cb254-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb254-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb254-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cb254-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb254-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cb254-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb254-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cb254-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb254-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cb254-138">標頭</span><span class="sxs-lookup"><span data-stu-id="cb254-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb254-139"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="cb254-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb254-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb254-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb254-141">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="cb254-141">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="cb254-142">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="cb254-142">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

