---
title: 'INapSystemHealthValidator 介面 (NapSystemHealthValidator .h) '
description: 必須由 SHV 開發人員執行，才能讓 NAP 系統與 SHV 進行通訊。
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- INapSystemHealthValidator 介面 NAP
- INapSystemHealthValidator 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685758"
---
# <a name="inapsystemhealthvalidator-interface"></a><span data-ttu-id="7c1a1-105">INapSystemHealthValidator 介面</span><span class="sxs-lookup"><span data-stu-id="7c1a1-105">INapSystemHealthValidator interface</span></span>

> [!Note]  
> <span data-ttu-id="7c1a1-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="7c1a1-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7c1a1-107">**INapSystemHealthValidator** 提供的方法必須由 SHV 開發人員執行，才能讓 NAP 系統與 shv 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="7c1a1-107">The **INapSystemHealthValidator** provides methods that must be implemented by SHV developers to enable the NAP system to communicate with an SHV.</span></span>

## <a name="members"></a><span data-ttu-id="7c1a1-108">成員</span><span class="sxs-lookup"><span data-stu-id="7c1a1-108">Members</span></span>

<span data-ttu-id="7c1a1-109">**INapSystemHealthValidator** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="7c1a1-109">The **INapSystemHealthValidator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7c1a1-110">**INapSystemHealthValidator** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7c1a1-110">**INapSystemHealthValidator** also has these types of members:</span></span>

-   [<span data-ttu-id="7c1a1-111">方法</span><span class="sxs-lookup"><span data-stu-id="7c1a1-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7c1a1-112">方法</span><span class="sxs-lookup"><span data-stu-id="7c1a1-112">Methods</span></span>

<span data-ttu-id="7c1a1-113">**INapSystemHealthValidator** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7c1a1-113">The **INapSystemHealthValidator** interface has these methods.</span></span>



| <span data-ttu-id="7c1a1-114">方法</span><span class="sxs-lookup"><span data-stu-id="7c1a1-114">Method</span></span>                                                                                   | <span data-ttu-id="7c1a1-115">描述</span><span class="sxs-lookup"><span data-stu-id="7c1a1-115">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c1a1-116">**INapSystemHealthValidator：： Validate**</span><span class="sxs-lookup"><span data-stu-id="7c1a1-116">**INapSystemHealthValidator::Validate**</span></span>](inapsystemhealthvalidator-validate-method.md) | <span data-ttu-id="7c1a1-117">NAP 系統會呼叫此應用程式定義的方法，以驗證從用戶端接收的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 。</span><span class="sxs-lookup"><span data-stu-id="7c1a1-117">The NAP system calls this application defined method to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="7c1a1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c1a1-118">Requirements</span></span>



| <span data-ttu-id="7c1a1-119">需求</span><span class="sxs-lookup"><span data-stu-id="7c1a1-119">Requirement</span></span> | <span data-ttu-id="7c1a1-120">值</span><span class="sxs-lookup"><span data-stu-id="7c1a1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c1a1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c1a1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7c1a1-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="7c1a1-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="7c1a1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c1a1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7c1a1-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c1a1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c1a1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7c1a1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c1a1-126"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a1-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c1a1-127">Idl</span><span class="sxs-lookup"><span data-stu-id="7c1a1-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c1a1-128"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a1-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c1a1-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c1a1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c1a1-130">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="7c1a1-130">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="7c1a1-131">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="7c1a1-131">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

