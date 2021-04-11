---
title: 'INapClientManagement2 介面 (NapManagement .h) '
description: '提供 NAP 用戶端管理的方法。 |INapClientManagement2 介面 (NapManagement .h) '
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- INapClientManagement2 介面 NAP
- INapClientManagement2 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035304"
---
# <a name="inapclientmanagement2-interface"></a><span data-ttu-id="0232c-106">INapClientManagement2 介面</span><span class="sxs-lookup"><span data-stu-id="0232c-106">INapClientManagement2 interface</span></span>

> [!Note]  
> <span data-ttu-id="0232c-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="0232c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0232c-108">**INapClientManagement2** 介面提供 NAP 用戶端管理的方法。</span><span class="sxs-lookup"><span data-stu-id="0232c-108">The **INapClientManagement2** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="0232c-109">此介面會繼承 [**INapClientManagement**](inapclientmanagement.md) 的所有方法，因此應該改用。</span><span class="sxs-lookup"><span data-stu-id="0232c-109">This interface inherits all the methods of [**INapClientManagement**](inapclientmanagement.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="0232c-110">成員</span><span class="sxs-lookup"><span data-stu-id="0232c-110">Members</span></span>

<span data-ttu-id="0232c-111">**INapClientManagement2** 介面繼承自 [**INapClientManagement**](inapclientmanagement.md)。</span><span class="sxs-lookup"><span data-stu-id="0232c-111">The **INapClientManagement2** interface inherits from [**INapClientManagement**](inapclientmanagement.md).</span></span> <span data-ttu-id="0232c-112">**INapClientManagement2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0232c-112">**INapClientManagement2** also has these types of members:</span></span>

-   [<span data-ttu-id="0232c-113">方法</span><span class="sxs-lookup"><span data-stu-id="0232c-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0232c-114">方法</span><span class="sxs-lookup"><span data-stu-id="0232c-114">Methods</span></span>

<span data-ttu-id="0232c-115">**INapClientManagement2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0232c-115">The **INapClientManagement2** interface has these methods.</span></span>



| <span data-ttu-id="0232c-116">方法</span><span class="sxs-lookup"><span data-stu-id="0232c-116">Method</span></span>                                                                                                    | <span data-ttu-id="0232c-117">描述</span><span class="sxs-lookup"><span data-stu-id="0232c-117">Description</span></span>                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0232c-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="0232c-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span></span>](inapclientmanagement2-getsystemisolationinfoex.md) | <span data-ttu-id="0232c-119">抓取 Nap 用戶端的隔離狀態和擴充隔離狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0232c-119">Retrieves information about the isolation state and extended isolation state of the Nap client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0232c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0232c-120">Requirements</span></span>



| <span data-ttu-id="0232c-121">需求</span><span class="sxs-lookup"><span data-stu-id="0232c-121">Requirement</span></span> | <span data-ttu-id="0232c-122">值</span><span class="sxs-lookup"><span data-stu-id="0232c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0232c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0232c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0232c-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0232c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0232c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0232c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0232c-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0232c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0232c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0232c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0232c-128"><dt>NapManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="0232c-128"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="0232c-129">Idl</span><span class="sxs-lookup"><span data-stu-id="0232c-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0232c-130"><dt>NapManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0232c-130"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="0232c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0232c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0232c-132"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0232c-132"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="0232c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0232c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0232c-134">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="0232c-134">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> <dt>

[<span data-ttu-id="0232c-135">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="0232c-135">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0232c-136">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="0232c-136">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





