---
title: PxeProviderInitialize 回呼函式
description: 從提供者動態連結程式庫匯出 (DLL) ，它會初始化提供者，並讓它準備好接收用戶端要求。
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- PxeProviderInitialize 回呼函式 Windows 部署服務
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966533"
---
# <a name="pxeproviderinitialize-callback-function"></a><span data-ttu-id="8b842-104">PxeProviderInitialize 回呼函式</span><span class="sxs-lookup"><span data-stu-id="8b842-104">PxeProviderInitialize callback function</span></span>

<span data-ttu-id="8b842-105">從提供者動態連結程式庫匯出 (DLL) ，它會初始化提供者，並讓它準備好接收用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="8b842-105">An export from a provider dynamic-link library (DLL) that initializes the provider and prepares it to receive client requests.</span></span> <span data-ttu-id="8b842-106">需要提供者才能匯出 *PxeProviderInitialize* 函數。</span><span class="sxs-lookup"><span data-stu-id="8b842-106">Providers are required to export the *PxeProviderInitialize* function.</span></span> <span data-ttu-id="8b842-107">對提供者的任何回呼都必須在處理 *PxeProviderInitialize* 期間，向 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)函式的呼叫註冊。</span><span class="sxs-lookup"><span data-stu-id="8b842-107">Any callbacks to the provider must be registered with a call to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function during the processing of *PxeProviderInitialize*.</span></span> <span data-ttu-id="8b842-108">當此函式傳回時，提供者必須完全初始化並準備好處理用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="8b842-108">On the return of this function, the provider must be fully initialized and ready to process client requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b842-109">語法</span><span class="sxs-lookup"><span data-stu-id="8b842-109">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a><span data-ttu-id="8b842-110">參數</span><span class="sxs-lookup"><span data-stu-id="8b842-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b842-111">*hProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b842-111">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b842-112">提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b842-112">Handle to the provider instance.</span></span> <span data-ttu-id="8b842-113">這個控制碼必須由提供者儲存，並在後續的呼叫中使用。</span><span class="sxs-lookup"><span data-stu-id="8b842-113">This handle must be stored by the provider and used in any subsequent calls.</span></span> <span data-ttu-id="8b842-114">在呼叫 [*PxeProviderShutdown*](pxeprovidershutdown.md) 回呼函式之前，這個控制碼是有效的。</span><span class="sxs-lookup"><span data-stu-id="8b842-114">This handle is valid until the [*PxeProviderShutdown*](pxeprovidershutdown.md) callback function is called.</span></span>

</dd> <dt>

<span data-ttu-id="8b842-115">*hProviderKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b842-115">*hProviderKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b842-116">要儲存提供者設定資訊之登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b842-116">Handle to a registry key where provider configuration information is to be stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b842-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b842-117">Return value</span></span>

<span data-ttu-id="8b842-118">如果提供者初始化成功，回呼應該會傳回 **錯誤 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="8b842-118">If the provider initialization succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="8b842-119">如果發生失敗，則應該傳回適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8b842-119">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b842-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b842-120">Requirements</span></span>



| <span data-ttu-id="8b842-121">需求</span><span class="sxs-lookup"><span data-stu-id="8b842-121">Requirement</span></span> | <span data-ttu-id="8b842-122">值</span><span class="sxs-lookup"><span data-stu-id="8b842-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8b842-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b842-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8b842-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="8b842-124">None supported</span></span><br/>                                                          |
| <span data-ttu-id="8b842-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b842-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8b842-126">僅限 windows Server 2008、Windows Server 2003 SP2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b842-126">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b842-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b842-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b842-128">Windows 部署服務伺服器函數</span><span class="sxs-lookup"><span data-stu-id="8b842-128">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="8b842-129">*PxeProviderShutdown*</span><span class="sxs-lookup"><span data-stu-id="8b842-129">*PxeProviderShutdown*</span></span>](pxeprovidershutdown.md)
</dt> </dl>

 

 





