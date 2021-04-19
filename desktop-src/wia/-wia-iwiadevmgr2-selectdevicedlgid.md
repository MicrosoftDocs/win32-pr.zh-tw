---
description: 顯示對話方塊，讓使用者選取硬體裝置以取得影像。
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'IWiaDevMgr2：： SelectDeviceDlgID 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bad749eb48e72b362070ea4951d4e9eac380e737
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972674"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a><span data-ttu-id="338f9-103">IWiaDevMgr2：： SelectDeviceDlgID 方法</span><span class="sxs-lookup"><span data-stu-id="338f9-103">IWiaDevMgr2::SelectDeviceDlgID method</span></span>

<span data-ttu-id="338f9-104">顯示對話方塊，讓使用者選取硬體裝置以取得影像。</span><span class="sxs-lookup"><span data-stu-id="338f9-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="338f9-105">語法</span><span class="sxs-lookup"><span data-stu-id="338f9-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="338f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="338f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="338f9-107">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="338f9-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="338f9-108">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="338f9-108">Type: **HWND**</span></span>

<span data-ttu-id="338f9-109">指定 [ **選取裝置** ] 對話方塊的父視窗。</span><span class="sxs-lookup"><span data-stu-id="338f9-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="338f9-110">*lDeviceType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="338f9-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="338f9-111">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="338f9-111">Type: **LONG**</span></span>

<span data-ttu-id="338f9-112">指定要使用的 WIA 2.0 裝置類型。</span><span class="sxs-lookup"><span data-stu-id="338f9-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="338f9-113">如需可能值的清單，請參閱 [WIA 裝置類型](-wia-wia-device-type-specifiers.md) 規範。</span><span class="sxs-lookup"><span data-stu-id="338f9-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="338f9-114">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="338f9-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="338f9-115">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="338f9-115">Type: **LONG**</span></span>

<span data-ttu-id="338f9-116">指定對話方塊的行為。</span><span class="sxs-lookup"><span data-stu-id="338f9-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="338f9-117">值可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="338f9-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="338f9-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="338f9-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="338f9-119">使用預設行為。</span><span class="sxs-lookup"><span data-stu-id="338f9-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="338f9-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ 選取 \_ 裝置 \_ NODEFAULT**</span><span class="sxs-lookup"><span data-stu-id="338f9-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="338f9-121">即使只有一個相符的裝置，仍顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="338f9-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="338f9-122">*pbstrDeviceID* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="338f9-122">*pbstrDeviceID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="338f9-123">類型： \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="338f9-123">Type: \**BSTR\** _</span></span>

<span data-ttu-id="338f9-124">接收裝置識別碼字串之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="338f9-124">Pointer to a string that receives the identifier string of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="338f9-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="338f9-125">Return value</span></span>

<span data-ttu-id="338f9-126">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="338f9-126">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="338f9-127">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="338f9-127">This method can return one of these values.</span></span>



| <span data-ttu-id="338f9-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="338f9-128">Return code</span></span>                                                                                                  | <span data-ttu-id="338f9-129">Description</span><span class="sxs-lookup"><span data-stu-id="338f9-129">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="338f9-130"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="338f9-130"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="338f9-131">已成功選取裝置。</span><span class="sxs-lookup"><span data-stu-id="338f9-131">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="338f9-132"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="338f9-132"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="338f9-133">使用者已取消對話方塊。</span><span class="sxs-lookup"><span data-stu-id="338f9-133">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="338f9-134"><dt>**WIA \_ S \_ 沒有 \_ 任何 \_ 可用的裝置**</dt></span><span class="sxs-lookup"><span data-stu-id="338f9-134"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="338f9-135">沒有任何 WIA 2.0 硬體裝置符合 *lDeviceType* 參數中提供的規格。</span><span class="sxs-lookup"><span data-stu-id="338f9-135">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="338f9-136">備註</span><span class="sxs-lookup"><span data-stu-id="338f9-136">Remarks</span></span>

<span data-ttu-id="338f9-137">此方法會建立並顯示 [ **選取裝置** ] 對話方塊，讓使用者可以選取 WIA 2.0 裝置來取得影像。</span><span class="sxs-lookup"><span data-stu-id="338f9-137">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="338f9-138">如果成功選取裝置， **IWiaDevMgr2：： SelectDeviceDlgID** 方法會透過其 *pbstrDeviceID* 參數，將其識別碼字串傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="338f9-138">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlgID** method passes its identifier string to the application through its *pbstrDeviceID* parameter.</span></span>

<span data-ttu-id="338f9-139">應用程式可以透過 *lDeviceType* 參數指定裝置類型，以將向使用者顯示的裝置限制為特定類型。</span><span class="sxs-lookup"><span data-stu-id="338f9-139">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="338f9-140">如果只有一部裝置符合規格， **IWiaDevMgr2：： SelectDeviceDlgID** 不會顯示 [ **選取裝置** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="338f9-140">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlgID** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="338f9-141">相反地，它會將裝置的識別碼字串傳遞至應用程式，而不會顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="338f9-141">Instead it passes the device's identifier string to the application without displaying the dialog box.</span></span> <span data-ttu-id="338f9-142">您可以覆寫此行為，並強制 **IWiaDevMgr2：： SelectDeviceDlgID** 藉由傳遞 WIA \_ 選取 \_ 裝置 \_ NODEFAULT 作為 *lFlags* 參數的值來顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="338f9-142">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlgID** to display the dialog box by passing WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="338f9-143">如果有一個以上的 WIA 2.0 裝置符合規格，則所有相符的裝置都會顯示在 [SelectDevice] 對話方塊中，讓使用者可以選擇其中一個。</span><span class="sxs-lookup"><span data-stu-id="338f9-143">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the SelectDevice dialog box so the user may choose one.</span></span>

> [!Note]  
> <span data-ttu-id="338f9-144">建議應用程式 **在 [檔案**] 功能表上，透過 [掃描器]**中** 名稱為的功能表項目，讓裝置和影像可供選擇。</span><span class="sxs-lookup"><span data-stu-id="338f9-144">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="338f9-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="338f9-145">Requirements</span></span>



| <span data-ttu-id="338f9-146">需求</span><span class="sxs-lookup"><span data-stu-id="338f9-146">Requirement</span></span> | <span data-ttu-id="338f9-147">值</span><span class="sxs-lookup"><span data-stu-id="338f9-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="338f9-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="338f9-148">Minimum supported client</span></span><br/> | <span data-ttu-id="338f9-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="338f9-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="338f9-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="338f9-150">Minimum supported server</span></span><br/> | <span data-ttu-id="338f9-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="338f9-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="338f9-152">標頭</span><span class="sxs-lookup"><span data-stu-id="338f9-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="338f9-153"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="338f9-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="338f9-154">Idl</span><span class="sxs-lookup"><span data-stu-id="338f9-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="338f9-155"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="338f9-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 




