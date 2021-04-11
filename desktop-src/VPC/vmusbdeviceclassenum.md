---
title: 'VMUSBDeviceClassEnum 列舉 (VPCCOMInterfaces) '
description: 指定 USB 裝置類別。
ms.assetid: 3f5044ea-f7a4-4524-bfb8-55db22732f81
keywords:
- VMUSBDeviceClassEnum 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMUSBDeviceClassEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70335ae083ac2a80717ae64cc8c76f0aff9e791b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104903"
---
# <a name="vmusbdeviceclassenum-enumeration"></a><span data-ttu-id="c2981-104">VMUSBDeviceClassEnum 列舉</span><span class="sxs-lookup"><span data-stu-id="c2981-104">VMUSBDeviceClassEnum enumeration</span></span>

<span data-ttu-id="c2981-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="c2981-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c2981-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="c2981-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c2981-107">指定 USB 裝置類別。</span><span class="sxs-lookup"><span data-stu-id="c2981-107">Specifies the USB device class.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2981-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2981-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUSBDeviceClass_InterfaceDescriptor  = 0x00,
  vmUSBDeviceClass_Audio                = 0x01,
  vmUSBDeviceClass_Communication        = 0x02,
  vmUSBDeviceClass_HID                  = 0x03,
  vmUSBDeviceClass_Physical             = 0x05,
  vmUSBDeviceClass_Image                = 0x06,
  vmUSBDeviceClass_Printer              = 0x07,
  vmUSBDeviceClass_MassStorage          = 0x08,
  vmUSBDeviceClass_Hub                  = 0x09,
  vmUSBDeviceClass_CDCData              = 0x0A,
  vmUSBDeviceClass_SmartCard            = 0x0B,
  vmUSBDeviceClass_ContentSecurity      = 0x0D,
  vmUSBDeviceClass_Video                = 0x0E,
  vmUSBDeviceClass_PersonalHealthcare   = 0x0F,
  vmUSBDeviceClass_DiagnosticDevice     = 0xDC,
  vmUSBDeviceClass_WirelessController   = 0xE0,
  vmUSBDeviceClass_Miscellaneous        = 0xEF,
  vmUSBDeviceClass_ApplicationSpecific  = 0xFE,
  vmUSBDeviceClass_VendorSpecific       = 0xFF
} VMUSBDeviceClassEnum;
```



## <a name="constants"></a><span data-ttu-id="c2981-109">常數</span><span class="sxs-lookup"><span data-stu-id="c2981-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c2981-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**vmUSBDeviceClass \_ InterfaceDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c2981-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**vmUSBDeviceClass\_InterfaceDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-111">無法識別的裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-111">An unidentified device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**vmUSBDeviceClass \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="c2981-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**vmUSBDeviceClass\_Audio**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-113">音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-113">Audio device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**vmUSBDeviceClass \_ 通訊**</span><span class="sxs-lookup"><span data-stu-id="c2981-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**vmUSBDeviceClass\_Communication**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-115">通訊裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-115">Communication device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**vmUSBDeviceClass \_ HID**</span><span class="sxs-lookup"><span data-stu-id="c2981-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**vmUSBDeviceClass\_HID**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-117">HID 裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-117">HID device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmUSBDeviceClass \_ 實體**</span><span class="sxs-lookup"><span data-stu-id="c2981-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmUSBDeviceClass\_Physical**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-119">實體感應式裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-119">Physical sensory device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**vmUSBDeviceClass \_ 影像**</span><span class="sxs-lookup"><span data-stu-id="c2981-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**vmUSBDeviceClass\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-121">正在掃描或映射裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-121">Scanning or imaging device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**vmUSBDeviceClass \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="c2981-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**vmUSBDeviceClass\_Printer**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-123">印表機裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-123">Printer device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmUSBDeviceClass \_ MassStorage**</span><span class="sxs-lookup"><span data-stu-id="c2981-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmUSBDeviceClass\_MassStorage**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-125">大量儲存裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-125">Mass storage device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**vmUSBDeviceClass \_ 中樞**</span><span class="sxs-lookup"><span data-stu-id="c2981-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**vmUSBDeviceClass\_Hub**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-127">中樞裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-127">Hub device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmUSBDeviceClass \_ CDCData**</span><span class="sxs-lookup"><span data-stu-id="c2981-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmUSBDeviceClass\_CDCData**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-129">CDC 資料裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-129">CDC data device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**vmUSBDeviceClass \_ 智慧卡**</span><span class="sxs-lookup"><span data-stu-id="c2981-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**vmUSBDeviceClass\_SmartCard**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-131">智慧卡裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-131">Smart card device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**vmUSBDeviceClass \_ ContentSecurity**</span><span class="sxs-lookup"><span data-stu-id="c2981-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**vmUSBDeviceClass\_ContentSecurity**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-133">內容安全性裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-133">Content security device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**vmUSBDeviceClass \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="c2981-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**vmUSBDeviceClass\_Video**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-135">影片裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-135">Video device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmUSBDeviceClass \_ PersonalHealthcare**</span><span class="sxs-lookup"><span data-stu-id="c2981-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmUSBDeviceClass\_PersonalHealthcare**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-137">保健裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-137">Health care device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmUSBDeviceClass \_ DiagnosticDevice**</span><span class="sxs-lookup"><span data-stu-id="c2981-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmUSBDeviceClass\_DiagnosticDevice**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-139">診斷裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-139">Diagnostic device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmUSBDeviceClass \_ WirelessController**</span><span class="sxs-lookup"><span data-stu-id="c2981-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmUSBDeviceClass\_WirelessController**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-141">無線裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-141">Wireless device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmUSBDeviceClass \_ 其他**</span><span class="sxs-lookup"><span data-stu-id="c2981-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmUSBDeviceClass\_Miscellaneous**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-143">其他裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-143">Miscellaneous device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**vmUSBDeviceClass \_ ApplicationSpecific**</span><span class="sxs-lookup"><span data-stu-id="c2981-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**vmUSBDeviceClass\_ApplicationSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-145">應用程式特定的裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-145">Application-specific device.</span></span>

</dd> <dt>

<span data-ttu-id="c2981-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmUSBDeviceClass \_ VendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="c2981-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmUSBDeviceClass\_VendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="c2981-147">廠商特定的裝置。</span><span class="sxs-lookup"><span data-stu-id="c2981-147">Vendor-specific device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2981-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2981-148">Requirements</span></span>



| <span data-ttu-id="c2981-149">需求</span><span class="sxs-lookup"><span data-stu-id="c2981-149">Requirement</span></span> | <span data-ttu-id="c2981-150">值</span><span class="sxs-lookup"><span data-stu-id="c2981-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2981-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2981-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c2981-152">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2981-152">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2981-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2981-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c2981-154">都不支援</span><span class="sxs-lookup"><span data-stu-id="c2981-154">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c2981-155">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c2981-155">End of client support</span></span><br/>    | <span data-ttu-id="c2981-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2981-156">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c2981-157">產品</span><span class="sxs-lookup"><span data-stu-id="c2981-157">Product</span></span><br/>                  | <span data-ttu-id="c2981-158">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c2981-158">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c2981-159">標頭</span><span class="sxs-lookup"><span data-stu-id="c2981-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2981-160"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2981-160"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2981-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2981-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2981-162">**IVMUSBDevice：:D eviceClass**</span><span class="sxs-lookup"><span data-stu-id="c2981-162">**IVMUSBDevice::DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)
</dt> </dl>

 

