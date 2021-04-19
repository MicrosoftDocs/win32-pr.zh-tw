---
title: PxeProviderShutdown 回呼函式
description: 呼叫以關閉提供者。
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- PxeProviderShutdown 回呼函式 Windows 部署服務
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980288"
---
# <a name="pxeprovidershutdown-callback-function"></a><span data-ttu-id="057ee-104">PxeProviderShutdown 回呼函式</span><span class="sxs-lookup"><span data-stu-id="057ee-104">PxeProviderShutdown callback function</span></span>

<span data-ttu-id="057ee-105">呼叫以關閉提供者。</span><span class="sxs-lookup"><span data-stu-id="057ee-105">Called to shutdown the provider.</span></span> <span data-ttu-id="057ee-106">藉由呼叫 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函數，並將 *CallbackType* 參數設定為 **PXE \_ 回呼 \_ SHUTDOWN**，即可註冊此函式。</span><span class="sxs-lookup"><span data-stu-id="057ee-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SHUTDOWN**.</span></span> <span data-ttu-id="057ee-107">呼叫此函式之後，傳遞給 [*PxeProviderInitialize*](pxeproviderinitialize.md)函數的 *hProvider* 控制碼將不再有效。</span><span class="sxs-lookup"><span data-stu-id="057ee-107">After this function is called, the *hProvider* handle passed to the [*PxeProviderInitialize*](pxeproviderinitialize.md) function is no longer valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="057ee-108">語法</span><span class="sxs-lookup"><span data-stu-id="057ee-108">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a><span data-ttu-id="057ee-109">參數</span><span class="sxs-lookup"><span data-stu-id="057ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="057ee-110">*pCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="057ee-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="057ee-111">傳遞至 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函數的內容值。</span><span class="sxs-lookup"><span data-stu-id="057ee-111">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="057ee-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="057ee-112">Return value</span></span>

<span data-ttu-id="057ee-113">如果提供者關閉成功，回呼應該會傳回 **錯誤 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="057ee-113">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="057ee-114">如果發生失敗，則應該傳回適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="057ee-114">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="057ee-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="057ee-115">Requirements</span></span>



| <span data-ttu-id="057ee-116">需求</span><span class="sxs-lookup"><span data-stu-id="057ee-116">Requirement</span></span> | <span data-ttu-id="057ee-117">值</span><span class="sxs-lookup"><span data-stu-id="057ee-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="057ee-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="057ee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="057ee-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="057ee-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="057ee-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="057ee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="057ee-121">僅限 windows Server 2008、Windows Server 2003 SP2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="057ee-121">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="057ee-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="057ee-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="057ee-123">Windows 部署服務伺服器函數</span><span class="sxs-lookup"><span data-stu-id="057ee-123">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="057ee-124">*PxeProviderInitialize*</span><span class="sxs-lookup"><span data-stu-id="057ee-124">*PxeProviderInitialize*</span></span>](pxeproviderinitialize.md)
</dt> <dt>

[<span data-ttu-id="057ee-125">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="057ee-125">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





