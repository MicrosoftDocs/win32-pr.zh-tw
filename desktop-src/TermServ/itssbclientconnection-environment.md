---
title: ITsSbClientConnection 環境屬性
description: 抓取物件，此物件包含裝載目的電腦之環境的相關資訊。
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- 環境屬性遠端桌面服務
- 環境屬性遠端桌面服務，ITsSbClientConnection 介面
- ITsSbClientConnection 介面遠端桌面服務，環境屬性
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18018c8f8fc5e7d017809cf5fe109db7c52712c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465980"
---
# <a name="itssbclientconnectionenvironment-property"></a><span data-ttu-id="b3ce3-106">ITsSbClientConnection：：環境屬性</span><span class="sxs-lookup"><span data-stu-id="b3ce3-106">ITsSbClientConnection::Environment property</span></span>

<span data-ttu-id="b3ce3-107">抓取物件，此物件包含裝載目的電腦之環境的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b3ce3-107">Retrieves an object that contains information about the environment that hosts the target computer.</span></span> <span data-ttu-id="b3ce3-108">例如，在虛擬桌面案例中，此物件會包含裝載虛擬機器之電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b3ce3-108">For example, in a virtual desktop scenario, this object would contain information about the computer that hosts the virtual machine.</span></span>

<span data-ttu-id="b3ce3-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b3ce3-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ce3-110">語法</span><span class="sxs-lookup"><span data-stu-id="b3ce3-110">Syntax</span></span>


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a><span data-ttu-id="b3ce3-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="b3ce3-111">Property value</span></span>

<span data-ttu-id="b3ce3-112">指向 [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) 環境物件指標的指標。</span><span class="sxs-lookup"><span data-stu-id="b3ce3-112">A pointer to a pointer to an [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) environment object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b3ce3-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b3ce3-113">Error codes</span></span>

<span data-ttu-id="b3ce3-114">如果方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b3ce3-114">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3ce3-115">否則，它會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b3ce3-115">Otherwise, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="b3ce3-116">可能的值包括（但不限於）下列清單中的值。</span><span class="sxs-lookup"><span data-stu-id="b3ce3-116">Possible values include, but are not limited to, those in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b3ce3-117">E \_ 指標</span><span class="sxs-lookup"><span data-stu-id="b3ce3-117">E\_POINTER</span></span>
</dt> <dd>

<span data-ttu-id="b3ce3-118">找不到環境。</span><span class="sxs-lookup"><span data-stu-id="b3ce3-118">The environment was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3ce3-119">備註</span><span class="sxs-lookup"><span data-stu-id="b3ce3-119">Remarks</span></span>

<span data-ttu-id="b3ce3-120">協調流程外掛程式可以呼叫這個方法，以抓取目標虛擬機器的環境資訊。</span><span class="sxs-lookup"><span data-stu-id="b3ce3-120">An orchestration plug-in can call this method to retrieve environment information about a target virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3ce3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3ce3-121">Requirements</span></span>



| <span data-ttu-id="b3ce3-122">需求</span><span class="sxs-lookup"><span data-stu-id="b3ce3-122">Requirement</span></span> | <span data-ttu-id="b3ce3-123">值</span><span class="sxs-lookup"><span data-stu-id="b3ce3-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ce3-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3ce3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b3ce3-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="b3ce3-125">None supported</span></span><br/>                                                            |
| <span data-ttu-id="b3ce3-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3ce3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b3ce3-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3ce3-127">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="b3ce3-128">Idl</span><span class="sxs-lookup"><span data-stu-id="b3ce3-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3ce3-129"><dt>Sbtsv .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3ce3-129"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3ce3-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3ce3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ce3-131">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="b3ce3-131">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





