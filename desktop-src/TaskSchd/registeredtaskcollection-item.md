---
title: RegisteredTaskCollection 專案屬性
description: 針對腳本，從集合取得指定的已註冊工作。
ms.assetid: 8b396478-4cd9-426c-afe8-29539ff0b859
keywords:
- Item 屬性工作排程器
- 專案屬性工作排程器，RegisteredTaskCollection 物件
- RegisteredTaskCollection 物件工作排程器，Item 屬性
topic_type:
- apiref
api_name:
- RegisteredTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ec79eb526b85b88afc0e5747a80b45f07b99a9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969145"
---
# <a name="registeredtaskcollectionitem-property"></a><span data-ttu-id="569c6-106">RegisteredTaskCollection 專案屬性</span><span class="sxs-lookup"><span data-stu-id="569c6-106">RegisteredTaskCollection.Item property</span></span>

<span data-ttu-id="569c6-107">針對腳本，從集合取得指定的已註冊工作。</span><span class="sxs-lookup"><span data-stu-id="569c6-107">For scripting, gets the specified registered task from the collection.</span></span>

<span data-ttu-id="569c6-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="569c6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="569c6-109">語法</span><span class="sxs-lookup"><span data-stu-id="569c6-109">Syntax</span></span>


```VB
RegisteredTaskCollection.Item( _
  ByVal Index _
) As RegisteredTask
```



## <a name="property-value"></a><span data-ttu-id="569c6-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="569c6-110">Property value</span></span>

<span data-ttu-id="569c6-111">[**RegisteredTask**](registeredtask.md)物件，其中包含已註冊的工作。</span><span class="sxs-lookup"><span data-stu-id="569c6-111">A [**RegisteredTask**](registeredtask.md) object that contains the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="569c6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="569c6-112">Requirements</span></span>



| <span data-ttu-id="569c6-113">需求</span><span class="sxs-lookup"><span data-stu-id="569c6-113">Requirement</span></span> | <span data-ttu-id="569c6-114">值</span><span class="sxs-lookup"><span data-stu-id="569c6-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="569c6-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="569c6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="569c6-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="569c6-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="569c6-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="569c6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="569c6-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="569c6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="569c6-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="569c6-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="569c6-120"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="569c6-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="569c6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="569c6-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="569c6-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="569c6-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="569c6-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="569c6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="569c6-124">工作排程器</span><span class="sxs-lookup"><span data-stu-id="569c6-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





