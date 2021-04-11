---
description: 檢查是否已載入線上使用者設定檔。
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: 'OnProfileLoaded 函式 (Lsaidprov) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692931"
---
# <a name="onprofileloaded-function"></a><span data-ttu-id="f8c54-103">OnProfileLoaded 函式</span><span class="sxs-lookup"><span data-stu-id="f8c54-103">OnProfileLoaded function</span></span>

<span data-ttu-id="f8c54-104">檢查是否已載入線上使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="f8c54-104">Checks that the online user profile is loaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c54-105">語法</span><span class="sxs-lookup"><span data-stu-id="f8c54-105">Syntax</span></span>


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a><span data-ttu-id="f8c54-106">參數</span><span class="sxs-lookup"><span data-stu-id="f8c54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8c54-107">*ProviderHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8c54-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c54-108">提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="f8c54-108">The provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="f8c54-109">*UserToken* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8c54-109">*UserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c54-110">正在載入或卸載其設定檔的使用者 Token。</span><span class="sxs-lookup"><span data-stu-id="f8c54-110">Token of the user whose profile is being loaded or unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="f8c54-111">已 *載入* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8c54-111">*Loaded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c54-112">如果已載入設定檔，**則為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f8c54-112">**TRUE** if the profile has been loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8c54-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8c54-113">Return value</span></span>

<span data-ttu-id="f8c54-114">如果函式成功，函數會傳回狀態 \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="f8c54-114">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="f8c54-115">如果函式失敗，函式會傳回非零的錯誤碼，此錯誤碼為診斷目的提供者特有的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f8c54-115">If the function fails, the function returns a nonzero error code that is a provider-specific error for diagnostic purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8c54-116">備註</span><span class="sxs-lookup"><span data-stu-id="f8c54-116">Remarks</span></span>

<span data-ttu-id="f8c54-117">每次呼叫 [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) 函數時，就會呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="f8c54-117">This function is called each time the [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) function is called.</span></span> <span data-ttu-id="f8c54-118">它不會與 **LoadUserProfile** 同步;也就是說， **LoadUserProfile** 可能已傳回，而且設定檔可能會在呼叫函式時卸載。</span><span class="sxs-lookup"><span data-stu-id="f8c54-118">It is not synchronized with **LoadUserProfile**; that is, **LoadUserProfile** might have returned and the profile might have been unloaded by the time the function was called.</span></span> <span data-ttu-id="f8c54-119">即使已載入設定檔，也可以多次呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="f8c54-119">This function can be called more than once even when the profile has been loaded.</span></span> <span data-ttu-id="f8c54-120">身分識別提供者不能假設 *載入* 等於 TRUE 的這個函式的呼叫，後面會接著 *載入* 等於 FALSE 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f8c54-120">The identity provider must not assume that a call to this function with *Loaded* equal to TRUE will be followed by a call with *Loaded* equal to FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c54-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8c54-121">Requirements</span></span>



| <span data-ttu-id="f8c54-122">需求</span><span class="sxs-lookup"><span data-stu-id="f8c54-122">Requirement</span></span> | <span data-ttu-id="f8c54-123">值</span><span class="sxs-lookup"><span data-stu-id="f8c54-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c54-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8c54-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f8c54-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8c54-125">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f8c54-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8c54-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f8c54-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8c54-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f8c54-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f8c54-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8c54-129"><dt>Lsaidprov。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8c54-129"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

 
