---
title: 'DRV_INSTALL 訊息 (Mmsystem .h) '
description: 通知驅動程式正在安裝。 驅動程式應該建立並初始化任何所需的登錄機碼和值，並確認支援的驅動程式和硬體已安裝並正確設定。
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- DRV_INSTALL message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935074"
---
# <a name="drv_install-message"></a><span data-ttu-id="27817-105">WINSPOOL.DRV \_ 安裝訊息</span><span class="sxs-lookup"><span data-stu-id="27817-105">DRV\_INSTALL message</span></span>

<span data-ttu-id="27817-106">通知驅動程式正在安裝。</span><span class="sxs-lookup"><span data-stu-id="27817-106">Notifies the driver that is it being installed.</span></span> <span data-ttu-id="27817-107">驅動程式應該建立並初始化任何所需的登錄機碼和值，並確認支援的驅動程式和硬體已安裝並正確設定。</span><span class="sxs-lookup"><span data-stu-id="27817-107">The driver should create and initialize any needed registry keys and values and verify that the supporting drivers and hardware are installed and properly configured.</span></span>

## <a name="parameters"></a><span data-ttu-id="27817-108">參數</span><span class="sxs-lookup"><span data-stu-id="27817-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27817-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="27817-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="27817-110">可安裝驅動程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27817-110">Identifier of the installable driver.</span></span> <span data-ttu-id="27817-111">這與先前 [**Winspool.drv \_ 開啟**](drv-open.md) 訊息中的驅動程式所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="27817-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="27817-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="27817-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="27817-113">可安裝的驅動程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="27817-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="27817-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="27817-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="27817-115">[**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)結構的位址或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="27817-115">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="27817-116">如果指定了結構，它就會包含與驅動程式相關聯的登錄機碼和值的名稱。</span><span class="sxs-lookup"><span data-stu-id="27817-116">If a structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27817-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="27817-117">Return Value</span></span>

<span data-ttu-id="27817-118">傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="27817-118">Returns one of these values:</span></span>



| <span data-ttu-id="27817-119">需求</span><span class="sxs-lookup"><span data-stu-id="27817-119">Requirement</span></span> | <span data-ttu-id="27817-120">值</span><span class="sxs-lookup"><span data-stu-id="27817-120">Value</span></span> |
|-----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="27817-121">DRVCNF \_ 確定</span><span class="sxs-lookup"><span data-stu-id="27817-121">DRVCNF\_OK</span></span>      | <span data-ttu-id="27817-122">安裝成功;不需要採取任何進一步的動作。</span><span class="sxs-lookup"><span data-stu-id="27817-122">The installation is successful; no further action is required.</span></span>                             |
| <span data-ttu-id="27817-123">DRVCNF \_ 取消</span><span class="sxs-lookup"><span data-stu-id="27817-123">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="27817-124">安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="27817-124">The installation failed..</span></span>                                                                  |
| <span data-ttu-id="27817-125">DRVCNF \_ 重新開機</span><span class="sxs-lookup"><span data-stu-id="27817-125">DRVCNF\_RESTART</span></span> | <span data-ttu-id="27817-126">安裝成功，但在系統重新開機之前不會生效。</span><span class="sxs-lookup"><span data-stu-id="27817-126">The installation is successful, but it does not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="27817-127">備註</span><span class="sxs-lookup"><span data-stu-id="27817-127">Remarks</span></span>

<span data-ttu-id="27817-128">未使用 *lParam1* 參數。</span><span class="sxs-lookup"><span data-stu-id="27817-128">The *lParam1* parameter is not used.</span></span>

<span data-ttu-id="27817-129">有些可安裝的驅動程式會將設定資訊附加至指派給與驅動程式相關聯之登錄值的值。</span><span class="sxs-lookup"><span data-stu-id="27817-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="27817-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="27817-130">Requirements</span></span>



| <span data-ttu-id="27817-131">需求</span><span class="sxs-lookup"><span data-stu-id="27817-131">Requirement</span></span> | <span data-ttu-id="27817-132">值</span><span class="sxs-lookup"><span data-stu-id="27817-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27817-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27817-133">Minimum supported client</span></span><br/> | <span data-ttu-id="27817-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27817-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="27817-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27817-135">Minimum supported server</span></span><br/> | <span data-ttu-id="27817-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27817-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="27817-137">標頭</span><span class="sxs-lookup"><span data-stu-id="27817-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="27817-138"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="27817-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27817-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27817-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27817-140">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="27817-140">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="27817-141">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="27817-141">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

