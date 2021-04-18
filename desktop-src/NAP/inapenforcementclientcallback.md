---
title: 'INapEnforcementClientCallback 介面 (NapEnforcementClient .h) '
description: 強制用戶端必須實行，才能讓 NapAgent 與其通訊。
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- INapEnforcementClientCallback 介面 NAP
- INapEnforcementClientCallback 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d5c7e066115a6d51879775d9b8cfab3cbe4888
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965121"
---
# <a name="inapenforcementclientcallback-interface"></a><span data-ttu-id="d6006-105">INapEnforcementClientCallback 介面</span><span class="sxs-lookup"><span data-stu-id="d6006-105">INapEnforcementClientCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="d6006-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="d6006-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d6006-107">**INapEnforcementClientCallback** 介面提供強制用戶端必須執行的回呼方法，才能讓 NapAgent 與它們進行通訊。</span><span class="sxs-lookup"><span data-stu-id="d6006-107">The **INapEnforcementClientCallback** interface provides callback methods that enforcement clients must implement to enable the NapAgent to communicate with them.</span></span>

## <a name="members"></a><span data-ttu-id="d6006-108">成員</span><span class="sxs-lookup"><span data-stu-id="d6006-108">Members</span></span>

<span data-ttu-id="d6006-109">**INapEnforcementClientCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="d6006-109">The **INapEnforcementClientCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d6006-110">**INapEnforcementClientCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d6006-110">**INapEnforcementClientCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="d6006-111">方法</span><span class="sxs-lookup"><span data-stu-id="d6006-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d6006-112">方法</span><span class="sxs-lookup"><span data-stu-id="d6006-112">Methods</span></span>

<span data-ttu-id="d6006-113">**INapEnforcementClientCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d6006-113">The **INapEnforcementClientCallback** interface has these methods.</span></span>



| <span data-ttu-id="d6006-114">方法</span><span class="sxs-lookup"><span data-stu-id="d6006-114">Method</span></span>                                                                                                         | <span data-ttu-id="d6006-115">描述</span><span class="sxs-lookup"><span data-stu-id="d6006-115">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="d6006-116">**INapEnforcementClientCallback::GetConnections**</span><span class="sxs-lookup"><span data-stu-id="d6006-116">**INapEnforcementClientCallback::GetConnections**</span></span>](inapenforcementclientcallback-getconnections-method.md)   | <span data-ttu-id="d6006-117">供 NapAgent 用來取出連接。</span><span class="sxs-lookup"><span data-stu-id="d6006-117">Used by the NapAgent to retrieve connections.</span></span><br/>                         |
| [<span data-ttu-id="d6006-118">**INapEnforcementClientCallback::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="d6006-118">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md) | <span data-ttu-id="d6006-119">NapAgent 用來通知強制用戶端有 SoH 變更。</span><span class="sxs-lookup"><span data-stu-id="d6006-119">Used by the NapAgent to inform the enforcement client of SoH changes.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d6006-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6006-120">Requirements</span></span>



| <span data-ttu-id="d6006-121">需求</span><span class="sxs-lookup"><span data-stu-id="d6006-121">Requirement</span></span> | <span data-ttu-id="d6006-122">值</span><span class="sxs-lookup"><span data-stu-id="d6006-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6006-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6006-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d6006-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6006-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d6006-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6006-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d6006-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6006-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d6006-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d6006-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6006-128"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="d6006-128"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6006-129">Idl</span><span class="sxs-lookup"><span data-stu-id="d6006-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6006-130"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6006-130"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



 

