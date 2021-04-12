---
description: 註冊 Windows 映像取得 (WIA) 2.0 事件通知的執行中應用程式。
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'IWiaDevMgr2：： RegisterEventCallbackInterface 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192793"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a><span data-ttu-id="e0793-103">IWiaDevMgr2：： RegisterEventCallbackInterface 方法</span><span class="sxs-lookup"><span data-stu-id="e0793-103">IWiaDevMgr2::RegisterEventCallbackInterface method</span></span>

<span data-ttu-id="e0793-104">註冊 Windows 映像取得 (WIA) 2.0 事件通知的執行中應用程式。</span><span class="sxs-lookup"><span data-stu-id="e0793-104">Registers a running application for Windows Image Acquisition (WIA) 2.0 event notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0793-105">語法</span><span class="sxs-lookup"><span data-stu-id="e0793-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a><span data-ttu-id="e0793-106">參數</span><span class="sxs-lookup"><span data-stu-id="e0793-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0793-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e0793-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0793-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="e0793-108">Type: **LONG**</span></span>

<span data-ttu-id="e0793-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="e0793-109">Currently unused.</span></span> <span data-ttu-id="e0793-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="e0793-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e0793-111">*bstrDeviceID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e0793-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0793-112">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e0793-112">Type: **BSTR**</span></span>

<span data-ttu-id="e0793-113">指定 WIA 2.0 裝置的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0793-113">Specifies the unique identifier of a WIA 2.0 device.</span></span> <span data-ttu-id="e0793-114">將此參數設定為 **Null** ，以在所有 WIA 2.0 裝置上註冊事件。</span><span class="sxs-lookup"><span data-stu-id="e0793-114">Set this parameter to **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="e0793-115">*pEventGUID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e0793-115">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0793-116">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="e0793-116">Type: \**const GUID\** _</span></span>

<span data-ttu-id="e0793-117">指定應用程式所註冊之事件識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="e0793-117">Specifies a pointer to the event identifier that the application is registering for.</span></span> <span data-ttu-id="e0793-118">請參閱標準事件識別碼的 [WIA 事件識別碼](-wia-wia-event-identifiers.md) 。</span><span class="sxs-lookup"><span data-stu-id="e0793-118">See [WIA Event Identifiers](-wia-wia-event-identifiers.md) for standard event identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="e0793-119">_pIWiaEventCallback \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0793-119">_pIWiaEventCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0793-120">類型： \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _</span><span class="sxs-lookup"><span data-stu-id="e0793-120">Type: \**[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\** _</span></span>

<span data-ttu-id="e0793-121">指定 WIA 2.0 用來傳送事件通知之 [_ *IWiaEventCallback* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e0793-121">Specifies a pointer to the [_ *IWiaEventCallback*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) interface that the WIA 2.0 uses to send event notification.</span></span>

</dd> <dt>

<span data-ttu-id="e0793-122">*pEventObject* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e0793-122">*pEventObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0793-123">類型： **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="e0793-123">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="e0793-124">接收 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="e0793-124">Receives the address of a pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0793-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0793-125">Return value</span></span>

<span data-ttu-id="e0793-126">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e0793-126">Type: **HRESULT**</span></span>

<span data-ttu-id="e0793-127">傳回標準 COM 錯誤碼或下列。</span><span class="sxs-lookup"><span data-stu-id="e0793-127">Returns the standard COM error codes or the following.</span></span>



| <span data-ttu-id="e0793-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e0793-128">Return code</span></span>                                                                               | <span data-ttu-id="e0793-129">Description</span><span class="sxs-lookup"><span data-stu-id="e0793-129">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0793-130"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e0793-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="e0793-131">無法傳回 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。</span><span class="sxs-lookup"><span data-stu-id="e0793-131">The [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface cannot be returned.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="e0793-132">備註</span><span class="sxs-lookup"><span data-stu-id="e0793-132">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="e0793-133">在仍映射服務重新開機後，使用相同進程中的 [**IWiaDevMgr：： RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface)、 **IWiaDevMgr2：： RegisterEventCallbackInterface** 和 [**DeviceManager**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) 方法，可能會導致存取違規，如果在服務停止之前使用了函數。</span><span class="sxs-lookup"><span data-stu-id="e0793-133">Using the [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2::RegisterEventCallbackInterface**, and [**DeviceManager.RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) methods from the same process after the Still Image Service is restarted may cause an access violation, if the functions were used before the service was stopped.</span></span>

 

<span data-ttu-id="e0793-134">當 WIA 2.0 應用程式開始執行時，會使用這個方法來註冊以接收硬體裝置事件。</span><span class="sxs-lookup"><span data-stu-id="e0793-134">When WIA 2.0 applications begin executing, they use this method to register to receive hardware device events.</span></span> <span data-ttu-id="e0793-135">這可防止應用程式在另一個已註冊的事件發生時重新開機。</span><span class="sxs-lookup"><span data-stu-id="e0793-135">This prevents the application from being restarted when another event for which it is registered occurs.</span></span> <span data-ttu-id="e0793-136">當應用程式呼叫 **IWiaDevMgr2：： RegisterEventCallbackInterface** 來註冊本身以接收來自裝置的 WIA 2.0 事件時，WIA 2.0 會將已註冊的事件路由至程式。</span><span class="sxs-lookup"><span data-stu-id="e0793-136">Once an application calls **IWiaDevMgr2::RegisterEventCallbackInterface** to register itself to receive WIA 2.0 events from a device, the registered events are routed to the program by WIA 2.0.</span></span>

<span data-ttu-id="e0793-137">應用程式必須在透過 *pEventObject* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="e0793-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *pEventObject* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="e0793-138">在多執行緒應用程式中，事件通知回呼可能會與註冊回呼的執行緒位於不同的執行緒上。</span><span class="sxs-lookup"><span data-stu-id="e0793-138">In a multithreaded application, the event notification callback may come in on a different thread from the one that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e0793-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0793-139">Requirements</span></span>



| <span data-ttu-id="e0793-140">需求</span><span class="sxs-lookup"><span data-stu-id="e0793-140">Requirement</span></span> | <span data-ttu-id="e0793-141">值</span><span class="sxs-lookup"><span data-stu-id="e0793-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0793-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0793-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e0793-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0793-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e0793-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0793-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e0793-145">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0793-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e0793-146">標頭</span><span class="sxs-lookup"><span data-stu-id="e0793-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0793-147"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="e0793-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0793-148">Idl</span><span class="sxs-lookup"><span data-stu-id="e0793-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e0793-149"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e0793-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
