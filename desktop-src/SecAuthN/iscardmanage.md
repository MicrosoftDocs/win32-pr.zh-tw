---
description: 用來連接到特定的智慧卡或讀取器，以建立其他選用的介面來執行特定的智慧卡功能、鎖定特定的智慧卡以進行獨佔使用，以及取得智慧卡或讀取器的狀態。
ms.assetid: 67077034-5bd0-4176-9dc7-774caba3d427
title: ISCardManage 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage
api_type:
- COM
api_location: ''
ms.openlocfilehash: cce31ea21701c098b09a0bd96360afb374a9bccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194503"
---
# <a name="iscardmanage-interface"></a><span data-ttu-id="4d44f-103">ISCardManage 介面</span><span class="sxs-lookup"><span data-stu-id="4d44f-103">ISCardManage interface</span></span>

<span data-ttu-id="4d44f-104">\[**ISCardManage** 介面不再適用于 windows server 2008、windows Vista 及 windows Server 2003 Service Pack 1 (SP1) 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="4d44f-104">\[The **ISCardManage** interface no longer available for use as of Windows Server 2008, Windows Vista, and Windows Server 2003 with Service Pack 1 (SP1) and later.</span></span> <span data-ttu-id="4d44f-105">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="4d44f-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4d44f-106">下列介面定義是以標準的形式提供，可在開發 [*智慧卡*](../secgloss/s-gly.md)[*服務提供者*](../secgloss/c-gly.md)時遵循。</span><span class="sxs-lookup"><span data-stu-id="4d44f-106">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="4d44f-107">必須提供 **ISCardManage** 介面。</span><span class="sxs-lookup"><span data-stu-id="4d44f-107">The **ISCardManage** interface must be provided.</span></span> <span data-ttu-id="4d44f-108">它是用來連接到特定的 [*智慧卡*](../secgloss/s-gly.md) 或 [*讀取器*](../secgloss/r-gly.md)，以建立其他選用的介面來執行特定的智慧卡功能、鎖定特定的智慧卡以進行獨佔使用，以及取得智慧卡或讀者的狀態。</span><span class="sxs-lookup"><span data-stu-id="4d44f-108">It is used for attaching to a specific [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md), for creating other optional interfaces to perform specific smart card functions, for locking a specific smart card for exclusive use, and for getting the status of a smart card or reader.</span></span> <span data-ttu-id="4d44f-109">作為一組，這些服務可以負責維護妥善定義的內容，讓應用程式可以與 [*智慧卡*](../secgloss/s-gly.md) 或 [*讀者*](../secgloss/r-gly.md)進行通訊。</span><span class="sxs-lookup"><span data-stu-id="4d44f-109">As a set, these services can be responsible for maintaining a well-defined context within which an application can communicate with a [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md).</span></span>

<span data-ttu-id="4d44f-110">以下是 **ISCardManage** 介面的一般用法。</span><span class="sxs-lookup"><span data-stu-id="4d44f-110">Following is a typical use of **ISCardManage** interface.</span></span>

<span data-ttu-id="4d44f-111">**連接到智慧卡**</span><span class="sxs-lookup"><span data-stu-id="4d44f-111">**To connect to a smart card**</span></span>

1.  <span data-ttu-id="4d44f-112">建立與卡片相關聯的 **ISCardManage** 介面。</span><span class="sxs-lookup"><span data-stu-id="4d44f-112">Create the **ISCardManage** interface associated with the card.</span></span>
2.  <span data-ttu-id="4d44f-113">連接到特定智慧卡讀卡機 ([**AttachByIFD**](iscardmanage-attachbyifd.md)) 或使用先前取得的控制碼 ([**AttachByHandle**](iscardmanage-attachbyhandle.md)) ，以連接到智慧卡。</span><span class="sxs-lookup"><span data-stu-id="4d44f-113">Connect to a smart card by attaching to a specific smart card reader ([**AttachByIFD**](iscardmanage-attachbyifd.md)) or by using a previously acquired handle ([**AttachByHandle**](iscardmanage-attachbyhandle.md)).</span></span>
3.  <span data-ttu-id="4d44f-114">建立其他介面來執行智慧卡作業 ([**CreateCardAuth**](iscardmanage-createcardauth.md)、 [**CreateFileAccess**](iscardmanage-createfileaccess.md)、 [**CreateCHVerification**](iscardmanage-createchverification.md)或 [**CreateInterface**](iscardmanage-createinterface.md)) 。</span><span class="sxs-lookup"><span data-stu-id="4d44f-114">Create other interfaces to perform smart card operations ([**CreateCardAuth**](iscardmanage-createcardauth.md), [**CreateFileAccess**](iscardmanage-createfileaccess.md), [**CreateCHVerification**](iscardmanage-createchverification.md), or [**CreateInterface**](iscardmanage-createinterface.md)).</span></span>
4.  <span data-ttu-id="4d44f-115">釋放卡片 (卸 [**離**](iscardmanage-detach.md)) 。</span><span class="sxs-lookup"><span data-stu-id="4d44f-115">Release the card ([**Detach**](iscardmanage-detach.md)).</span></span>
5.  <span data-ttu-id="4d44f-116">視需要釋放 **ISCardManage** 介面和其他專案。</span><span class="sxs-lookup"><span data-stu-id="4d44f-116">Release the **ISCardManage** interface and others as required.</span></span>

## <a name="members"></a><span data-ttu-id="4d44f-117">成員</span><span class="sxs-lookup"><span data-stu-id="4d44f-117">Members</span></span>

<span data-ttu-id="4d44f-118">**ISCardManage** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="4d44f-118">The **ISCardManage** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4d44f-119">**ISCardManage** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4d44f-119">**ISCardManage** also has these types of members:</span></span>

-   [<span data-ttu-id="4d44f-120">方法</span><span class="sxs-lookup"><span data-stu-id="4d44f-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4d44f-121">方法</span><span class="sxs-lookup"><span data-stu-id="4d44f-121">Methods</span></span>

<span data-ttu-id="4d44f-122">**ISCardManage** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4d44f-122">The **ISCardManage** interface has these methods.</span></span>



| <span data-ttu-id="4d44f-123">方法</span><span class="sxs-lookup"><span data-stu-id="4d44f-123">Method</span></span>                                                            | <span data-ttu-id="4d44f-124">描述</span><span class="sxs-lookup"><span data-stu-id="4d44f-124">Description</span></span>                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d44f-125">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="4d44f-125">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)             | <span data-ttu-id="4d44f-126">允許應用程式使用智慧卡 [*資源管理員*](../secgloss/r-gly.md)所傳回的控制碼，建立智慧卡的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="4d44f-126">Allows an application to create a communication link to a smart card using a handle returned by the smart card [*resource manager*](../secgloss/r-gly.md).</span></span><br/>                                              |
| [<span data-ttu-id="4d44f-127">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="4d44f-127">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)                   | <span data-ttu-id="4d44f-128">允許應用程式要求建立以顯示名稱參考之特定讀取器的內容。</span><span class="sxs-lookup"><span data-stu-id="4d44f-128">Allows an application to request establishment of a context for a specific reader referenced with a display name.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="4d44f-129">**CreateCardAuth**</span><span class="sxs-lookup"><span data-stu-id="4d44f-129">**CreateCardAuth**</span></span>](iscardmanage-createcardauth.md)             | <span data-ttu-id="4d44f-130">允許建立 [**ISCardAuth**](iscardauth.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="4d44f-130">Allows the creation of a [**ISCardAuth**](iscardauth.md) interface.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="4d44f-131">**CreateCHVerification**</span><span class="sxs-lookup"><span data-stu-id="4d44f-131">**CreateCHVerification**</span></span>](iscardmanage-createchverification.md) | <span data-ttu-id="4d44f-132">允許建立 [**ISCardVerify**](iscardverify.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="4d44f-132">Allows the creation of a [**ISCardVerify**](iscardverify.md) interface.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="4d44f-133">**CreateFileAccess**</span><span class="sxs-lookup"><span data-stu-id="4d44f-133">**CreateFileAccess**</span></span>](iscardmanage-createfileaccess.md)         | <span data-ttu-id="4d44f-134">允許建立 [**ISCardFileAccess**](iscardfileaccess.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="4d44f-134">Allows the creation of a [**ISCardFileAccess**](iscardfileaccess.md) interface.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="4d44f-135">**CreateInterface**</span><span class="sxs-lookup"><span data-stu-id="4d44f-135">**CreateInterface**</span></span>](iscardmanage-createinterface.md)           | <span data-ttu-id="4d44f-136">允許建立介面。</span><span class="sxs-lookup"><span data-stu-id="4d44f-136">Allows the creation of an interface.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="4d44f-137">**中斷連結**</span><span class="sxs-lookup"><span data-stu-id="4d44f-137">**Detach**</span></span>](iscardmanage-detach.md)                             | <span data-ttu-id="4d44f-138">分別釋放 [**AttachByHandle**](iscardmanage-attachbyhandle.md) 或 [**AttachByIFD**](iscardmanage-attachbyifd.md) 所配置的特定智慧卡或讀取器的附件。</span><span class="sxs-lookup"><span data-stu-id="4d44f-138">Releases the attachment to a particular smart card or reader allocated by [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md) respectively.</span></span><br/>                                                                |
| [<span data-ttu-id="4d44f-139">**重新連接**</span><span class="sxs-lookup"><span data-stu-id="4d44f-139">**Reconnect**</span></span>](iscardmanage-reconnect.md)                       | <span data-ttu-id="4d44f-140">允許應用程式重新連線到智慧卡或讀取器，而不需要分別發出卸 [**離**](iscardmanage-detach.md) 、 [**AttachByHandle**](iscardmanage-attachbyhandle.md) 或 [**AttachByIFD**](iscardmanage-attachbyifd.md) 。</span><span class="sxs-lookup"><span data-stu-id="4d44f-140">Allows an application to reconnect to a smart card or reader without having to issue a [**Detach**](iscardmanage-detach.md) followed by [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md) respectively.</span></span><br/> |
| [<span data-ttu-id="4d44f-141">**SCardLock**</span><span class="sxs-lookup"><span data-stu-id="4d44f-141">**SCardLock**</span></span>](iscardmanage-scardlock.md)                       | <span data-ttu-id="4d44f-142">鎖定連線的智慧卡或讀取器以供獨佔使用。</span><span class="sxs-lookup"><span data-stu-id="4d44f-142">Locks a connected smart card or reader for exclusive use.</span></span><br/>                                                                                                                                                                                                       |
| [<span data-ttu-id="4d44f-143">**SCardUnlock**</span><span class="sxs-lookup"><span data-stu-id="4d44f-143">**SCardUnlock**</span></span>](iscardmanage-scardunlock.md)                   | <span data-ttu-id="4d44f-144">釋出連線智慧卡或讀取器的專用用途。</span><span class="sxs-lookup"><span data-stu-id="4d44f-144">Releases exclusive use of the connected smart card or reader.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="4d44f-145">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4d44f-145">**Status**</span></span>](iscardmanage-status.md)                             | <span data-ttu-id="4d44f-146">允許應用程式取得智慧卡或讀取器的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4d44f-146">Allows an application to get the current status of the smart card or reader.</span></span><br/>                                                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="4d44f-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d44f-147">Requirements</span></span>



| <span data-ttu-id="4d44f-148">需求</span><span class="sxs-lookup"><span data-stu-id="4d44f-148">Requirement</span></span> | <span data-ttu-id="4d44f-149">值</span><span class="sxs-lookup"><span data-stu-id="4d44f-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4d44f-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d44f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="4d44f-151">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d44f-151">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4d44f-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d44f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="4d44f-153">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d44f-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4d44f-154">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4d44f-154">End of client support</span></span><br/>    | <span data-ttu-id="4d44f-155">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4d44f-155">Windows XP</span></span><br/>                                |
| <span data-ttu-id="4d44f-156">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="4d44f-156">End of server support</span></span><br/>    | <span data-ttu-id="4d44f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4d44f-157">Windows Server 2003</span></span><br/>                       |



 

 
