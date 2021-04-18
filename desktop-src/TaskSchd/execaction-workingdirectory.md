---
title: ExecAction. WorkingDirectory 屬性
description: 針對腳本，取得或設定包含可執行檔或可執行檔所使用之檔案的目錄。
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- WorkingDirectory 屬性工作排程器
- WorkingDirectory 屬性工作排程器，ExecAction 物件
- ExecAction 物件工作排程器、WorkingDirectory 屬性
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968753"
---
# <a name="execactionworkingdirectory-property"></a><span data-ttu-id="5eec2-106">ExecAction. WorkingDirectory 屬性</span><span class="sxs-lookup"><span data-stu-id="5eec2-106">ExecAction.WorkingDirectory property</span></span>

<span data-ttu-id="5eec2-107">針對腳本，取得或設定包含可執行檔或可執行檔所使用之檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="5eec2-107">For scripting, gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eec2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5eec2-108">Syntax</span></span>


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a><span data-ttu-id="5eec2-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="5eec2-109">Property value</span></span>

<span data-ttu-id="5eec2-110">包含可執行檔或可執行檔所使用之檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="5eec2-110">The directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eec2-111">備註</span><span class="sxs-lookup"><span data-stu-id="5eec2-111">Remarks</span></span>

<span data-ttu-id="5eec2-112">讀取或寫入 XML 時，會在工作排程器架構的 [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) 元素中指定應用程式的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="5eec2-112">When reading or writing XML, the working directory of the application is specified in the [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="5eec2-113">檢查此路徑以確定它在註冊工作時有效，而不是在設定這個屬性時有效。</span><span class="sxs-lookup"><span data-stu-id="5eec2-113">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eec2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5eec2-114">Requirements</span></span>



| <span data-ttu-id="5eec2-115">需求</span><span class="sxs-lookup"><span data-stu-id="5eec2-115">Requirement</span></span> | <span data-ttu-id="5eec2-116">值</span><span class="sxs-lookup"><span data-stu-id="5eec2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5eec2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5eec2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5eec2-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5eec2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5eec2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5eec2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5eec2-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5eec2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5eec2-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5eec2-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="5eec2-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5eec2-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5eec2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5eec2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5eec2-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5eec2-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eec2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5eec2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eec2-126">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="5eec2-126">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="5eec2-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="5eec2-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





