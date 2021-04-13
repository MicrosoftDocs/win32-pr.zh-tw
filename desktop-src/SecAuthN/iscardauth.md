---
description: ISCardAuth 介面定義是以標準的形式提供，可在開發智慧卡服務提供者時遵循。ISCardAuth 介面可以用來公開智慧卡所支援的驗證服務。
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: ISCardAuth 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468948"
---
# <a name="iscardauth-interface"></a><span data-ttu-id="cd632-103">ISCardAuth 介面</span><span class="sxs-lookup"><span data-stu-id="cd632-103">ISCardAuth interface</span></span>

<span data-ttu-id="cd632-104">\[**ISCardAuth** 介面可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="cd632-104">\[The **ISCardAuth** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cd632-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="cd632-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cd632-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="cd632-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cd632-107">**ISCardAuth** 介面定義是以標準的形式提供，可在開發 [*智慧卡*](../secgloss/s-gly.md)[*服務提供者*](../secgloss/c-gly.md)時遵循。</span><span class="sxs-lookup"><span data-stu-id="cd632-107">The **ISCardAuth** interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="cd632-108">**ISCardAuth** 介面可以用來公開智慧卡所支援的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="cd632-108">The **ISCardAuth** interface can be used to expose authentication services supported by a smart card.</span></span> <span data-ttu-id="cd632-109">這些服務包括應用程式驗證、智慧卡驗證和使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="cd632-109">These services include application authentication, smart card authentication, and user authentication.</span></span>

<span data-ttu-id="cd632-110">下列範例顯示 **ISCardAuth** 介面的一般用法。</span><span class="sxs-lookup"><span data-stu-id="cd632-110">The following example shows a typical use of the **ISCardAuth** interface.</span></span>

<span data-ttu-id="cd632-111">**使用 ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="cd632-111">**To use ISCardAuth**</span></span>

1.  <span data-ttu-id="cd632-112">透過對應的 [**ISCardManage**](iscardmanage.md)介面方法) 來建立 **ISCardAuth** 介面 (。</span><span class="sxs-lookup"><span data-stu-id="cd632-112">Create an **ISCardAuth** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="cd632-113"> ([**應用程式 \_ 驗證**](iscardauth-app-auth.md)、 [**GetChallenge**](iscardauth-getchallenge.md)、 [**ICC \_ 驗證**](iscardauth-icc-auth.md)或 [**使用者 \_ 驗證**](iscardauth-user-auth.md)) ，呼叫適當的 **ISCardAuth** 方法。</span><span class="sxs-lookup"><span data-stu-id="cd632-113">Call the appropriate **ISCardAuth** method ([**APP\_Auth**](iscardauth-app-auth.md), [**GetChallenge**](iscardauth-getchallenge.md), [**ICC\_Auth**](iscardauth-icc-auth.md), or [**User\_Auth**](iscardauth-user-auth.md)).</span></span>
3.  <span data-ttu-id="cd632-114">釋放 **ISCardAuth** 介面。</span><span class="sxs-lookup"><span data-stu-id="cd632-114">Release the **ISCardAuth** interface.</span></span>

## <a name="members"></a><span data-ttu-id="cd632-115">成員</span><span class="sxs-lookup"><span data-stu-id="cd632-115">Members</span></span>

<span data-ttu-id="cd632-116">**ISCardAuth** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="cd632-116">The **ISCardAuth** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="cd632-117">**ISCardAuth** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cd632-117">**ISCardAuth** also has these types of members:</span></span>

-   [<span data-ttu-id="cd632-118">方法</span><span class="sxs-lookup"><span data-stu-id="cd632-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cd632-119">方法</span><span class="sxs-lookup"><span data-stu-id="cd632-119">Methods</span></span>

<span data-ttu-id="cd632-120">**ISCardAuth** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="cd632-120">The **ISCardAuth** interface has these methods.</span></span>



| <span data-ttu-id="cd632-121">方法</span><span class="sxs-lookup"><span data-stu-id="cd632-121">Method</span></span>                                          | <span data-ttu-id="cd632-122">描述</span><span class="sxs-lookup"><span data-stu-id="cd632-122">Description</span></span>                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd632-123">**應用程式 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="cd632-123">**APP\_Auth**</span></span>](iscardauth-app-auth.md)        | <span data-ttu-id="cd632-124">允許應用程式使用挑戰/簽章通訊協定本身進行驗證。</span><span class="sxs-lookup"><span data-stu-id="cd632-124">Allows the application to authenticate itself using a challenge/signature protocol.</span></span><br/> |
| [<span data-ttu-id="cd632-125">**GetChallenge**</span><span class="sxs-lookup"><span data-stu-id="cd632-125">**GetChallenge**</span></span>](iscardauth-getchallenge.md) | <span data-ttu-id="cd632-126">從智慧卡傳回挑戰。</span><span class="sxs-lookup"><span data-stu-id="cd632-126">Returns a challenge from the smart card.</span></span><br/>                                            |
| [<span data-ttu-id="cd632-127">**ICC \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="cd632-127">**ICC\_Auth**</span></span>](iscardauth-icc-auth.md)        | <span data-ttu-id="cd632-128">允許應用程式驗證智慧卡。</span><span class="sxs-lookup"><span data-stu-id="cd632-128">Allows an application to authenticate the smart card.</span></span><br/>                               |
| [<span data-ttu-id="cd632-129">**使用者 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="cd632-129">**User\_Auth**</span></span>](iscardauth-user-auth.md)      | <span data-ttu-id="cd632-130">允許存取使用者驗證服務。</span><span class="sxs-lookup"><span data-stu-id="cd632-130">Allows access to user authentication services.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="cd632-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd632-131">Requirements</span></span>



| <span data-ttu-id="cd632-132">需求</span><span class="sxs-lookup"><span data-stu-id="cd632-132">Requirement</span></span> | <span data-ttu-id="cd632-133">值</span><span class="sxs-lookup"><span data-stu-id="cd632-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd632-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd632-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cd632-135">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd632-135">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="cd632-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd632-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cd632-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd632-137">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cd632-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cd632-138">End of client support</span></span><br/>    | <span data-ttu-id="cd632-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd632-139">Windows XP</span></span><br/>                                |
| <span data-ttu-id="cd632-140">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="cd632-140">End of server support</span></span><br/>    | <span data-ttu-id="cd632-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd632-141">Windows Server 2003</span></span><br/>                       |



 

 
