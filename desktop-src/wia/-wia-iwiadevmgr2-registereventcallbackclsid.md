---
description: IWiaDevMgr2：： RegisterEventCallbackCLSID 方法會註冊應用程式以接收事件，即使應用程式並未執行也一樣。
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'IWiaDevMgr2：： RegisterEventCallbackCLSID 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 63e69d12d47f90ba40f5cc785d8b864c40158774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512044"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a><span data-ttu-id="f7a40-103">IWiaDevMgr2：： RegisterEventCallbackCLSID 方法</span><span class="sxs-lookup"><span data-stu-id="f7a40-103">IWiaDevMgr2::RegisterEventCallbackCLSID method</span></span>

<span data-ttu-id="f7a40-104">**IWiaDevMgr2：： RegisterEventCallbackCLSID** 方法會註冊應用程式以接收事件，即使應用程式並未執行也一樣。</span><span class="sxs-lookup"><span data-stu-id="f7a40-104">The **IWiaDevMgr2::RegisterEventCallbackCLSID** method registers an application to receive events even if the application is not running.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a40-105">語法</span><span class="sxs-lookup"><span data-stu-id="f7a40-105">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="f7a40-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7a40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7a40-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7a40-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a40-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="f7a40-108">Type: **LONG**</span></span>

<span data-ttu-id="f7a40-109">指定註冊旗標。</span><span class="sxs-lookup"><span data-stu-id="f7a40-109">Specifies registration flags.</span></span> <span data-ttu-id="f7a40-110">可以設定為下列值：</span><span class="sxs-lookup"><span data-stu-id="f7a40-110">Can be set to the following values:</span></span>



| <span data-ttu-id="f7a40-111">註冊旗標</span><span class="sxs-lookup"><span data-stu-id="f7a40-111">Registration Flag</span></span>                | <span data-ttu-id="f7a40-112">意義</span><span class="sxs-lookup"><span data-stu-id="f7a40-112">Meaning</span></span>                                           |
|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="f7a40-113">WIA \_ 註冊 \_ 事件 \_ 回呼</span><span class="sxs-lookup"><span data-stu-id="f7a40-113">WIA\_REGISTER\_EVENT\_CALLBACK</span></span>   | <span data-ttu-id="f7a40-114">報名活動。</span><span class="sxs-lookup"><span data-stu-id="f7a40-114">Register for the event.</span></span>                           |
| <span data-ttu-id="f7a40-115">WIA \_ 取消註冊 \_ 事件 \_ 回呼</span><span class="sxs-lookup"><span data-stu-id="f7a40-115">WIA\_UNREGISTER\_EVENT\_CALLBACK</span></span> | <span data-ttu-id="f7a40-116">刪除事件的註冊。</span><span class="sxs-lookup"><span data-stu-id="f7a40-116">Delete the registration for the event.</span></span>            |
| <span data-ttu-id="f7a40-117">WIA \_ 設定 \_ 預設 \_ 處理常式</span><span class="sxs-lookup"><span data-stu-id="f7a40-117">WIA\_SET\_DEFAULT\_HANDLER</span></span>       | <span data-ttu-id="f7a40-118">將應用程式設定為預設事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="f7a40-118">Set the application as the default event handler.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f7a40-119">*bstrDeviceID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7a40-119">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a40-120">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f7a40-120">Type: **BSTR**</span></span>

<span data-ttu-id="f7a40-121">指定裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7a40-121">Specifies a device identifier.</span></span> <span data-ttu-id="f7a40-122">傳遞 **Null** 以註冊所有 WIA 2.0 裝置上的事件。</span><span class="sxs-lookup"><span data-stu-id="f7a40-122">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="f7a40-123">*pEventGUID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7a40-123">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a40-124">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="f7a40-124">Type: \**const GUID\** _</span></span>

