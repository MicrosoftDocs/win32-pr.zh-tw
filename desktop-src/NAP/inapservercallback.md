---
title: 'INapServerCallback 介面 (NapSystemHealthValidator .h) '
description: Shv 用來發出非同步要求完成的信號。
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- INapServerCallback 介面 NAP
- INapServerCallback 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464341"
---
# <a name="inapservercallback-interface"></a><span data-ttu-id="da915-105">INapServerCallback 介面</span><span class="sxs-lookup"><span data-stu-id="da915-105">INapServerCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="da915-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="da915-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="da915-107">**INapServerCallback** 會提供一種方法，讓 shv 用來指示非同步要求完成。</span><span class="sxs-lookup"><span data-stu-id="da915-107">The **INapServerCallback** provides a method that SHVs use to signal asynchronous request completion.</span></span>

## <a name="members"></a><span data-ttu-id="da915-108">成員</span><span class="sxs-lookup"><span data-stu-id="da915-108">Members</span></span>

<span data-ttu-id="da915-109">**INapServerCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="da915-109">The **INapServerCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="da915-110">**INapServerCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="da915-110">**INapServerCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="da915-111">方法</span><span class="sxs-lookup"><span data-stu-id="da915-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="da915-112">方法</span><span class="sxs-lookup"><span data-stu-id="da915-112">Methods</span></span>

<span data-ttu-id="da915-113">**INapServerCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="da915-113">The **INapServerCallback** interface has these methods.</span></span>



| <span data-ttu-id="da915-114">方法</span><span class="sxs-lookup"><span data-stu-id="da915-114">Method</span></span>                                                                         | <span data-ttu-id="da915-115">描述</span><span class="sxs-lookup"><span data-stu-id="da915-115">Description</span></span>                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="da915-116">**INapServerCallback：： OnComplete**</span><span class="sxs-lookup"><span data-stu-id="da915-116">**INapServerCallback::OnComplete**</span></span>](inapservercallback-oncomplete-method.md) | <span data-ttu-id="da915-117">由 Shv 用來指示非同步要求完成。</span><span class="sxs-lookup"><span data-stu-id="da915-117">Used by SHVs to signal asynchronous request completion.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="da915-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="da915-118">Requirements</span></span>



| <span data-ttu-id="da915-119">需求</span><span class="sxs-lookup"><span data-stu-id="da915-119">Requirement</span></span> | <span data-ttu-id="da915-120">值</span><span class="sxs-lookup"><span data-stu-id="da915-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da915-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da915-121">Minimum supported client</span></span><br/> | <span data-ttu-id="da915-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="da915-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="da915-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da915-123">Minimum supported server</span></span><br/> | <span data-ttu-id="da915-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da915-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da915-125">標頭</span><span class="sxs-lookup"><span data-stu-id="da915-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="da915-126"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="da915-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="da915-127">Idl</span><span class="sxs-lookup"><span data-stu-id="da915-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="da915-128"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="da915-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="da915-129">DLL</span><span class="sxs-lookup"><span data-stu-id="da915-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da915-130"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da915-130"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="da915-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da915-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da915-132">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="da915-132">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="da915-133">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="da915-133">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

