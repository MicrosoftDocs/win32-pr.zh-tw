---
description: IWiaDevMgr2：： RegisterEventCallbackProgram 方法會註冊應用程式以接收裝置事件。 它主要是為了提供與未針對 Windows 映像取得所撰寫之應用程式的回溯相容性， (WIA) 2.0。
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'IWiaDevMgr2：： RegisterEventCallbackProgram 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b18b5833b7616493c24f0128caa7c910b685e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974084"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a><span data-ttu-id="a371f-104">IWiaDevMgr2：： RegisterEventCallbackProgram 方法</span><span class="sxs-lookup"><span data-stu-id="a371f-104">IWiaDevMgr2::RegisterEventCallbackProgram method</span></span>

<span data-ttu-id="a371f-105">**IWiaDevMgr2：： RegisterEventCallbackProgram** 方法會註冊應用程式以接收裝置事件。</span><span class="sxs-lookup"><span data-stu-id="a371f-105">The **IWiaDevMgr2::RegisterEventCallbackProgram** method registers an application to receive device events.</span></span> <span data-ttu-id="a371f-106">它主要是為了提供與未針對 Windows 映像取得所撰寫之應用程式的回溯相容性， (WIA) 2.0。</span><span class="sxs-lookup"><span data-stu-id="a371f-106">It is primarily provided for backward compatibility with applications that were not written for Windows Image Acquisition (WIA) 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="a371f-107">語法</span><span class="sxs-lookup"><span data-stu-id="a371f-107">Syntax</span></span>


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a><span data-ttu-id="a371f-108">參數</span><span class="sxs-lookup"><span data-stu-id="a371f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a371f-109">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a371f-109">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a371f-110">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="a371f-110">Type: **LONG**</span></span>

<span data-ttu-id="a371f-111">註冊旗標。</span><span class="sxs-lookup"><span data-stu-id="a371f-111">The registration flags.</span></span> <span data-ttu-id="a371f-112">可以設定為下列值。</span><span class="sxs-lookup"><span data-stu-id="a371f-112">Can be set to the following values.</span></span>



| <span data-ttu-id="a371f-113">值</span><span class="sxs-lookup"><span data-stu-id="a371f-113">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="a371f-114">意義</span><span class="sxs-lookup"><span data-stu-id="a371f-114">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <span data-ttu-id="a371f-115"><dt>**WIA \_ 註冊 \_ 事件 \_ 回呼**</dt></span><span class="sxs-lookup"><span data-stu-id="a371f-115"><dt>**WIA\_REGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl>       | <span data-ttu-id="a371f-116">報名活動。</span><span class="sxs-lookup"><span data-stu-id="a371f-116">Register for the event.</span></span><br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <span data-ttu-id="a371f-117"><dt>**WIA \_ 取消註冊 \_ 事件 \_ 回呼**</dt></span><span class="sxs-lookup"><span data-stu-id="a371f-117"><dt>**WIA\_UNREGISTER\_EVENT\_CALLBACK**</dt></span></span> </dl> | <span data-ttu-id="a371f-118">刪除事件的註冊。</span><span class="sxs-lookup"><span data-stu-id="a371f-118">Delete the registration for the event.</span></span><br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <span data-ttu-id="a371f-119"><dt>**WIA \_ 設定 \_ 預設 \_ 處理常式**</dt></span><span class="sxs-lookup"><span data-stu-id="a371f-119"><dt>**WIA\_SET\_DEFAULT\_HANDLER**</dt></span></span> </dl>                   | <span data-ttu-id="a371f-120">將應用程式設定為預設事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="a371f-120">Set the application as the default event handler.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a371f-121">*bstrDeviceID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a371f-121">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a371f-122">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a371f-122">Type: **BSTR**</span></span>

<span data-ttu-id="a371f-123">裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="a371f-123">A device identifier.</span></span> <span data-ttu-id="a371f-124">傳遞 **Null** 以註冊所有 WIA 2.0 裝置上的事件。</span><span class="sxs-lookup"><span data-stu-id="a371f-124">Pass **NULL** to register for the event on all WIA 2.0 devices.</span></span>

</dd> <dt>

<span data-ttu-id="a371f-125">*pEventGUID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a371f-125">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a371f-126">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="a371f-126">Type: \**const GUID\** _</span></span>

