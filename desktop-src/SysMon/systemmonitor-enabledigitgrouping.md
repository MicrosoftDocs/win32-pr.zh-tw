---
title: SystemMonitor. EnableDigitGrouping 屬性
description: 抓取或設定值，這個值會決定 SYSMON 是否在顯示數值時使用數位群組。
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- EnableDigitGrouping 屬性 SysMon
- EnableDigitGrouping 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，EnableDigitGrouping 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384717"
---
# <a name="systemmonitorenabledigitgrouping-property"></a><span data-ttu-id="608a5-106">SystemMonitor. EnableDigitGrouping 屬性</span><span class="sxs-lookup"><span data-stu-id="608a5-106">SystemMonitor.EnableDigitGrouping property</span></span>

<span data-ttu-id="608a5-107">抓取或設定值，這個值會決定 SYSMON 是否在顯示數值時使用數位群組。</span><span class="sxs-lookup"><span data-stu-id="608a5-107">Retrieves or sets a value that determines if SYSMON uses digit grouping when displaying numeric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="608a5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="608a5-108">Syntax</span></span>


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a><span data-ttu-id="608a5-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="608a5-109">Property value</span></span>

<span data-ttu-id="608a5-110">若為 True，SYSMON 會在顯示數值時分組位數，例如1214。</span><span class="sxs-lookup"><span data-stu-id="608a5-110">If True, SYSMON will group digits when displaying numeric values, for example, 1,214.</span></span> <span data-ttu-id="608a5-111">如果為 False，則不會將數值分組，例如1214。</span><span class="sxs-lookup"><span data-stu-id="608a5-111">If False, numeric values are not grouped, for example, 1214.</span></span> <span data-ttu-id="608a5-112">預設值為 True。</span><span class="sxs-lookup"><span data-stu-id="608a5-112">True is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="608a5-113">備註</span><span class="sxs-lookup"><span data-stu-id="608a5-113">Remarks</span></span>

<span data-ttu-id="608a5-114">數位群組符號已當地語系化。</span><span class="sxs-lookup"><span data-stu-id="608a5-114">The digit grouping symbol is localized.</span></span>

## <a name="requirements"></a><span data-ttu-id="608a5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="608a5-115">Requirements</span></span>



| <span data-ttu-id="608a5-116">需求</span><span class="sxs-lookup"><span data-stu-id="608a5-116">Requirement</span></span> | <span data-ttu-id="608a5-117">值</span><span class="sxs-lookup"><span data-stu-id="608a5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="608a5-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="608a5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="608a5-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="608a5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="608a5-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="608a5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="608a5-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="608a5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="608a5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="608a5-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="608a5-123"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="608a5-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





