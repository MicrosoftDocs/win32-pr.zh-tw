---
description: WmiRevertToPolicyBrightness 方法是用來將亮度還原至原則設定。 這個方法不會影響 ALS 亮度設定。
ms.assetid: 9a520c3f-3563-4ef4-b397-14e487c8e8bb
title: WmiMonitorBrightnessMethods 類別的 WmiRevertToPolicyBrightness 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiRevertToPolicyBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 03e1ed74486c7a5a2f2c61dc858e715850ec516e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193264"
---
# <a name="wmireverttopolicybrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="6284e-104">WmiMonitorBrightnessMethods 類別的 WmiRevertToPolicyBrightness 方法</span><span class="sxs-lookup"><span data-stu-id="6284e-104">WmiRevertToPolicyBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="6284e-105">**WmiRevertToPolicyBrightness** 方法是用來將亮度還原至原則設定。</span><span class="sxs-lookup"><span data-stu-id="6284e-105">The **WmiRevertToPolicyBrightness** method is used to revert the brightness to the policy setting.</span></span> <span data-ttu-id="6284e-106">這個方法不會影響 ALS 亮度設定。</span><span class="sxs-lookup"><span data-stu-id="6284e-106">This method has no effect on the ALS brightness settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="6284e-107">語法</span><span class="sxs-lookup"><span data-stu-id="6284e-107">Syntax</span></span>


```mof
uint32 WmiRevertToPolicyBrightness();
```



## <a name="parameters"></a><span data-ttu-id="6284e-108">參數</span><span class="sxs-lookup"><span data-stu-id="6284e-108">Parameters</span></span>

<span data-ttu-id="6284e-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6284e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6284e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6284e-110">Return value</span></span>

<span data-ttu-id="6284e-111">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="6284e-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="6284e-112">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="6284e-112">Any other number indicates an error.</span></span> <span data-ttu-id="6284e-113">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="6284e-113">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="6284e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6284e-114">Requirements</span></span>



| <span data-ttu-id="6284e-115">需求</span><span class="sxs-lookup"><span data-stu-id="6284e-115">Requirement</span></span> | <span data-ttu-id="6284e-116">值</span><span class="sxs-lookup"><span data-stu-id="6284e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6284e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6284e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6284e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6284e-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6284e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6284e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6284e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6284e-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6284e-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="6284e-121">Namespace</span></span><br/>                | <span data-ttu-id="6284e-122">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="6284e-122">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="6284e-123">MOF</span><span class="sxs-lookup"><span data-stu-id="6284e-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6284e-124"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="6284e-124"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="6284e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6284e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6284e-126"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6284e-126"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6284e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6284e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6284e-128">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="6284e-128">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="6284e-129">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="6284e-129">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

