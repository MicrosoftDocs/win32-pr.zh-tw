---
description: IWiaDevMgr2：： SelectDeviceDlg 方法-顯示對話方塊，讓使用者選取硬體裝置以取得影像。
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'IWiaDevMgr2：： SelectDeviceDlg 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 60ec24f264b8fe0424f17fc32deaf803e55c3346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091256"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a><span data-ttu-id="8e72e-103">IWiaDevMgr2：： SelectDeviceDlg 方法</span><span class="sxs-lookup"><span data-stu-id="8e72e-103">IWiaDevMgr2::SelectDeviceDlg method</span></span>

<span data-ttu-id="8e72e-104">顯示對話方塊，讓使用者選取硬體裝置以取得影像。</span><span class="sxs-lookup"><span data-stu-id="8e72e-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e72e-105">語法</span><span class="sxs-lookup"><span data-stu-id="8e72e-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a><span data-ttu-id="8e72e-106">參數</span><span class="sxs-lookup"><span data-stu-id="8e72e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e72e-107">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e72e-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e72e-108">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="8e72e-108">Type: **HWND**</span></span>

<span data-ttu-id="8e72e-109">指定 [ **選取裝置** ] 對話方塊的父視窗。</span><span class="sxs-lookup"><span data-stu-id="8e72e-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="8e72e-110">*lDeviceType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e72e-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e72e-111">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="8e72e-111">Type: **LONG**</span></span>

<span data-ttu-id="8e72e-112">指定要使用的 WIA 2.0 裝置類型。</span><span class="sxs-lookup"><span data-stu-id="8e72e-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="8e72e-113">如需可能值的清單，請參閱 [WIA 裝置類型](-wia-wia-device-type-specifiers.md) 規範。</span><span class="sxs-lookup"><span data-stu-id="8e72e-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="8e72e-114">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e72e-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e72e-115">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="8e72e-115">Type: **LONG**</span></span>

<span data-ttu-id="8e72e-116">指定對話方塊的行為。</span><span class="sxs-lookup"><span data-stu-id="8e72e-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="8e72e-117">值可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="8e72e-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="8e72e-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="8e72e-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="8e72e-119">使用預設行為。</span><span class="sxs-lookup"><span data-stu-id="8e72e-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="8e72e-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ 選取 \_ 裝置 \_ NODEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8e72e-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="8e72e-121">即使只有一個相符的裝置，仍顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="8e72e-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8e72e-122">*pbstrDeviceID* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8e72e-122">*pbstrDeviceID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e72e-123">類型： **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="8e72e-123">Type: **BSTR\***</span></span>

<span data-ttu-id="8e72e-124">在輸出時，會接收包含裝置識別碼字串的字串。</span><span class="sxs-lookup"><span data-stu-id="8e72e-124">On output, receives a string which contains the device's identifier string.</span></span> <span data-ttu-id="8e72e-125">在輸入時，如果需要這項資訊，請傳遞指標的位址，如果不需要，則傳遞 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8e72e-125">On input, pass the address of a pointer if this information is needed, or **NULL** if it is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="8e72e-126">*ppItemRoot* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="8e72e-126">*ppItemRoot* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8e72e-127">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8e72e-127">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="8e72e-128">接收階層樹狀結構的根項目之 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標位址，此介面表示所選的 WIA 2.0 裝置。</span><span class="sxs-lookup"><span data-stu-id="8e72e-128">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item of the hierarchical tree that represents the selected WIA 2.0 device.</span></span> <span data-ttu-id="8e72e-129">如果找不到任何裝置，則會收到 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8e72e-129">If no device is found, it receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e72e-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e72e-130">Return value</span></span>

<span data-ttu-id="8e72e-131">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8e72e-131">Type: **HRESULT**</span></span>

<span data-ttu-id="8e72e-132">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8e72e-132">This method can return one of these values.</span></span>



