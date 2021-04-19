---
title: 'INapComponentConfig3 介面 (NapCommon .h) '
description: 提供適用于系統健全狀況驗證程式的 NAP 系統組態方法 (Shv) 設定和修改特定設定識別碼的設定資料。
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- INapComponentConfig3 介面 NAP
- INapComponentConfig3 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996175"
---
# <a name="inapcomponentconfig3-interface"></a><span data-ttu-id="3670d-105">INapComponentConfig3 介面</span><span class="sxs-lookup"><span data-stu-id="3670d-105">INapComponentConfig3 interface</span></span>

> [!Note]  
> <span data-ttu-id="3670d-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="3670d-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3670d-107">**INapComponentConfig3** 介面會為系統健康狀態驗證 (SHV 提供 NAP 系統組態方法，) 設定和修改特定設定識別碼的設定資料。</span><span class="sxs-lookup"><span data-stu-id="3670d-107">The **INapComponentConfig3** interface provides NAP system configuration methods for system health validators (SHVs) to set and modify configuration data for a specific configuration ID.</span></span>

> [!Note]  
> <span data-ttu-id="3670d-108">此介面會繼承 [**INapComponentConfig2**](inapcomponentconfig2.md) 的所有方法，因此應該改用。</span><span class="sxs-lookup"><span data-stu-id="3670d-108">This interface inherits all the methods of [**INapComponentConfig2**](inapcomponentconfig2.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="3670d-109">成員</span><span class="sxs-lookup"><span data-stu-id="3670d-109">Members</span></span>

<span data-ttu-id="3670d-110">**INapComponentConfig3** 介面繼承自 [**INapComponentConfig2**](inapcomponentconfig2.md)。</span><span class="sxs-lookup"><span data-stu-id="3670d-110">The **INapComponentConfig3** interface inherits from [**INapComponentConfig2**](inapcomponentconfig2.md).</span></span> <span data-ttu-id="3670d-111">**INapComponentConfig3** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3670d-111">**INapComponentConfig3** also has these types of members:</span></span>

-   [<span data-ttu-id="3670d-112">方法</span><span class="sxs-lookup"><span data-stu-id="3670d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3670d-113">方法</span><span class="sxs-lookup"><span data-stu-id="3670d-113">Methods</span></span>

<span data-ttu-id="3670d-114">**INapComponentConfig3** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3670d-114">The **INapComponentConfig3** interface has these methods.</span></span>



| <span data-ttu-id="3670d-115">方法</span><span class="sxs-lookup"><span data-stu-id="3670d-115">Method</span></span>                                                                                | <span data-ttu-id="3670d-116">描述</span><span class="sxs-lookup"><span data-stu-id="3670d-116">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3670d-117">**INapComponentConfig3：:D eleteAllConfig**</span><span class="sxs-lookup"><span data-stu-id="3670d-117">**INapComponentConfig3::DeleteAllConfig**</span></span>](inapcomponentconfig3-deleteallconfig.md) | <span data-ttu-id="3670d-118">由 Shv 所執行，以提供在安裝之後將 SHV 存放區重設為其原始狀態的方法。</span><span class="sxs-lookup"><span data-stu-id="3670d-118">Implemented by SHVs to provide a way to reset the SHV store to its original state after setup.</span></span><br/>      |
| [<span data-ttu-id="3670d-119">**INapComponentConfig3：:D eleteConfig**</span><span class="sxs-lookup"><span data-stu-id="3670d-119">**INapComponentConfig3::DeleteConfig**</span></span>](inapcomponentconfig3-deleteconfig.md)       | <span data-ttu-id="3670d-120">由 Shv 所執行，以提供一種方法來刪除特定設定識別碼的設定資料。</span><span class="sxs-lookup"><span data-stu-id="3670d-120">Implemented by SHVs to provide a way to delete configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="3670d-121">**INapComponentConfig3::GetConfigFromID**</span><span class="sxs-lookup"><span data-stu-id="3670d-121">**INapComponentConfig3::GetConfigFromID**</span></span>](inapcomponentconfig3-getconfigfromid.md) | <span data-ttu-id="3670d-122">由 Shv 所執行，以提供一種方式來取得特定設定識別碼的設定資料。</span><span class="sxs-lookup"><span data-stu-id="3670d-122">Implemented by SHVs to provide a way to obtain configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="3670d-123">**INapComponentConfig3：： >newconfig.json**</span><span class="sxs-lookup"><span data-stu-id="3670d-123">**INapComponentConfig3::NewConfig**</span></span>](inapcomponentconfig3-newconfig.md)             | <span data-ttu-id="3670d-124">由 Shv 所執行，以提供一種方式來建立特定設定識別碼的設定資料。</span><span class="sxs-lookup"><span data-stu-id="3670d-124">Implemented by SHVs to provide a way to create configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="3670d-125">**INapComponentConfig3::SetConfigToID**</span><span class="sxs-lookup"><span data-stu-id="3670d-125">**INapComponentConfig3::SetConfigToID**</span></span>](inapcomponentconfig3-setconfigtoid.md)     | <span data-ttu-id="3670d-126">由 Shv 所執行，以提供一種方式來設定特定設定識別碼的設定資料。</span><span class="sxs-lookup"><span data-stu-id="3670d-126">Implemented by SHVs to provide a way to set the configuration data for a specific configuration ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3670d-127">備註</span><span class="sxs-lookup"><span data-stu-id="3670d-127">Remarks</span></span>

<span data-ttu-id="3670d-128">系統健康情況代理程式 (Sha) 或隔離強制用戶端 (Qec) 不應執行此介面。</span><span class="sxs-lookup"><span data-stu-id="3670d-128">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="3670d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="3670d-129">Requirements</span></span>



| <span data-ttu-id="3670d-130">需求</span><span class="sxs-lookup"><span data-stu-id="3670d-130">Requirement</span></span> | <span data-ttu-id="3670d-131">值</span><span class="sxs-lookup"><span data-stu-id="3670d-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3670d-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3670d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3670d-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="3670d-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3670d-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3670d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3670d-135">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3670d-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3670d-136">標頭</span><span class="sxs-lookup"><span data-stu-id="3670d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3670d-137"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="3670d-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="3670d-138">Idl</span><span class="sxs-lookup"><span data-stu-id="3670d-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3670d-139"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3670d-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3670d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3670d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3670d-141">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="3670d-141">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> <dt>

[<span data-ttu-id="3670d-142">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="3670d-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3670d-143">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="3670d-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