<span data-ttu-id="f7a40-125">指定應用程式註冊的事件。</span><span class="sxs-lookup"><span data-stu-id="f7a40-125">Specifies the event that the application is registering for.</span></span> <span data-ttu-id="f7a40-126">如需標準事件的清單，請參閱 [WIA 事件識別碼](-wia-wia-event-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="f7a40-126">For a list of standard events, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7a40-127">_pClsID \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7a40-127">_pClsID\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a40-128">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="f7a40-128">Type: \**const GUID\** _</span></span>

<span data-ttu-id="f7a40-129">應用程式類別識別碼的指標 (_ \* CLSID \* \* ) 。</span><span class="sxs-lookup"><span data-stu-id="f7a40-129">Pointer to the application class ID (_\*CLSID\*\*).</span></span> <span data-ttu-id="f7a40-130">當事件發生時，WIA 2.0 執行時間系統會使用應用程式 **CLSID** 來啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="f7a40-130">The WIA 2.0 run-time system uses the application **CLSID** to start the application when an event occurs that it is registered for.</span></span>

</dd> <dt>

<span data-ttu-id="f7a40-131">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7a40-131">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a40-132">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f7a40-132">Type: **BSTR**</span></span>

<span data-ttu-id="f7a40-133">指定為事件註冊的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="f7a40-133">Specifies the name of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="f7a40-134">*bstrDescription* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7a40-134">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a40-135">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f7a40-135">Type: **BSTR**</span></span>

<span data-ttu-id="f7a40-136">指定針對事件註冊之應用程式的文字描述。</span><span class="sxs-lookup"><span data-stu-id="f7a40-136">Specifies a text description of the application that registers for the event.</span></span>

</dd> <dt>

<span data-ttu-id="f7a40-137">*bstrIcon* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7a40-137">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7a40-138">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f7a40-138">Type: **BSTR**</span></span>

<span data-ttu-id="f7a40-139">指定要用於註冊事件之應用程式圖示的影像檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="f7a40-139">Specifies the name of an image file to use for the icon for the application that registers for the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7a40-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7a40-140">Return value</span></span>

<span data-ttu-id="f7a40-141">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f7a40-141">Type: **HRESULT**</span></span>

<span data-ttu-id="f7a40-142">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f7a40-142">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f7a40-143">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f7a40-143">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7a40-144">備註</span><span class="sxs-lookup"><span data-stu-id="f7a40-144">Remarks</span></span>

<span data-ttu-id="f7a40-145">WIA 2.0 應用程式會使用這個方法來註冊，以接收硬體裝置事件。</span><span class="sxs-lookup"><span data-stu-id="f7a40-145">WIA 2.0 applications use this method to register to receive hardware device events.</span></span> <span data-ttu-id="f7a40-146">在呼叫 **IWiaDevMgr2：： RegisterEventCallbackCLSID** 之後，應用程式會註冊以接收 WIA 2.0 裝置事件，即使它並未執行也一樣。</span><span class="sxs-lookup"><span data-stu-id="f7a40-146">After **IWiaDevMgr2::RegisterEventCallbackCLSID** is called, the application is registered to receive WIA 2.0 device events even if it is not running.</span></span>

<span data-ttu-id="f7a40-147">當事件發生時，WIA 2.0 系統會決定要註冊哪個應用程式以接收事件。</span><span class="sxs-lookup"><span data-stu-id="f7a40-147">When the event occurs, the WIA 2.0 system determines which application is registered to receive the event.</span></span> <span data-ttu-id="f7a40-148">它會使用 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數和 *pClsID* 參數中指定的 CLSID 來建立應用程式的實例，然後呼叫 [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) 方法，將事件資訊傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="f7a40-148">It uses the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and the CLSID specified in the *pClsID* parameter to create an instance of the application, and then calls the [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method to transmit the event information to the application.</span></span>

<span data-ttu-id="f7a40-149">應用程式可以叫用 [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) 方法來列舉事件註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="f7a40-149">An application can invoke the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to enumerate event registration information.</span></span>

<span data-ttu-id="f7a40-150">如果應用程式不是已註冊的元件物件模型 (COM) 元件，而且與 WIA 2.0 架構不相容，請使用 [**IWiaDevMgr2：： RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) 方法來註冊裝置事件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f7a40-150">If the application is not a registered Component Object Model (COM) component and is not compatible with the WIA 2.0 architecture, use the [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method to register an application for device events.</span></span>

> [!Note]  
> <span data-ttu-id="f7a40-151">在多執行緒應用程式中，並不保證會在註冊回呼的相同執行緒上傳回事件通知回呼。</span><span class="sxs-lookup"><span data-stu-id="f7a40-151">In a multi-threaded application, there is no guarantee that the event notification callback is returned on the same thread that registered the callback.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f7a40-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7a40-152">Requirements</span></span>



| <span data-ttu-id="f7a40-153">需求</span><span class="sxs-lookup"><span data-stu-id="f7a40-153">Requirement</span></span> | <span data-ttu-id="f7a40-154">值</span><span class="sxs-lookup"><span data-stu-id="f7a40-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f7a40-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7a40-155">Minimum supported client</span></span><br/> | <span data-ttu-id="f7a40-156">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7a40-156">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f7a40-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7a40-157">Minimum supported server</span></span><br/> | <span data-ttu-id="f7a40-158">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7a40-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f7a40-159">標頭</span><span class="sxs-lookup"><span data-stu-id="f7a40-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7a40-160"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="f7a40-160"><dt>Wia.h</dt></span></span> </dl> |



 

 
