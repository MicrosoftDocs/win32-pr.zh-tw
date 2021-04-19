---
description: 此函式會採用原始屬性（如果原始權杖中有提供），並在繼承權杖的複本上設定這些屬性，並傳回重複的標記。
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: srpInheritOriginClaim 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973241"
---
# <a name="srpinheritoriginclaim-function"></a><span data-ttu-id="a8691-103">srpInheritOriginClaim 函式</span><span class="sxs-lookup"><span data-stu-id="a8691-103">srpInheritOriginClaim function</span></span>

<span data-ttu-id="a8691-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a8691-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a8691-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a8691-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a8691-106">此函式會採用原始屬性（如果原始權杖中有提供），並在繼承權杖的複本上設定這些屬性，並傳回重複的標記。</span><span class="sxs-lookup"><span data-stu-id="a8691-106">This function takes the origin attribute if present from the origin token and sets them on a duplicate of the inheriting token, and returns the duplicate token.</span></span> <span data-ttu-id="a8691-107">然後，呼叫端可以模擬傳回的權杖。</span><span class="sxs-lookup"><span data-stu-id="a8691-107">The caller can then impersonate the returned token.</span></span> <span data-ttu-id="a8691-108">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="a8691-108">This function has no associated import library.</span></span> <span data-ttu-id="a8691-109">您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 srpapi.dll。</span><span class="sxs-lookup"><span data-stu-id="a8691-109">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to srpapi.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8691-110">語法</span><span class="sxs-lookup"><span data-stu-id="a8691-110">Syntax</span></span>


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a><span data-ttu-id="a8691-111">參數</span><span class="sxs-lookup"><span data-stu-id="a8691-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8691-112">*OriginToken* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8691-112">*OriginToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8691-113">權杖的控制碼，這個標記會重複，並接收繼承的原始屬性。</span><span class="sxs-lookup"><span data-stu-id="a8691-113">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="a8691-114">這個控制碼必須以權杖 \_ 重複存取權限開啟。</span><span class="sxs-lookup"><span data-stu-id="a8691-114">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span>

</dd> <dt>

<span data-ttu-id="a8691-115">*InheritingToken* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8691-115">*InheritingToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8691-116">權杖的控制碼，這個標記會重複，並接收繼承的原始屬性。</span><span class="sxs-lookup"><span data-stu-id="a8691-116">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="a8691-117">這個控制碼必須以權杖 \_ 重複存取權限開啟。</span><span class="sxs-lookup"><span data-stu-id="a8691-117">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span> 

</dd> <dt>

<span data-ttu-id="a8691-118">*ResultToken*</span><span class="sxs-lookup"><span data-stu-id="a8691-118">*ResultToken*</span></span> 
</dt> <dd>

<span data-ttu-id="a8691-119">成功時，接收重複的標記。</span><span class="sxs-lookup"><span data-stu-id="a8691-119">On success, receives the duplicated token.</span></span> <span data-ttu-id="a8691-120">呼叫端可以模擬它，以使用繼承的原始屬性來執行作業。</span><span class="sxs-lookup"><span data-stu-id="a8691-120">The caller can impersonate it to perform operations with the inherited origin attribute.</span></span> <span data-ttu-id="a8691-121">呼叫端會取得此控制碼的擁有權，而且必須將其關閉。</span><span class="sxs-lookup"><span data-stu-id="a8691-121">The caller takes ownership of this handle and must close it.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8691-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8691-122">Return value</span></span>

<span data-ttu-id="a8691-123">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a8691-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a8691-124">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a8691-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8691-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8691-125">Requirements</span></span>



| <span data-ttu-id="a8691-126">需求</span><span class="sxs-lookup"><span data-stu-id="a8691-126">Requirement</span></span> | <span data-ttu-id="a8691-127">值</span><span class="sxs-lookup"><span data-stu-id="a8691-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8691-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8691-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a8691-129">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8691-129">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a8691-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8691-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a8691-131">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8691-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8691-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a8691-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8691-133"><dt>Srpapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8691-133"><dt>Srpapi.dll</dt></span></span> </dl> |



 

