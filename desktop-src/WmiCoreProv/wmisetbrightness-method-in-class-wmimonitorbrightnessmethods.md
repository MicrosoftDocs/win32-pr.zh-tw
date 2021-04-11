---
description: 設定電腦監視器的顯示亮度。
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: WmiMonitorBrightnessMethods 類別的 WmiSetBrightness 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 599610b0d81de283d97ca347486c4adcbe0103dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026965"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="1c181-103">WmiMonitorBrightnessMethods 類別的 WmiSetBrightness 方法</span><span class="sxs-lookup"><span data-stu-id="1c181-103">WmiSetBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="1c181-104">**WmiSetBrightness** 方法會設定電腦監視器的顯示亮度。</span><span class="sxs-lookup"><span data-stu-id="1c181-104">The **WmiSetBrightness** method sets the display brightness of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c181-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c181-105">Syntax</span></span>


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="1c181-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c181-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c181-107">*逾時*</span><span class="sxs-lookup"><span data-stu-id="1c181-107">*Timeout*</span></span> 
</dt> <dd>

<span data-ttu-id="1c181-108">Timeout （以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1c181-108">Timeout, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="1c181-109">*亮度*</span><span class="sxs-lookup"><span data-stu-id="1c181-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="1c181-110">亮度（以百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="1c181-110">Brightness, in percent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c181-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c181-111">Return value</span></span>

<span data-ttu-id="1c181-112">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="1c181-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="1c181-113">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="1c181-113">Any other number indicates an error.</span></span> <span data-ttu-id="1c181-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="1c181-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="1c181-115">範例</span><span class="sxs-lookup"><span data-stu-id="1c181-115">Examples</span></span>

<span data-ttu-id="1c181-116">如需有關如何抓取及設定監視器亮度的詳細討論，請參閱「腳本撰寫者 [使用 PowerShell 來報告和設定監視器亮度](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) 的 blog」主題。</span><span class="sxs-lookup"><span data-stu-id="1c181-116">For an extended discussion of retrieving and setting monitor brightness, see the Scripting Guy's [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) blog topic.</span></span>

<span data-ttu-id="1c181-117">下列 PowerShell 範例會將監視的亮度設定為50%。</span><span class="sxs-lookup"><span data-stu-id="1c181-117">The following PowerShell sample sets the brightness of the monitor to 50%.</span></span>


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



## <a name="requirements"></a><span data-ttu-id="1c181-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c181-118">Requirements</span></span>



| <span data-ttu-id="1c181-119">需求</span><span class="sxs-lookup"><span data-stu-id="1c181-119">Requirement</span></span> | <span data-ttu-id="1c181-120">值</span><span class="sxs-lookup"><span data-stu-id="1c181-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c181-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c181-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1c181-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c181-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1c181-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c181-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1c181-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c181-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1c181-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="1c181-125">Namespace</span></span><br/>                | <span data-ttu-id="1c181-126">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="1c181-126">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1c181-127">MOF</span><span class="sxs-lookup"><span data-stu-id="1c181-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c181-128"><dt>WmiCore mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c181-128"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c181-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1c181-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c181-130"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c181-130"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c181-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c181-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c181-132">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="1c181-132">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="1c181-133">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="1c181-133">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

