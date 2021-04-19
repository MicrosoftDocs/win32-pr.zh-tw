---
description: 如果目前已暫止封裝的進程，則繼續執行。
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: IPackageDebugSettings：： Resume 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971213"
---
# <a name="ipackagedebugsettingsresume-method"></a><span data-ttu-id="3b411-103">IPackageDebugSettings：： Resume 方法</span><span class="sxs-lookup"><span data-stu-id="3b411-103">IPackageDebugSettings::Resume method</span></span>

<span data-ttu-id="3b411-104">如果目前已暫止封裝的進程，則繼續執行。</span><span class="sxs-lookup"><span data-stu-id="3b411-104">Resumes the processes of the package if they are currently suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b411-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b411-105">Syntax</span></span>


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="3b411-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b411-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b411-107">*packageFullName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b411-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b411-108">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3b411-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="3b411-109">封裝的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="3b411-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b411-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b411-110">Return value</span></span>

<span data-ttu-id="3b411-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3b411-111">Type: **HRESULT**</span></span>

<span data-ttu-id="3b411-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3b411-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b411-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b411-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b411-114">備註</span><span class="sxs-lookup"><span data-stu-id="3b411-114">Remarks</span></span>

<span data-ttu-id="3b411-115">每個進程都會收到 [**繼續**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) 的事件。</span><span class="sxs-lookup"><span data-stu-id="3b411-115">Each process receives the [**Resuming**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="3b411-116">這對開發人員而言非常有用，可逐步瞭解其應用程式如何回應此事件。</span><span class="sxs-lookup"><span data-stu-id="3b411-116">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b411-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b411-117">Requirements</span></span>



| <span data-ttu-id="3b411-118">需求</span><span class="sxs-lookup"><span data-stu-id="3b411-118">Requirement</span></span> | <span data-ttu-id="3b411-119">值</span><span class="sxs-lookup"><span data-stu-id="3b411-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b411-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b411-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b411-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3b411-121">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="3b411-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b411-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b411-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3b411-123">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="3b411-124">Idl</span><span class="sxs-lookup"><span data-stu-id="3b411-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b411-125"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b411-125"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b411-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b411-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b411-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b411-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
