---
description: 用來控制環境光線感應器的亮度狀態。
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: WmiMonitorBrightnessMethods 類別的 WmiSetALSBrightnessState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 593b007f75c7eb134de4bb4c9f83c7246e9a51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982757"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="83ad4-103">WmiMonitorBrightnessMethods 類別的 WmiSetALSBrightnessState 方法</span><span class="sxs-lookup"><span data-stu-id="83ad4-103">WmiSetALSBrightnessState method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="83ad4-104">**WmiSetALSBrightnessState** 方法是用來控制環境光線感應器的亮度狀態。</span><span class="sxs-lookup"><span data-stu-id="83ad4-104">The **WmiSetALSBrightnessState** method is used to control the ambient light sensor brightness state.</span></span> <span data-ttu-id="83ad4-105">如果使用 [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) 方法建立了使用中的亮度覆寫，該覆寫將優先于使用此方法的 ALS 亮度設定。</span><span class="sxs-lookup"><span data-stu-id="83ad4-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="83ad4-106">若要讓已啟用的 ALS 亮度覆寫生效，必須使用 [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) 方法來還原亮度原則。</span><span class="sxs-lookup"><span data-stu-id="83ad4-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="83ad4-107">語法</span><span class="sxs-lookup"><span data-stu-id="83ad4-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a><span data-ttu-id="83ad4-108">參數</span><span class="sxs-lookup"><span data-stu-id="83ad4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83ad4-109">*State*</span><span class="sxs-lookup"><span data-stu-id="83ad4-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="83ad4-110">ALS 亮度狀態。</span><span class="sxs-lookup"><span data-stu-id="83ad4-110">ALS brightness state.</span></span> <span data-ttu-id="83ad4-111">False 會停用 ALS 亮度覆寫，並為其啟用。</span><span class="sxs-lookup"><span data-stu-id="83ad4-111">False disables the ALS brightness override and true enables it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83ad4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="83ad4-112">Return value</span></span>

<span data-ttu-id="83ad4-113">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="83ad4-113">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="83ad4-114">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="83ad4-114">Any other number indicates an error.</span></span> <span data-ttu-id="83ad4-115">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="83ad4-115">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="83ad4-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="83ad4-116">Requirements</span></span>



| <span data-ttu-id="83ad4-117">需求</span><span class="sxs-lookup"><span data-stu-id="83ad4-117">Requirement</span></span> | <span data-ttu-id="83ad4-118">值</span><span class="sxs-lookup"><span data-stu-id="83ad4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83ad4-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83ad4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="83ad4-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83ad4-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="83ad4-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83ad4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="83ad4-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83ad4-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="83ad4-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="83ad4-123">Namespace</span></span><br/>                | <span data-ttu-id="83ad4-124">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="83ad4-124">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="83ad4-125">MOF</span><span class="sxs-lookup"><span data-stu-id="83ad4-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83ad4-126"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="83ad4-126"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="83ad4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="83ad4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83ad4-128"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83ad4-128"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83ad4-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83ad4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83ad4-130">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="83ad4-130">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="83ad4-131">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="83ad4-131">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

