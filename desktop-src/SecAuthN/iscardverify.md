---
description: 提供用來設定 CHV (卡持有者驗證) 碼以及驗證使用者的服務。
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: ISCardVerify 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693319"
---
# <a name="iscardverify-interface"></a><span data-ttu-id="9eac8-103">ISCardVerify 介面</span><span class="sxs-lookup"><span data-stu-id="9eac8-103">ISCardVerify interface</span></span>

<span data-ttu-id="9eac8-104">\[**ISCardVerify** 介面可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="9eac8-104">\[The **ISCardVerify** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9eac8-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="9eac8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9eac8-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="9eac8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9eac8-107">下列介面定義是以標準的形式提供，可在開發 [*智慧卡*](../secgloss/s-gly.md)[*服務提供者*](../secgloss/c-gly.md)時遵循。</span><span class="sxs-lookup"><span data-stu-id="9eac8-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="9eac8-108">**ISCardVerify** 介面提供了用來設定 CHV (卡持有者驗證) 碼以及驗證使用者的服務。</span><span class="sxs-lookup"><span data-stu-id="9eac8-108">The **ISCardVerify** interface provides services for setting CHV (card holder verification) code and for verifying the user.</span></span>

<span data-ttu-id="9eac8-109">**ISCardVerify** 類別是針對執行應用程式專屬 CHV 原則的應用程式所定義，且具有智慧卡內部執行的詳細知識。</span><span class="sxs-lookup"><span data-stu-id="9eac8-109">The **ISCardVerify** class is defined for applications that implement application-specific CHV policy, and that have a detailed knowledge of the smart card's internal implementation.</span></span>

<span data-ttu-id="9eac8-110">以下是 **ISCardVerify** 介面的一般用法。</span><span class="sxs-lookup"><span data-stu-id="9eac8-110">Following is a typical use of the **ISCardVerify** interface.</span></span>

<span data-ttu-id="9eac8-111">下列程式會使用 **ISCardVerify** 來變更 CHV 程式碼。</span><span class="sxs-lookup"><span data-stu-id="9eac8-111">The following procedure uses **ISCardVerify** to change the CHV code.</span></span>

<span data-ttu-id="9eac8-112">**變更智慧卡的 CHV 碼**</span><span class="sxs-lookup"><span data-stu-id="9eac8-112">**To change the CHV code of a smart card**</span></span>

1.  <span data-ttu-id="9eac8-113">透過對應的 [**ISCardManage**](iscardmanage.md)介面方法) 來建立 **ISCardVerify** 介面 (。</span><span class="sxs-lookup"><span data-stu-id="9eac8-113">Create an **ISCardVerify** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="9eac8-114">呼叫 [**ChangeCode**](iscardverify-changecode.md) 方法，並提供新的程式碼，並指定其為本機或全域，以及啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="9eac8-114">Call the [**ChangeCode**](iscardverify-changecode.md) method and provide new code, specifying if it is local or global and if it is enabled or disabled.</span></span>
3.  <span data-ttu-id="9eac8-115">釋放 **ISCardVerify** 介面。</span><span class="sxs-lookup"><span data-stu-id="9eac8-115">Release the **ISCardVerify** interface.</span></span>

## <a name="members"></a><span data-ttu-id="9eac8-116">成員</span><span class="sxs-lookup"><span data-stu-id="9eac8-116">Members</span></span>

<span data-ttu-id="9eac8-117">**ISCardVerify** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="9eac8-117">The **ISCardVerify** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9eac8-118">**ISCardVerify** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9eac8-118">**ISCardVerify** also has these types of members:</span></span>

-   [<span data-ttu-id="9eac8-119">方法</span><span class="sxs-lookup"><span data-stu-id="9eac8-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9eac8-120">方法</span><span class="sxs-lookup"><span data-stu-id="9eac8-120">Methods</span></span>

<span data-ttu-id="9eac8-121">**ISCardVerify** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9eac8-121">The **ISCardVerify** interface has these methods.</span></span>



| <span data-ttu-id="9eac8-122">方法</span><span class="sxs-lookup"><span data-stu-id="9eac8-122">Method</span></span>                                                        | <span data-ttu-id="9eac8-123">描述</span><span class="sxs-lookup"><span data-stu-id="9eac8-123">Description</span></span>                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eac8-124">**ChangeCode**</span><span class="sxs-lookup"><span data-stu-id="9eac8-124">**ChangeCode**</span></span>](iscardverify-changecode.md)                 | <span data-ttu-id="9eac8-125">變更目前的 CHV 碼。</span><span class="sxs-lookup"><span data-stu-id="9eac8-125">Changes the current CHV code.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="9eac8-126">**ResetSecurityState**</span><span class="sxs-lookup"><span data-stu-id="9eac8-126">**ResetSecurityState**</span></span>](iscardverify-resetsecuritystate.md) | <span data-ttu-id="9eac8-127">重設智慧卡的 [*安全性內容*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="9eac8-127">Resets the [*security context*](../secgloss/s-gly.md) of the smart card.</span></span><br/> |
| <span data-ttu-id="9eac8-128">[**疏通**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9eac8-128">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>                       | <span data-ttu-id="9eac8-129">重新啟用 [*安全性內容*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="9eac8-129">Re-enables the [*security context*](../secgloss/s-gly.md).</span></span><br/>               |
| [<span data-ttu-id="9eac8-130">**驗證**</span><span class="sxs-lookup"><span data-stu-id="9eac8-130">**Verify**</span></span>](iscardverify-verify.md)                         | <span data-ttu-id="9eac8-131">驗證使用者。</span><span class="sxs-lookup"><span data-stu-id="9eac8-131">Authenticates the user.</span></span><br/>                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="9eac8-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="9eac8-132">Requirements</span></span>



| <span data-ttu-id="9eac8-133">需求</span><span class="sxs-lookup"><span data-stu-id="9eac8-133">Requirement</span></span> | <span data-ttu-id="9eac8-134">值</span><span class="sxs-lookup"><span data-stu-id="9eac8-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9eac8-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9eac8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9eac8-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9eac8-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9eac8-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9eac8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9eac8-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9eac8-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9eac8-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9eac8-139">End of client support</span></span><br/>    | <span data-ttu-id="9eac8-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9eac8-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="9eac8-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9eac8-141">End of server support</span></span><br/>    | <span data-ttu-id="9eac8-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9eac8-142">Windows Server 2003</span></span><br/>                       |



 

 
