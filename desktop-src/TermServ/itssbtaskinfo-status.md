---
title: ITsSbTaskInfo Status 屬性
description: 抓取 RDV 工作 \_ \_ 狀態列舉值，這個值表示工作的狀態。
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Status 屬性遠端桌面服務
- Status 屬性遠端桌面服務，ITsSbTaskInfo 介面
- ITsSbTaskInfo 介面遠端桌面服務，Status 屬性
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3206013c32ee6cf3323f19c9e95e89c8d6756eb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685860"
---
# <a name="itssbtaskinfostatus-property"></a><span data-ttu-id="77a1a-106">ITsSbTaskInfo：： Status 屬性</span><span class="sxs-lookup"><span data-stu-id="77a1a-106">ITsSbTaskInfo::Status property</span></span>

<span data-ttu-id="77a1a-107">抓取 [**RDV 工作 \_ \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) 列舉值，這個值表示工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="77a1a-107">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

<span data-ttu-id="77a1a-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="77a1a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="77a1a-109">語法</span><span class="sxs-lookup"><span data-stu-id="77a1a-109">Syntax</span></span>


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a><span data-ttu-id="77a1a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="77a1a-110">Property value</span></span>

<span data-ttu-id="77a1a-111">[**RDV 工作 \_ \_ 狀態**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)列舉值，表示工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="77a1a-111">An [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="77a1a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="77a1a-112">Requirements</span></span>



| <span data-ttu-id="77a1a-113">需求</span><span class="sxs-lookup"><span data-stu-id="77a1a-113">Requirement</span></span> | <span data-ttu-id="77a1a-114">值</span><span class="sxs-lookup"><span data-stu-id="77a1a-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="77a1a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77a1a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="77a1a-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="77a1a-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="77a1a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77a1a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="77a1a-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77a1a-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="77a1a-119">Idl</span><span class="sxs-lookup"><span data-stu-id="77a1a-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="77a1a-120"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="77a1a-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77a1a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77a1a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77a1a-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="77a1a-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





