---
description: 如果封裝目前正在執行，則暫停該封裝的進程。
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: IPackageDebugSettings：：暫止方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690424"
---
# <a name="ipackagedebugsettingssuspend-method"></a><span data-ttu-id="68a03-103">IPackageDebugSettings：：暫止方法</span><span class="sxs-lookup"><span data-stu-id="68a03-103">IPackageDebugSettings::Suspend method</span></span>

<span data-ttu-id="68a03-104">如果封裝目前正在執行，則暫停該封裝的進程。</span><span class="sxs-lookup"><span data-stu-id="68a03-104">Suspends the processes of the package if they are currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a03-105">語法</span><span class="sxs-lookup"><span data-stu-id="68a03-105">Syntax</span></span>


```C++
HRESULT Suspend(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="68a03-106">參數</span><span class="sxs-lookup"><span data-stu-id="68a03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68a03-107">*packageFullName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68a03-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68a03-108">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="68a03-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="68a03-109">封裝的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="68a03-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68a03-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="68a03-110">Return value</span></span>

<span data-ttu-id="68a03-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="68a03-111">Type: **HRESULT**</span></span>

<span data-ttu-id="68a03-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="68a03-112">This method can return one of these values.</span></span>



| <span data-ttu-id="68a03-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="68a03-113">Return code</span></span>                                                                                            | <span data-ttu-id="68a03-114">Description</span><span class="sxs-lookup"><span data-stu-id="68a03-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="68a03-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="68a03-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="68a03-116">作業成功。</span><span class="sxs-lookup"><span data-stu-id="68a03-116">The operation succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="68a03-117"><dt>**E 不 \_ 合法的 \_ STATECHANGE**</dt></span><span class="sxs-lookup"><span data-stu-id="68a03-117"><dt>**E\_ILLEGAL\_STATECHANGE**</dt></span></span> </dl> | <span data-ttu-id="68a03-118">進程目前未執行。</span><span class="sxs-lookup"><span data-stu-id="68a03-118">The process is not currently running.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="68a03-119">備註</span><span class="sxs-lookup"><span data-stu-id="68a03-119">Remarks</span></span>

<span data-ttu-id="68a03-120">每個進程都會收到 [**暫停**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) 事件。</span><span class="sxs-lookup"><span data-stu-id="68a03-120">Each process receives the [**Suspending**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="68a03-121">這對開發人員而言非常有用，可逐步瞭解其應用程式如何回應此事件。</span><span class="sxs-lookup"><span data-stu-id="68a03-121">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="68a03-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="68a03-122">Requirements</span></span>



| <span data-ttu-id="68a03-123">需求</span><span class="sxs-lookup"><span data-stu-id="68a03-123">Requirement</span></span> | <span data-ttu-id="68a03-124">值</span><span class="sxs-lookup"><span data-stu-id="68a03-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68a03-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68a03-125">Minimum supported client</span></span><br/> | <span data-ttu-id="68a03-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="68a03-126">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="68a03-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68a03-127">Minimum supported server</span></span><br/> | <span data-ttu-id="68a03-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68a03-128">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="68a03-129">Idl</span><span class="sxs-lookup"><span data-stu-id="68a03-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68a03-130"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="68a03-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68a03-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68a03-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="68a03-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="68a03-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
