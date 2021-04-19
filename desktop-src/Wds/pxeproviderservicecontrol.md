---
title: PxeProviderServiceControl 回呼函式
description: 當 WDS 服務收到服務控制程式代碼時呼叫。
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- PxeProviderServiceControl 回呼函式 Windows 部署服務
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967966"
---
# <a name="pxeproviderservicecontrol-callback-function"></a><span data-ttu-id="afe79-104">PxeProviderServiceControl 回呼函式</span><span class="sxs-lookup"><span data-stu-id="afe79-104">PxeProviderServiceControl callback function</span></span>

<span data-ttu-id="afe79-105">當 WDS 服務收到服務控制程式代碼時呼叫。</span><span class="sxs-lookup"><span data-stu-id="afe79-105">Called when a service control code is received by the WDS service.</span></span> <span data-ttu-id="afe79-106">藉由呼叫 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函數，並將 *CallbackType* 參數設定為 **PXE \_ 回呼 \_ 服務 \_ 控制**，即可註冊此回呼函式。</span><span class="sxs-lookup"><span data-stu-id="afe79-106">This callback function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SERVICE\_CONTROL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe79-107">語法</span><span class="sxs-lookup"><span data-stu-id="afe79-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a><span data-ttu-id="afe79-108">參數</span><span class="sxs-lookup"><span data-stu-id="afe79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afe79-109">*pCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="afe79-109">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afe79-110">傳遞至 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函數的內容值。</span><span class="sxs-lookup"><span data-stu-id="afe79-110">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> <dt>

<span data-ttu-id="afe79-111">*dwControl*</span><span class="sxs-lookup"><span data-stu-id="afe79-111">*dwControl*</span></span> 
</dt> <dd>

<span data-ttu-id="afe79-112">控制程式代碼。</span><span class="sxs-lookup"><span data-stu-id="afe79-112">Control code.</span></span> <span data-ttu-id="afe79-113">如需可能值的清單，請參閱 [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)函數的 *dwControl* 參數。</span><span class="sxs-lookup"><span data-stu-id="afe79-113">For the list of possible values, see the *dwControl* parameter of the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afe79-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="afe79-114">Return value</span></span>

<span data-ttu-id="afe79-115">如果提供者關閉成功，回呼應該會傳回 **錯誤 \_ 成功**。</span><span class="sxs-lookup"><span data-stu-id="afe79-115">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="afe79-116">如果發生失敗，則應該傳回適當的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="afe79-116">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="afe79-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="afe79-117">Requirements</span></span>



| <span data-ttu-id="afe79-118">需求</span><span class="sxs-lookup"><span data-stu-id="afe79-118">Requirement</span></span> | <span data-ttu-id="afe79-119">值</span><span class="sxs-lookup"><span data-stu-id="afe79-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="afe79-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afe79-120">Minimum supported client</span></span><br/> | <span data-ttu-id="afe79-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="afe79-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="afe79-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afe79-122">Minimum supported server</span></span><br/> | <span data-ttu-id="afe79-123">僅限 windows Server 2008、Windows Server 2003 SP2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afe79-123">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="afe79-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afe79-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe79-125">Windows 部署服務伺服器函數</span><span class="sxs-lookup"><span data-stu-id="afe79-125">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="afe79-126">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="afe79-126">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

