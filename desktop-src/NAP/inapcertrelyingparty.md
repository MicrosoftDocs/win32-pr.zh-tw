---
title: 'INapCertRelyingParty 介面 (NapCertRelyingParty .h) '
description: 憑證-信賴憑證者必須使用來與 NapAgent 通訊。
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- INapCertRelyingParty 介面 NAP
- INapCertRelyingParty 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapCertRelyingParty
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b4439389c6ee65076f710bb6ea752c73a51ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025267"
---
# <a name="inapcertrelyingparty-interface"></a><span data-ttu-id="15d4b-105">INapCertRelyingParty 介面</span><span class="sxs-lookup"><span data-stu-id="15d4b-105">INapCertRelyingParty interface</span></span>

> [!Note]  
> <span data-ttu-id="15d4b-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="15d4b-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="15d4b-107">**INapCertRelyingParty** 介面提供憑證信賴憑證者必須用來與 NapAgent 進行通訊的方法。</span><span class="sxs-lookup"><span data-stu-id="15d4b-107">The **INapCertRelyingParty** interface provides methods that certificate-relying parties must use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="15d4b-108">成員</span><span class="sxs-lookup"><span data-stu-id="15d4b-108">Members</span></span>

<span data-ttu-id="15d4b-109">**INapCertRelyingParty** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="15d4b-109">The **INapCertRelyingParty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="15d4b-110">**INapCertRelyingParty** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="15d4b-110">**INapCertRelyingParty** also has these types of members:</span></span>

-   [<span data-ttu-id="15d4b-111">方法</span><span class="sxs-lookup"><span data-stu-id="15d4b-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="15d4b-112">方法</span><span class="sxs-lookup"><span data-stu-id="15d4b-112">Methods</span></span>

<span data-ttu-id="15d4b-113">**INapCertRelyingParty** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="15d4b-113">The **INapCertRelyingParty** interface has these methods.</span></span>



| <span data-ttu-id="15d4b-114">方法</span><span class="sxs-lookup"><span data-stu-id="15d4b-114">Method</span></span>                                                                                                        | <span data-ttu-id="15d4b-115">描述</span><span class="sxs-lookup"><span data-stu-id="15d4b-115">Description</span></span>                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="15d4b-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span><span class="sxs-lookup"><span data-stu-id="15d4b-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span></span>](inapcertrelyingparty-getsubscribedrelyingparties.md) | <span data-ttu-id="15d4b-117">取得已訂閱的信賴憑證者清單。</span><span class="sxs-lookup"><span data-stu-id="15d4b-117">Gets a list of relying parties that have subscribed.</span></span><br/>                 |
| [<span data-ttu-id="15d4b-118">**INapCertRelyingParty::SubscribeCertByGroup**</span><span class="sxs-lookup"><span data-stu-id="15d4b-118">**INapCertRelyingParty::SubscribeCertByGroup**</span></span>](inapcertrelyingparty-subscribecertbygroup.md)               | <span data-ttu-id="15d4b-119">訂閱已註冊的健康情況憑證伺服器 (HCS) 。</span><span class="sxs-lookup"><span data-stu-id="15d4b-119">Subscribes to an already-registered health certificate server (HCS).</span></span><br/> |
| [<span data-ttu-id="15d4b-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span><span class="sxs-lookup"><span data-stu-id="15d4b-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span></span>](inapcertrelyingparty-unsubscribecertbygroup.md)           | <span data-ttu-id="15d4b-121">從 HCS 伺服器取消訂閱。</span><span class="sxs-lookup"><span data-stu-id="15d4b-121">Unsubscribes from an HCS server.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="15d4b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="15d4b-122">Requirements</span></span>



| <span data-ttu-id="15d4b-123">需求</span><span class="sxs-lookup"><span data-stu-id="15d4b-123">Requirement</span></span> | <span data-ttu-id="15d4b-124">值</span><span class="sxs-lookup"><span data-stu-id="15d4b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15d4b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15d4b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="15d4b-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15d4b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15d4b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15d4b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="15d4b-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15d4b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="15d4b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="15d4b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="15d4b-130"><dt>NapCertRelyingParty。h</dt></span><span class="sxs-lookup"><span data-stu-id="15d4b-130"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="15d4b-131">Idl</span><span class="sxs-lookup"><span data-stu-id="15d4b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15d4b-132"><dt>NapCertRelyingParty .idl</dt></span><span class="sxs-lookup"><span data-stu-id="15d4b-132"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15d4b-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15d4b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d4b-134">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="15d4b-134">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="15d4b-135">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="15d4b-135">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

