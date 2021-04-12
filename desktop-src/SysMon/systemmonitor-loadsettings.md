---
title: SystemMonitor. LoadSettings 方法
description: 將 HTML 範本檔案中的計數器加入至系統監視器。
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- LoadSettings 方法 SysMon
- LoadSettings 方法 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，LoadSettings 方法
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384709"
---
# <a name="systemmonitorloadsettings-method"></a><span data-ttu-id="6d2cc-106">SystemMonitor. LoadSettings 方法</span><span class="sxs-lookup"><span data-stu-id="6d2cc-106">SystemMonitor.LoadSettings method</span></span>

<span data-ttu-id="6d2cc-107">將 HTML 範本檔案中的計數器加入至系統監視器。</span><span class="sxs-lookup"><span data-stu-id="6d2cc-107">Adds the counters in the HTML template file to the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2cc-108">語法</span><span class="sxs-lookup"><span data-stu-id="6d2cc-108">Syntax</span></span>


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a><span data-ttu-id="6d2cc-109">參數</span><span class="sxs-lookup"><span data-stu-id="6d2cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d2cc-110">*SettingsFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6d2cc-110">*SettingsFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2cc-111">HTML 字串，指定要加入至系統監視器的計數器。</span><span class="sxs-lookup"><span data-stu-id="6d2cc-111">HTML string that specifies the counters to add to the System Monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d2cc-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d2cc-112">Return value</span></span>

<span data-ttu-id="6d2cc-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6d2cc-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d2cc-114">備註</span><span class="sxs-lookup"><span data-stu-id="6d2cc-114">Remarks</span></span>

<span data-ttu-id="6d2cc-115">若要將系統監視器中的目前計數器儲存至 HTML 檔案，請呼叫 [**SystemMonitor**](systemmonitor-saveas.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6d2cc-115">To save the current counters in the System Monitor to an HTML file, call the [**SystemMonitor.SaveAs**](systemmonitor-saveas.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d2cc-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d2cc-116">Requirements</span></span>



| <span data-ttu-id="6d2cc-117">需求</span><span class="sxs-lookup"><span data-stu-id="6d2cc-117">Requirement</span></span> | <span data-ttu-id="6d2cc-118">值</span><span class="sxs-lookup"><span data-stu-id="6d2cc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2cc-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d2cc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d2cc-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d2cc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d2cc-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d2cc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d2cc-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d2cc-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d2cc-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6d2cc-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d2cc-124"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6d2cc-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d2cc-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d2cc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d2cc-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="6d2cc-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