| <span data-ttu-id="8e72e-133">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8e72e-133">Return code</span></span>                                                                                                  | <span data-ttu-id="8e72e-134">Description</span><span class="sxs-lookup"><span data-stu-id="8e72e-134">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e72e-135"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8e72e-135"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="8e72e-136">已成功選取裝置。</span><span class="sxs-lookup"><span data-stu-id="8e72e-136">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="8e72e-137"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="8e72e-137"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="8e72e-138">使用者已取消對話方塊。</span><span class="sxs-lookup"><span data-stu-id="8e72e-138">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="8e72e-139"><dt>**WIA \_ S \_ 沒有 \_ 任何 \_ 可用的裝置**</dt></span><span class="sxs-lookup"><span data-stu-id="8e72e-139"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="8e72e-140">沒有任何 WIA 2.0 硬體裝置符合 *lDeviceType* 參數中提供的規格。</span><span class="sxs-lookup"><span data-stu-id="8e72e-140">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="8e72e-141">備註</span><span class="sxs-lookup"><span data-stu-id="8e72e-141">Remarks</span></span>

<span data-ttu-id="8e72e-142">此方法會建立並顯示 [ **選取裝置** ] 對話方塊，讓使用者可以選取 WIA 2.0 裝置來取得影像。</span><span class="sxs-lookup"><span data-stu-id="8e72e-142">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="8e72e-143">如果成功選取裝置， **IWiaDevMgr2：： SelectDeviceDlg** 方法會為裝置建立 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="8e72e-143">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlg** method creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for the device.</span></span> <span data-ttu-id="8e72e-144">它會在參數 *ppItemRoot* 中儲存根項目之 **IWiaItem2** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="8e72e-144">It stores a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span>

<span data-ttu-id="8e72e-145">應用程式可以透過 *lDeviceType* 參數指定裝置類型，以將向使用者顯示的裝置限制為特定類型。</span><span class="sxs-lookup"><span data-stu-id="8e72e-145">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="8e72e-146">如果只有一部裝置符合規格， **IWiaDevMgr2：： SelectDeviceDlg** 不會顯示 [ **選取裝置** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="8e72e-146">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlg** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="8e72e-147">相反地，它會建立裝置的 [**IWiaItem2**](-wia-iwiaitem2.md)樹狀結構，並在參數 *ppItemRoot* 中儲存根項目的 **IWiaItem2** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="8e72e-147">Instead it creates the [**IWiaItem2**](-wia-iwiaitem2.md) tree for the device and store a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span> <span data-ttu-id="8e72e-148">您可以覆寫此行為，並強制 **IWiaDevMgr2：： SelectDeviceDlg** 藉由指定 WIA \_ SELECT \_ DEVICE \_ NODEFAULT 作為 *lFlags* 參數的值來顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="8e72e-148">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlg** to display the dialog box by specifying WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="8e72e-149">如果有一個以上的 WIA 2.0 裝置符合規格，則所有相符的裝置都會顯示在 [ **選取裝置** ] 對話方塊中，讓使用者可以選擇其中一個。</span><span class="sxs-lookup"><span data-stu-id="8e72e-149">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the **Select Device** dialog box so the user may choose one.</span></span>

<span data-ttu-id="8e72e-150">應用程式必須在透過 *ppItemRoot* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="8e72e-150">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppItemRoot* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="8e72e-151">建議應用程式 **在 [檔案**] 功能表上，透過 [掃描器]**中** 名稱為的功能表項目，讓裝置和影像可供選擇。</span><span class="sxs-lookup"><span data-stu-id="8e72e-151">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8e72e-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e72e-152">Requirements</span></span>



| <span data-ttu-id="8e72e-153">需求</span><span class="sxs-lookup"><span data-stu-id="8e72e-153">Requirement</span></span> | <span data-ttu-id="8e72e-154">值</span><span class="sxs-lookup"><span data-stu-id="8e72e-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e72e-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e72e-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8e72e-156">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e72e-156">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8e72e-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e72e-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8e72e-158">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e72e-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8e72e-159">標頭</span><span class="sxs-lookup"><span data-stu-id="8e72e-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e72e-160"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="8e72e-160"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e72e-161">Idl</span><span class="sxs-lookup"><span data-stu-id="8e72e-161">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8e72e-162"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8e72e-162"><dt>Wia.idl</dt></span></span> </dl> |



 

 
