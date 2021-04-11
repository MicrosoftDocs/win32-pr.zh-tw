---
title: SessionStateChangeTrigger Delay 屬性
description: 針對腳本，取得或設定值，這個值表示偵測到終端機伺服器會話狀態變更之後，啟動工作之前的延遲時間。
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Delay 屬性工作排程器
- Delay 屬性工作排程器，SessionStateChangeTrigger 物件
- SessionStateChangeTrigger 物件工作排程器，Delay 屬性
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094139"
---
# <a name="sessionstatechangetriggerdelay-property"></a><span data-ttu-id="a485d-106">SessionStateChangeTrigger Delay 屬性</span><span class="sxs-lookup"><span data-stu-id="a485d-106">SessionStateChangeTrigger.Delay property</span></span>

<span data-ttu-id="a485d-107">針對腳本，取得或設定值，這個值表示偵測到終端機伺服器會話狀態變更之後，啟動工作之前的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="a485d-107">For scripting, gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span> <span data-ttu-id="a485d-108">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="a485d-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="a485d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a485d-109">Syntax</span></span>


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="a485d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="a485d-110">Property value</span></span>

<span data-ttu-id="a485d-111">偵測到終端機伺服器會話狀態變更之後，啟動工作之前所發生的延遲。</span><span class="sxs-lookup"><span data-stu-id="a485d-111">The delay that takes place before a task is started after a Terminal Server session state change is detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="a485d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a485d-112">Requirements</span></span>



| <span data-ttu-id="a485d-113">需求</span><span class="sxs-lookup"><span data-stu-id="a485d-113">Requirement</span></span> | <span data-ttu-id="a485d-114">值</span><span class="sxs-lookup"><span data-stu-id="a485d-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a485d-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a485d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a485d-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a485d-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a485d-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a485d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a485d-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a485d-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a485d-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a485d-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="a485d-120"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a485d-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a485d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a485d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a485d-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a485d-122"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