<span data-ttu-id="a371f-127">應用程式正在註冊的事件。</span><span class="sxs-lookup"><span data-stu-id="a371f-127">The event that the application is registering for.</span></span> <span data-ttu-id="a371f-128">如需有效的事件 Guid 清單，請參閱 [WIA 事件識別碼](-wia-wia-event-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="a371f-128">For a list of valid event GUIDs, see [WIA Event Identifiers](-wia-wia-event-identifiers.md).</span></span>

</dd> <dt>

<span data-ttu-id="a371f-129">_bstrFullAppName \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a371f-129">_bstrFullAppName\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a371f-130">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a371f-130">Type: **BSTR**</span></span>

<span data-ttu-id="a371f-131">應用程式的完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="a371f-131">The full path name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="a371f-132">*bstrCommandlineArg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a371f-132">*bstrCommandlineArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a371f-133">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a371f-133">Type: **BSTR**</span></span>

<span data-ttu-id="a371f-134">應用程式的適當命令列引數。</span><span class="sxs-lookup"><span data-stu-id="a371f-134">The appropriate command-line arguments for the application.</span></span>

</dd> <dt>

<span data-ttu-id="a371f-135">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a371f-135">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a371f-136">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a371f-136">Type: **BSTR**</span></span>

<span data-ttu-id="a371f-137">應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a371f-137">The name of the application.</span></span> <span data-ttu-id="a371f-138">當有多個應用程式註冊相同的事件時，就會向使用者顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a371f-138">The name is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="a371f-139">*bstrDescription* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a371f-139">*bstrDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a371f-140">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a371f-140">Type: **BSTR**</span></span>

<span data-ttu-id="a371f-141">應用程式的描述。</span><span class="sxs-lookup"><span data-stu-id="a371f-141">The description of the application.</span></span> <span data-ttu-id="a371f-142">當有多個應用程式註冊相同的事件時，就會向使用者顯示描述。</span><span class="sxs-lookup"><span data-stu-id="a371f-142">The description is displayed to the user when multiple applications register for the same event.</span></span>

</dd> <dt>

<span data-ttu-id="a371f-143">*bstrIcon* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a371f-143">*bstrIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a371f-144">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a371f-144">Type: **BSTR**</span></span>

<span data-ttu-id="a371f-145">表示應用程式的圖示。</span><span class="sxs-lookup"><span data-stu-id="a371f-145">The icon that represents the application.</span></span> <span data-ttu-id="a371f-146">當有多個應用程式註冊相同的事件時，使用者會看到圖示。</span><span class="sxs-lookup"><span data-stu-id="a371f-146">The icon is displayed to the user when multiple applications register for the same event.</span></span> <span data-ttu-id="a371f-147">字串包含應用程式的名稱，以及圖示以零為基底的索引（以逗號分隔），例如 "MyApp，0"。</span><span class="sxs-lookup"><span data-stu-id="a371f-147">The string contains the name of the application and the zero-based index of the icon separated by a comma, for example, "MyApp, 0".</span></span> <span data-ttu-id="a371f-148">可能有一個以上代表應用程式的圖示。</span><span class="sxs-lookup"><span data-stu-id="a371f-148">There might be more than one icon that represents an application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a371f-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="a371f-149">Return value</span></span>

<span data-ttu-id="a371f-150">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a371f-150">Type: **HRESULT**</span></span>

<span data-ttu-id="a371f-151">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a371f-151">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a371f-152">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a371f-152">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a371f-153">備註</span><span class="sxs-lookup"><span data-stu-id="a371f-153">Remarks</span></span>

<span data-ttu-id="a371f-154">使用 **IWiaDevMgr2：： RegisterEventCallbackProgram** 來註冊硬體裝置事件。</span><span class="sxs-lookup"><span data-stu-id="a371f-154">Use **IWiaDevMgr2::RegisterEventCallbackProgram** to register for hardware device events.</span></span> <span data-ttu-id="a371f-155">當應用程式註冊的事件發生時，就會啟動應用程式，並將事件資訊傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="a371f-155">When an event occurs that an application is registered for, the application is launched, and the event information is transmitted to the application.</span></span>

<span data-ttu-id="a371f-156">您可以使用 [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) 方法來取得事件註冊屬性之列舉值物件的指標。</span><span class="sxs-lookup"><span data-stu-id="a371f-156">Use the [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method to retrieve a pointer to an enumerator object for event registration properties.</span></span>

<span data-ttu-id="a371f-157">只使用 **IWiaDevMgr2：： RegisterEventCallbackProgram** 方法，與未針對 WIA 2.0 架構撰寫的應用程式回溯相容。</span><span class="sxs-lookup"><span data-stu-id="a371f-157">Only use the **IWiaDevMgr2::RegisterEventCallbackProgram** method for backward compatibility with applications not written for the WIA 2.0 architecture.</span></span> <span data-ttu-id="a371f-158">針對新的應用程式，使用 WIA 2.0 架構所提供的 COM) 介面 (元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="a371f-158">Use the Component Object Model (COM) interfaces provided by the WIA 2.0 architecture for new applications.</span></span> <span data-ttu-id="a371f-159">具體而言，請呼叫 [**IWiaDevMgr2：： RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) 或 [**IWiaDevMgr2：： RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) ，以針對裝置事件註冊新的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a371f-159">Specifically, call [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) to register a new application for device events.</span></span>

<span data-ttu-id="a371f-160">一般來說，這個方法是由安裝程式或腳本呼叫。</span><span class="sxs-lookup"><span data-stu-id="a371f-160">Typically, this method is called by an install program or a script.</span></span> <span data-ttu-id="a371f-161">安裝程式或腳本會註冊應用程式，以接收 WIA 2.0 裝置事件。</span><span class="sxs-lookup"><span data-stu-id="a371f-161">The install program or script registers the application to receive WIA 2.0 device events.</span></span> <span data-ttu-id="a371f-162">當事件發生時，WIA 2.0 執行時間系統會啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="a371f-162">When the event occurs, the application is started by the WIA 2.0 run-time system.</span></span>

## <a name="requirements"></a><span data-ttu-id="a371f-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="a371f-163">Requirements</span></span>



| <span data-ttu-id="a371f-164">需求</span><span class="sxs-lookup"><span data-stu-id="a371f-164">Requirement</span></span> | <span data-ttu-id="a371f-165">值</span><span class="sxs-lookup"><span data-stu-id="a371f-165">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a371f-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a371f-166">Minimum supported client</span></span><br/> | <span data-ttu-id="a371f-167">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a371f-167">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a371f-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a371f-168">Minimum supported server</span></span><br/> | <span data-ttu-id="a371f-169">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a371f-169">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a371f-170">標頭</span><span class="sxs-lookup"><span data-stu-id="a371f-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="a371f-171"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="a371f-171"><dt>Wia.h</dt></span></span> </dl> |



 

 




