---
title: 'DRV_OPEN 訊息 (Mmsystem .h) '
description: 指示驅動程式開啟新的實例。
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- DRV_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53c56e62cb85f09a3846c6d95d723b9fa05d95a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106223"
---
# <a name="drv_open-message"></a><span data-ttu-id="426b6-104">WINSPOOL.DRV \_ 開啟的訊息</span><span class="sxs-lookup"><span data-stu-id="426b6-104">DRV\_OPEN message</span></span>

<span data-ttu-id="426b6-105">指示驅動程式開啟新的實例。</span><span class="sxs-lookup"><span data-stu-id="426b6-105">Directs the driver to open an new instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="426b6-106">參數</span><span class="sxs-lookup"><span data-stu-id="426b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="426b6-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="426b6-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="426b6-108">可安裝驅動程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="426b6-108">Identifier of the installable driver.</span></span>

</dd> <dt>

<span data-ttu-id="426b6-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="426b6-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="426b6-110">可安裝的驅動程式實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="426b6-110">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="426b6-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="426b6-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="426b6-112">以 null 結束之寬字元字串的位址，指定用來開啟實例的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="426b6-112">Address of a null-terminated, wide-character string that specifies configuration information used to open the instance.</span></span> <span data-ttu-id="426b6-113">如果沒有可用的設定資訊，則此字串為空白或參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="426b6-113">If no configuration information is available, either this string is empty or the parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="426b6-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="426b6-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="426b6-115">32位驅動程式特定的資料。</span><span class="sxs-lookup"><span data-stu-id="426b6-115">32-bit driver-specific data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="426b6-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="426b6-116">Return Value</span></span>

<span data-ttu-id="426b6-117">如果成功，則傳回非零值，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="426b6-117">Returns a nonzero value if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="426b6-118">備註</span><span class="sxs-lookup"><span data-stu-id="426b6-118">Remarks</span></span>

<span data-ttu-id="426b6-119">如果驅動程式傳回非零值，系統會使用該值做為驅動程式識別碼， (*dwDriverId* 參數在其後傳送至驅動程式實例的訊息中) 。</span><span class="sxs-lookup"><span data-stu-id="426b6-119">If the driver returns a nonzero value, the system uses that value as the driver identifier (the *dwDriverId* parameter) in messages it subsequently sends to the driver instance.</span></span> <span data-ttu-id="426b6-120">驅動程式可以傳回任何類型的值做為識別碼。</span><span class="sxs-lookup"><span data-stu-id="426b6-120">The driver can return any type of value as the identifier.</span></span> <span data-ttu-id="426b6-121">例如，某些驅動程式會傳回指向實例特定資訊的記憶體位址。</span><span class="sxs-lookup"><span data-stu-id="426b6-121">For example, some drivers return memory addresses that point to instance-specific information.</span></span> <span data-ttu-id="426b6-122">使用這個方法來指定驅動程式實例的識別碼，可讓驅動程式在處理訊息時立即存取訊號。</span><span class="sxs-lookup"><span data-stu-id="426b6-122">Using this method of specifying identifiers for a driver instance gives the drivers ready access to the information while they are processing messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="426b6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="426b6-123">Requirements</span></span>



| <span data-ttu-id="426b6-124">需求</span><span class="sxs-lookup"><span data-stu-id="426b6-124">Requirement</span></span> | <span data-ttu-id="426b6-125">值</span><span class="sxs-lookup"><span data-stu-id="426b6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="426b6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="426b6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="426b6-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="426b6-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="426b6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="426b6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="426b6-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="426b6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="426b6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="426b6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="426b6-131"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="426b6-131"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="426b6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="426b6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="426b6-133">可安裝的驅動程式</span><span class="sxs-lookup"><span data-stu-id="426b6-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="426b6-134">可安裝的驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="426b6-134">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





