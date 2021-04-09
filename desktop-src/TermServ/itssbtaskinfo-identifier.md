---
title: ITsSbTaskInfo 識別碼屬性
description: 抓取由工作代理程式當做唯一識別碼使用的 GUID。
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- 識別碼屬性遠端桌面服務
- 識別碼屬性遠端桌面服務，ITsSbTaskInfo 介面
- ITsSbTaskInfo 介面遠端桌面服務，識別碼屬性
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 241ed2966e9ec92aa420af20ce142bcb724ad222
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686496"
---
# <a name="itssbtaskinfoidentifier-property"></a><span data-ttu-id="fa0b2-106">ITsSbTaskInfo：： Identifier 屬性</span><span class="sxs-lookup"><span data-stu-id="fa0b2-106">ITsSbTaskInfo::Identifier property</span></span>

<span data-ttu-id="fa0b2-107">抓取由工作代理程式當做唯一識別碼使用的 GUID。</span><span class="sxs-lookup"><span data-stu-id="fa0b2-107">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

<span data-ttu-id="fa0b2-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="fa0b2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa0b2-109">語法</span><span class="sxs-lookup"><span data-stu-id="fa0b2-109">Syntax</span></span>


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a><span data-ttu-id="fa0b2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="fa0b2-110">Property value</span></span>

<span data-ttu-id="fa0b2-111">接收 GUID 之 **BSTR** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="fa0b2-111">A pointer to a **BSTR** value that receives the GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa0b2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa0b2-112">Requirements</span></span>



| <span data-ttu-id="fa0b2-113">需求</span><span class="sxs-lookup"><span data-stu-id="fa0b2-113">Requirement</span></span> | <span data-ttu-id="fa0b2-114">值</span><span class="sxs-lookup"><span data-stu-id="fa0b2-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fa0b2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa0b2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fa0b2-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="fa0b2-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="fa0b2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa0b2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fa0b2-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa0b2-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="fa0b2-119">Idl</span><span class="sxs-lookup"><span data-stu-id="fa0b2-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa0b2-120"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b2-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa0b2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa0b2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa0b2-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="fa0b2-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





