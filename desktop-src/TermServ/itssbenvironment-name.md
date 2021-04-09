---
title: ITsSbEnvironment Name 屬性
description: 抓取值，指出主控目的電腦之環境的名稱。
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Name 屬性遠端桌面服務
- Name 屬性遠端桌面服務，ITsSbEnvironment 介面
- ITsSbEnvironment 介面遠端桌面服務，Name 屬性
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934118"
---
# <a name="itssbenvironmentname-property"></a><span data-ttu-id="bb0c9-106">ITsSbEnvironment：： Name 屬性</span><span class="sxs-lookup"><span data-stu-id="bb0c9-106">ITsSbEnvironment::Name property</span></span>

<span data-ttu-id="bb0c9-107">抓取值，指出主控目的電腦之環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb0c9-107">Retrieves a value that indicates the name of the environment that hosts the target computer.</span></span>

<span data-ttu-id="bb0c9-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="bb0c9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb0c9-109">語法</span><span class="sxs-lookup"><span data-stu-id="bb0c9-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="bb0c9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="bb0c9-110">Property value</span></span>

<span data-ttu-id="bb0c9-111">包含環境名稱之 **BSTR** 變數的指標。</span><span class="sxs-lookup"><span data-stu-id="bb0c9-111">A pointer to a **BSTR** variable that contains the name of the environment.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb0c9-112">備註</span><span class="sxs-lookup"><span data-stu-id="bb0c9-112">Remarks</span></span>

<span data-ttu-id="bb0c9-113">這個方法會傳回遠端桌面連線代理人 (RD 連線代理人) 未直接使用的字串。</span><span class="sxs-lookup"><span data-stu-id="bb0c9-113">This method returns a string that is not directly used by Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="bb0c9-114">RD 連線代理人將此字串傳遞給資源外掛程式。</span><span class="sxs-lookup"><span data-stu-id="bb0c9-114">RD Connection Broker passes this string to resource plug-ins.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb0c9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb0c9-115">Requirements</span></span>



| <span data-ttu-id="bb0c9-116">需求</span><span class="sxs-lookup"><span data-stu-id="bb0c9-116">Requirement</span></span> | <span data-ttu-id="bb0c9-117">值</span><span class="sxs-lookup"><span data-stu-id="bb0c9-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bb0c9-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb0c9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb0c9-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="bb0c9-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="bb0c9-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb0c9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb0c9-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb0c9-121">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="bb0c9-122">Idl</span><span class="sxs-lookup"><span data-stu-id="bb0c9-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb0c9-123"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb0c9-123"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb0c9-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb0c9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb0c9-125">**ITsSbEnvironment**</span><span class="sxs-lookup"><span data-stu-id="bb0c9-125">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





