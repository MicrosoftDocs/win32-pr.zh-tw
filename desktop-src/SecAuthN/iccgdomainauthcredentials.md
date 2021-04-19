---
description: 用戶端執行的介面，可讓開發人員在執行時間動態提供自己的認證，以使用 Active Directory 來驗證未加入網域的容器。
title: 'ICcgDomainAuthCredentials 介面 (ccgplugins .h) '
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "106988108"
---
# <a name="iccgdomainauthcredentials-interface"></a><span data-ttu-id="0b09d-103">ICcgDomainAuthCredentials 介面</span><span class="sxs-lookup"><span data-stu-id="0b09d-103">ICcgDomainAuthCredentials interface</span></span>

<span data-ttu-id="0b09d-104">用戶端執行的介面，可讓開發人員在執行時間動態提供自己的認證，以使用 Active Directory 來驗證未加入網域的容器。</span><span class="sxs-lookup"><span data-stu-id="0b09d-104">A client-implemented interface that allows developers to supply their own credentials dynamically at run time to authenticate non-domain joined containers with Active Directory.</span></span> 

## <a name="members"></a><span data-ttu-id="0b09d-105">成員</span><span class="sxs-lookup"><span data-stu-id="0b09d-105">Members</span></span>

<span data-ttu-id="0b09d-106">**ICcgDomainAuthCredentials** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="0b09d-106">The **ICcgDomainAuthCredentials** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0b09d-107">**ICcgDomainAuthCredentials** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0b09d-107">**ICcgDomainAuthCredentials** also has these types of members:</span></span>

-   [<span data-ttu-id="0b09d-108">方法</span><span class="sxs-lookup"><span data-stu-id="0b09d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0b09d-109">方法</span><span class="sxs-lookup"><span data-stu-id="0b09d-109">Methods</span></span>

<span data-ttu-id="0b09d-110">**ICcgDomainAuthCredentials** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0b09d-110">The **ICcgDomainAuthCredentials** interface has these methods.</span></span>



| <span data-ttu-id="0b09d-111">方法</span><span class="sxs-lookup"><span data-stu-id="0b09d-111">Method</span></span>                                           | <span data-ttu-id="0b09d-112">描述</span><span class="sxs-lookup"><span data-stu-id="0b09d-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b09d-113">**GetPasswordCredentials**</span><span class="sxs-lookup"><span data-stu-id="0b09d-113">**GetPasswordCredentials**</span></span>](iccgdomainauthcredentials-getpasswordcredentials.md)               | <span data-ttu-id="0b09d-114">傳回認證，以使用 Active Directory 驗證未加入網域的容器。</span><span class="sxs-lookup"><span data-stu-id="0b09d-114">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="0b09d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b09d-115">Requirements</span></span>



| <span data-ttu-id="0b09d-116">需求</span><span class="sxs-lookup"><span data-stu-id="0b09d-116">Requirement</span></span> | <span data-ttu-id="0b09d-117">值</span><span class="sxs-lookup"><span data-stu-id="0b09d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b09d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b09d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0b09d-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b09d-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0b09d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b09d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0b09d-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b09d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0b09d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0b09d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b09d-123"><dt>ccgplugins。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b09d-123"><dt>ccgplugins.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b09d-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0b09d-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b09d-125"><dt>ccgplugins .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0b09d-125"><dt>ccgplugins.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0b09d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0b09d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b09d-127"><dt>ccgplugins.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b09d-127"><dt>ccgplugins.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b09d-128">IID</span><span class="sxs-lookup"><span data-stu-id="0b09d-128">IID</span></span><br/>                      | <span data-ttu-id="0b09d-129">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="0b09d-129">6ecda518-2010-4437-8bc3-46e752b7b172</span></span><br/>          |



 

