---
title: ITsSbSession 網域屬性
description: 抓取使用者的功能變數名稱。
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- 網域屬性遠端桌面服務
- 網域屬性遠端桌面服務、ITsSbSession 介面
- ITsSbSession 介面遠端桌面服務，網域屬性
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4501413888d17a70610160117df3ad03fde73b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969628"
---
# <a name="itssbsessiondomain-property"></a><span data-ttu-id="26e9c-106">ITsSbSession：:D omain 屬性</span><span class="sxs-lookup"><span data-stu-id="26e9c-106">ITsSbSession::Domain property</span></span>

<span data-ttu-id="26e9c-107">抓取使用者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="26e9c-107">Retrieves the domain name of the user.</span></span>

<span data-ttu-id="26e9c-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="26e9c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="26e9c-109">語法</span><span class="sxs-lookup"><span data-stu-id="26e9c-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a><span data-ttu-id="26e9c-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="26e9c-110">Property value</span></span>

<span data-ttu-id="26e9c-111">**BSTR** 變數的指標，此變數會接收使用者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="26e9c-111">A pointer to a **BSTR** variable that receives the domain name of the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="26e9c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="26e9c-112">Requirements</span></span>



| <span data-ttu-id="26e9c-113">需求</span><span class="sxs-lookup"><span data-stu-id="26e9c-113">Requirement</span></span> | <span data-ttu-id="26e9c-114">值</span><span class="sxs-lookup"><span data-stu-id="26e9c-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="26e9c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26e9c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="26e9c-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="26e9c-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="26e9c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26e9c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="26e9c-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26e9c-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="26e9c-119">Idl</span><span class="sxs-lookup"><span data-stu-id="26e9c-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26e9c-120"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="26e9c-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e9c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26e9c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e9c-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="26e9c-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





