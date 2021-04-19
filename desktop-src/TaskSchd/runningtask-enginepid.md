---
title: RunningTask. EnginePID 屬性
description: 針對腳本，取得正在執行工作之引擎 (進程) 的處理序識別碼。
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- EnginePID 屬性工作排程器
- EnginePID 屬性工作排程器，RunningTask 物件
- RunningTask 物件工作排程器、EnginePID 屬性
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969181"
---
# <a name="runningtaskenginepid-property"></a><span data-ttu-id="46734-106">RunningTask. EnginePID 屬性</span><span class="sxs-lookup"><span data-stu-id="46734-106">RunningTask.EnginePID property</span></span>

<span data-ttu-id="46734-107">針對腳本，取得正在執行工作之引擎 (進程) 的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="46734-107">For scripting, gets the process ID for the engine (process) which is running the task.</span></span>

<span data-ttu-id="46734-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="46734-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="46734-109">語法</span><span class="sxs-lookup"><span data-stu-id="46734-109">Syntax</span></span>


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a><span data-ttu-id="46734-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="46734-110">Property value</span></span>

<span data-ttu-id="46734-111">正在執行工作之引擎的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="46734-111">The process ID for the engine which is running the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="46734-112">備註</span><span class="sxs-lookup"><span data-stu-id="46734-112">Remarks</span></span>

<span data-ttu-id="46734-113">這個屬性所傳回的處理序識別碼無法直接附加至字串。</span><span class="sxs-lookup"><span data-stu-id="46734-113">The process ID returned by this property cannot be appended directly to a string.</span></span> <span data-ttu-id="46734-114">傳回的值必須先透過呼叫傳回值的 [CInt](/previous-versions//fctcwhw9(v=vs.85)) 函式，轉換成整數值。</span><span class="sxs-lookup"><span data-stu-id="46734-114">The returned value needs to be converted to an integer value first by calling the [CInt](/previous-versions//fctcwhw9(v=vs.85)) function on the returned value.</span></span>


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a><span data-ttu-id="46734-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="46734-115">Requirements</span></span>



| <span data-ttu-id="46734-116">需求</span><span class="sxs-lookup"><span data-stu-id="46734-116">Requirement</span></span> | <span data-ttu-id="46734-117">值</span><span class="sxs-lookup"><span data-stu-id="46734-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46734-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46734-118">Minimum supported client</span></span><br/> | <span data-ttu-id="46734-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46734-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="46734-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46734-120">Minimum supported server</span></span><br/> | <span data-ttu-id="46734-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46734-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46734-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="46734-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="46734-123"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="46734-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="46734-124">DLL</span><span class="sxs-lookup"><span data-stu-id="46734-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46734-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46734-125"><dt>Taskschd.dll</dt></span></span> </dl> |



 

