---
description: 用來設定環境光源感應器的亮度值。
ms.assetid: 8b3ec692-4043-42b3-8dd6-7a147620e382
title: WmiMonitorBrightnessMethods 類別的 WmiSetALSBrightness 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 0768917f9197b6ee3de52877e031acbbdc8f9aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195403"
---
# <a name="wmisetalsbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="7d561-103">WmiMonitorBrightnessMethods 類別的 WmiSetALSBrightness 方法</span><span class="sxs-lookup"><span data-stu-id="7d561-103">WmiSetALSBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="7d561-104">**WmiSetALSBrightness** 方法是用來設定環境光源感應器亮度值。</span><span class="sxs-lookup"><span data-stu-id="7d561-104">The **WmiSetALSBrightness** method is used to set the ambient light sensor brightness value.</span></span> <span data-ttu-id="7d561-105">如果使用 [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) 方法建立了使用中的亮度覆寫，該覆寫將優先于使用此方法的 ALS 亮度設定。</span><span class="sxs-lookup"><span data-stu-id="7d561-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="7d561-106">若要讓已啟用的 ALS 亮度覆寫生效，必須使用 [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) 方法來還原亮度原則。</span><span class="sxs-lookup"><span data-stu-id="7d561-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d561-107">語法</span><span class="sxs-lookup"><span data-stu-id="7d561-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightness(
   uint8 Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="7d561-108">參數</span><span class="sxs-lookup"><span data-stu-id="7d561-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d561-109">*亮度*</span><span class="sxs-lookup"><span data-stu-id="7d561-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="7d561-110">以百分比表示的 ALS 亮度。</span><span class="sxs-lookup"><span data-stu-id="7d561-110">The ALS brightness as a percentage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d561-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d561-111">Return value</span></span>

<span data-ttu-id="7d561-112">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="7d561-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="7d561-113">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="7d561-113">Any other number indicates an error.</span></span> <span data-ttu-id="7d561-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="7d561-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d561-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d561-115">Requirements</span></span>



| <span data-ttu-id="7d561-116">需求</span><span class="sxs-lookup"><span data-stu-id="7d561-116">Requirement</span></span> | <span data-ttu-id="7d561-117">值</span><span class="sxs-lookup"><span data-stu-id="7d561-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d561-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d561-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7d561-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d561-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7d561-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d561-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7d561-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d561-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7d561-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="7d561-122">Namespace</span></span><br/>                | <span data-ttu-id="7d561-123">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="7d561-123">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="7d561-124">MOF</span><span class="sxs-lookup"><span data-stu-id="7d561-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d561-125"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d561-125"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d561-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7d561-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d561-127"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d561-127"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d561-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d561-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d561-129">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="7d561-129">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="7d561-130">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="7d561-130">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

