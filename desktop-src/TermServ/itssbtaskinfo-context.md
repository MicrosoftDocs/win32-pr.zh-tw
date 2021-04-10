---
title: ITsSbTaskInfo 內容屬性
description: 捕獲與工作相關聯的內容位元組。
ms.assetid: ce55ce2a-957f-4b50-b632-42079277102b
ms.tgt_platform: multiple
keywords:
- 內容屬性遠端桌面服務
- CoNtext 屬性遠端桌面服務，ITsSbTaskInfo 介面
- ITsSbTaskInfo 介面遠端桌面服務、內容屬性
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Context
- ITsSbTaskInfo.get_Context
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2adc4715f23b2c23ac6dfbdcdd8a489b2b0f5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106085"
---
# <a name="itssbtaskinfocontext-property"></a><span data-ttu-id="3455f-106">ITsSbTaskInfo：： CoNtext 屬性</span><span class="sxs-lookup"><span data-stu-id="3455f-106">ITsSbTaskInfo::Context property</span></span>

<span data-ttu-id="3455f-107">捕獲與工作相關聯的內容位元組。</span><span class="sxs-lookup"><span data-stu-id="3455f-107">Retrieves the context bytes associated with the task.</span></span>

<span data-ttu-id="3455f-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="3455f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3455f-109">語法</span><span class="sxs-lookup"><span data-stu-id="3455f-109">Syntax</span></span>


```C++
HRESULT get_Context(
  [out, retval] SAFEARRAY(BYTE) *pContext
);
```



## <a name="property-value"></a><span data-ttu-id="3455f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="3455f-110">Property value</span></span>

<span data-ttu-id="3455f-111">工作的內容。</span><span class="sxs-lookup"><span data-stu-id="3455f-111">The context of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="3455f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3455f-112">Requirements</span></span>



| <span data-ttu-id="3455f-113">需求</span><span class="sxs-lookup"><span data-stu-id="3455f-113">Requirement</span></span> | <span data-ttu-id="3455f-114">值</span><span class="sxs-lookup"><span data-stu-id="3455f-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3455f-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3455f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3455f-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="3455f-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="3455f-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3455f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3455f-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3455f-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="3455f-119">Idl</span><span class="sxs-lookup"><span data-stu-id="3455f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3455f-120"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3455f-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3455f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3455f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3455f-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="3455f-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





