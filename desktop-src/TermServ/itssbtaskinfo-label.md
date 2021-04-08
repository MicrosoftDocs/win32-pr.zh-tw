---
title: ITsSbTaskInfo 標籤屬性
description: 抓取描述工作用途的標籤。
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- Label 屬性遠端桌面服務
- Label 屬性遠端桌面服務，ITsSbTaskInfo 介面
- ITsSbTaskInfo 介面遠端桌面服務，Label 屬性
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f85aaea366cf002d4ec1bacce8f29a6aa67fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686431"
---
# <a name="itssbtaskinfolabel-property"></a><span data-ttu-id="f1e41-106">ITsSbTaskInfo：： Label 屬性</span><span class="sxs-lookup"><span data-stu-id="f1e41-106">ITsSbTaskInfo::Label property</span></span>

<span data-ttu-id="f1e41-107">抓取描述工作用途的標籤。</span><span class="sxs-lookup"><span data-stu-id="f1e41-107">Retrieves the label that describes the purpose of the task.</span></span>

<span data-ttu-id="f1e41-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f1e41-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e41-109">語法</span><span class="sxs-lookup"><span data-stu-id="f1e41-109">Syntax</span></span>


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a><span data-ttu-id="f1e41-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="f1e41-110">Property value</span></span>

<span data-ttu-id="f1e41-111">包含標籤之 **BSTR** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="f1e41-111">A pointer to a **BSTR** value that contains the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e41-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1e41-112">Requirements</span></span>



| <span data-ttu-id="f1e41-113">需求</span><span class="sxs-lookup"><span data-stu-id="f1e41-113">Requirement</span></span> | <span data-ttu-id="f1e41-114">值</span><span class="sxs-lookup"><span data-stu-id="f1e41-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e41-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1e41-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e41-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="f1e41-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="f1e41-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1e41-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e41-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1e41-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="f1e41-119">Idl</span><span class="sxs-lookup"><span data-stu-id="f1e41-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1e41-120"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1e41-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e41-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1e41-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e41-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="f1e41-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





