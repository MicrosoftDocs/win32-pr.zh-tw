---
title: ITsSbSession TargetName 屬性
description: 抓取建立此會話的目標名稱。
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- TargetName 屬性遠端桌面服務
- TargetName 屬性遠端桌面服務，ITsSbSession 介面
- ITsSbSession 介面遠端桌面服務，TargetName 屬性
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc703a32faedd250115da0b95215e620a8c15e19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970458"
---
# <a name="itssbsessiontargetname-property"></a><span data-ttu-id="e349b-106">ITsSbSession：： TargetName 屬性</span><span class="sxs-lookup"><span data-stu-id="e349b-106">ITsSbSession::TargetName property</span></span>

<span data-ttu-id="e349b-107">抓取建立此會話的目標名稱。</span><span class="sxs-lookup"><span data-stu-id="e349b-107">Retrieves the name of the target on which this session was created.</span></span>

<span data-ttu-id="e349b-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e349b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e349b-109">語法</span><span class="sxs-lookup"><span data-stu-id="e349b-109">Syntax</span></span>


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a><span data-ttu-id="e349b-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e349b-110">Property value</span></span>

<span data-ttu-id="e349b-111">**BSTR** 變數的指標，此變數會接收建立此會話的目標名稱。</span><span class="sxs-lookup"><span data-stu-id="e349b-111">A pointer to a **BSTR** variable that receives the name of the target on which this session was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="e349b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e349b-112">Requirements</span></span>



| <span data-ttu-id="e349b-113">需求</span><span class="sxs-lookup"><span data-stu-id="e349b-113">Requirement</span></span> | <span data-ttu-id="e349b-114">值</span><span class="sxs-lookup"><span data-stu-id="e349b-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e349b-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e349b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e349b-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="e349b-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="e349b-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e349b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e349b-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e349b-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="e349b-119">Idl</span><span class="sxs-lookup"><span data-stu-id="e349b-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e349b-120"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e349b-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e349b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e349b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e349b-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="e349b-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





