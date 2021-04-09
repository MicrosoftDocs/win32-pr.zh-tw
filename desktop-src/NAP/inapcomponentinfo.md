---
title: 'INapComponentInfo 介面 (NapCommon .h) '
description: 提供外掛程式元件 (的方法，例如 Sha 和 Shv) 必須執行，NAP 系統才能與其通訊。
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- INapComponentInfo 介面 NAP
- INapComponentInfo 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934168"
---
# <a name="inapcomponentinfo-interface"></a><span data-ttu-id="b16e3-105">INapComponentInfo 介面</span><span class="sxs-lookup"><span data-stu-id="b16e3-105">INapComponentInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="b16e3-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="b16e3-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b16e3-107">**INapComponentInfo** 介面提供外掛程式元件 (的方法，例如 Sha 和 shv，) 必須為 NAP 系統執行才能與它們進行通訊。</span><span class="sxs-lookup"><span data-stu-id="b16e3-107">The **INapComponentInfo** interface provides methods that plug-in components (such as SHAs and SHVs) must implement for the NAP system to communicate with them.</span></span> <span data-ttu-id="b16e3-108">NAP 系統會呼叫這些方法的執行，以抓取靜態的系統管理資訊 (例如，易記名稱或當地語系化的字串) 。</span><span class="sxs-lookup"><span data-stu-id="b16e3-108">The NAP system calls your implementation of these methods to retrieve static administrative information (for example, friendly name or localized strings).</span></span>

## <a name="members"></a><span data-ttu-id="b16e3-109">成員</span><span class="sxs-lookup"><span data-stu-id="b16e3-109">Members</span></span>

<span data-ttu-id="b16e3-110">**INapComponentInfo** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="b16e3-110">The **INapComponentInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b16e3-111">**INapComponentInfo** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b16e3-111">**INapComponentInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="b16e3-112">方法</span><span class="sxs-lookup"><span data-stu-id="b16e3-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b16e3-113">方法</span><span class="sxs-lookup"><span data-stu-id="b16e3-113">Methods</span></span>

<span data-ttu-id="b16e3-114">**INapComponentInfo** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b16e3-114">The **INapComponentInfo** interface has these methods.</span></span>



| <span data-ttu-id="b16e3-115">方法</span><span class="sxs-lookup"><span data-stu-id="b16e3-115">Method</span></span>                                                                                                         | <span data-ttu-id="b16e3-116">描述</span><span class="sxs-lookup"><span data-stu-id="b16e3-116">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b16e3-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span><span class="sxs-lookup"><span data-stu-id="b16e3-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span></span>](inapcomponentinfo-converterrorcodetomessageid-method.md) | <span data-ttu-id="b16e3-118">NAP 系統用來要求健康情況用戶端將 HRESULT 錯誤碼轉換成訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="b16e3-118">Used by the NAP System to request the health client convert an HRESULT error code to a message ID.</span></span><br/> |
| [<span data-ttu-id="b16e3-119">**INapComponentInfo：： GetDescription**</span><span class="sxs-lookup"><span data-stu-id="b16e3-119">**INapComponentInfo::GetDescription**</span></span>](inapcomponentinfo-getdescription-method.md)                           | <span data-ttu-id="b16e3-120">NAP 系統用來取得健全狀況用戶端的描述。</span><span class="sxs-lookup"><span data-stu-id="b16e3-120">Used by the NAP System to get the description of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="b16e3-121">**INapComponentInfo::GetFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="b16e3-121">**INapComponentInfo::GetFriendlyName**</span></span>](inapcomponentinfo-getfriendlyname-method.md)                         | <span data-ttu-id="b16e3-122">NAP 系統用來取得健全狀況用戶端的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="b16e3-122">Used by the NAP System to get the friendly name of a health client.</span></span><br/>                                |
| [<span data-ttu-id="b16e3-123">**INapComponentInfo::GetIcon**</span><span class="sxs-lookup"><span data-stu-id="b16e3-123">**INapComponentInfo::GetIcon**</span></span>](inapcomponentinfo-geticon-method.md)                                         | <span data-ttu-id="b16e3-124">NAP 系統用來取得健全狀況用戶端的圖示。</span><span class="sxs-lookup"><span data-stu-id="b16e3-124">Used by the NAP System to get the icon of a health client.</span></span><br/>                                         |
| [<span data-ttu-id="b16e3-125">**INapComponentInfo::GetLocalizedString**</span><span class="sxs-lookup"><span data-stu-id="b16e3-125">**INapComponentInfo::GetLocalizedString**</span></span>](inapcomponentinfo-getlocalizedstring-method.md)                   | <span data-ttu-id="b16e3-126">NAP 系統用來取得當地語系化的字串。</span><span class="sxs-lookup"><span data-stu-id="b16e3-126">Used by the NAP System to get localized strings.</span></span><br/>                                                   |
| [<span data-ttu-id="b16e3-127">**INapComponentInfo::GetVendorName**</span><span class="sxs-lookup"><span data-stu-id="b16e3-127">**INapComponentInfo::GetVendorName**</span></span>](inapcomponentinfo-getvendorname-method.md)                             | <span data-ttu-id="b16e3-128">NAP 系統用來取得健康情況用戶端的廠商名稱。</span><span class="sxs-lookup"><span data-stu-id="b16e3-128">Used by the NAP System to get the vendor name of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="b16e3-129">**INapComponentInfo：： GetVersion**</span><span class="sxs-lookup"><span data-stu-id="b16e3-129">**INapComponentInfo::GetVersion**</span></span>](inapcomponentinfo-getversion-method.md)                                   | <span data-ttu-id="b16e3-130">NAP 系統用來取得健全狀況用戶端的版本。</span><span class="sxs-lookup"><span data-stu-id="b16e3-130">Used by the NAP System to get the version of a health client.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="b16e3-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b16e3-131">Requirements</span></span>



| <span data-ttu-id="b16e3-132">需求</span><span class="sxs-lookup"><span data-stu-id="b16e3-132">Requirement</span></span> | <span data-ttu-id="b16e3-133">值</span><span class="sxs-lookup"><span data-stu-id="b16e3-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b16e3-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b16e3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b16e3-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b16e3-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b16e3-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b16e3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b16e3-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b16e3-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b16e3-138">標頭</span><span class="sxs-lookup"><span data-stu-id="b16e3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b16e3-139"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="b16e3-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="b16e3-140">Idl</span><span class="sxs-lookup"><span data-stu-id="b16e3-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b16e3-141"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b16e3-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b16e3-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b16e3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b16e3-143">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="b16e3-143">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b16e3-144">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="b16e3-144">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

