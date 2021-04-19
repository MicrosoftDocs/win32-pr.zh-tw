---
description: USB 裝置的管理特性。
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: 'CIM_USBDevice 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.USBVersion
- CIM_USBDevice.ClassCode
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.USBVersionInBCD
- CIM_USBDevice.MaxPacketSize
- CIM_USBDevice.VendorID
- CIM_USBDevice.ProductID
- CIM_USBDevice.DeviceReleaseNumber
- CIM_USBDevice.Manufacturer
- CIM_USBDevice.Product
- CIM_USBDevice.SerialNumber
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CommandTimeout
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4b43c57d69f0f9eb92293aa8fa1ff1aa1ebe96c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989341"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="599ca-103">CIM_USBDevice 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="599ca-103">CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="599ca-104">USB 裝置的管理特性。</span><span class="sxs-lookup"><span data-stu-id="599ca-104">The management characteristics of a USB device.</span></span>

## <a name="syntax"></a><span data-ttu-id="599ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="599ca-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::USB")]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   USBVersion;
  uint8    ClassCode;
  uint8    SubclassCode;
  uint8    ProtocolCode;
  uint16   USBVersionInBCD;
  uint8    MaxPacketSize;
  uint16   VendorID;
  uint16   ProductID;
  uint16   DeviceReleaseNumber;
  string   Manufacturer;
  string   Product;
  string   SerialNumber;
  uint8    NumberOfConfigs;
  uint8    CurrentConfigValue;
  uint8    CurrentAlternateSettings[];
  datetime CommandTimeout;
};
```

## <a name="members"></a><span data-ttu-id="599ca-106">成員</span><span class="sxs-lookup"><span data-stu-id="599ca-106">Members</span></span>

<span data-ttu-id="599ca-107">**CIM \_ USBDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="599ca-107">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="599ca-108">方法</span><span class="sxs-lookup"><span data-stu-id="599ca-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="599ca-109">屬性</span><span class="sxs-lookup"><span data-stu-id="599ca-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="599ca-110">方法</span><span class="sxs-lookup"><span data-stu-id="599ca-110">Methods</span></span>

<span data-ttu-id="599ca-111">**CIM \_ USBDevice** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="599ca-111">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="599ca-112">方法</span><span class="sxs-lookup"><span data-stu-id="599ca-112">Method</span></span>                                               | <span data-ttu-id="599ca-113">描述</span><span class="sxs-lookup"><span data-stu-id="599ca-113">Description</span></span>                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [<span data-ttu-id="599ca-114">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="599ca-114">**GetDescriptor**</span></span>](cim-usbdevice-getdescriptor.md) | <span data-ttu-id="599ca-115">抓取 USB 裝置描述項。</span><span class="sxs-lookup"><span data-stu-id="599ca-115">Retrieves a USB device descriptor.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="599ca-116">屬性</span><span class="sxs-lookup"><span data-stu-id="599ca-116">Properties</span></span>

<span data-ttu-id="599ca-117">**CIM \_ USBDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="599ca-117">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="599ca-118">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="599ca-118">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-119">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="599ca-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-121">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bDeviceClass」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceClass")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-122">USB 類別程式碼。</span><span class="sxs-lookup"><span data-stu-id="599ca-122">The USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-123">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="599ca-123">**CommandTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-124">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="599ca-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="599ca-126">可由支援 USB 重新導向的管理應用程式設定的逾時間隔。</span><span class="sxs-lookup"><span data-stu-id="599ca-126">A timeout interval that is configurable by management applications that support USB redirection.</span></span> <span data-ttu-id="599ca-127">當重新導向服務將 USB 裝置命令重新導向至遠端裝置，而且遠端裝置未在逾時間隔之前回應時，重新導向服務將會模擬 media 退出事件。</span><span class="sxs-lookup"><span data-stu-id="599ca-127">When the redirection service redirects a USB device command to a remote device, and the remote device does not respond before timeout interval, the redirection service will emulate a media eject event.</span></span> <span data-ttu-id="599ca-128">此外，服務可能會重新嘗試命令，或嘗試重新建立與遠端裝置的連線。</span><span class="sxs-lookup"><span data-stu-id="599ca-128">In addition, the service may re-try the command or try to re-establish the connection to the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-129">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="599ca-129">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-130">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="599ca-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="599ca-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-132">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ USBDevice**.**CurrentConfigValue**") </span><span class="sxs-lookup"><span data-stu-id="599ca-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-133">陣列，其中包含裝置目前設定中每個介面的替代設定。</span><span class="sxs-lookup"><span data-stu-id="599ca-133">An array that contains the alternate settings for each interface in the current configuration of the device.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-134">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="599ca-134">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-135">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="599ca-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-137">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ USBDevice**.**CurrentAlternateSettings**") </span><span class="sxs-lookup"><span data-stu-id="599ca-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-138">目前為裝置選取的設定。</span><span class="sxs-lookup"><span data-stu-id="599ca-138">The configuration currently selected for the device.</span></span> <span data-ttu-id="599ca-139">如果此值為零，則不會設定裝置。</span><span class="sxs-lookup"><span data-stu-id="599ca-139">If this value is zero, the Device is not configured.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-140">**DeviceReleaseNumber**</span><span class="sxs-lookup"><span data-stu-id="599ca-140">**DeviceReleaseNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-141">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="599ca-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-143">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bcdDevice」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdDevice")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-144">BCD 格式的裝置版本號碼。</span><span class="sxs-lookup"><span data-stu-id="599ca-144">The device release number in BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-145">**製造商**</span><span class="sxs-lookup"><span data-stu-id="599ca-145">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="599ca-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| iManufacturer」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iManufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-149">裝置的製造商字串。</span><span class="sxs-lookup"><span data-stu-id="599ca-149">The manufacturer string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-150">**MaxPacketSize**</span><span class="sxs-lookup"><span data-stu-id="599ca-150">**MaxPacketSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-151">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="599ca-151">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-153">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bMaxPacketSize」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bMaxPacketSize")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-154">USB 零端點的封包大小上限。</span><span class="sxs-lookup"><span data-stu-id="599ca-154">The maximum packet size for the USB zero endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-155">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="599ca-155">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-156">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="599ca-156">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-158">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bNumConfigurations」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bNumConfigurations")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-159">為裝置定義的裝置設定數目。</span><span class="sxs-lookup"><span data-stu-id="599ca-159">The number of device configurations that are defined for the Device.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-160">**產品**</span><span class="sxs-lookup"><span data-stu-id="599ca-160">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="599ca-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-163">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| iProduct」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iProduct")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-164">裝置的產品字串。</span><span class="sxs-lookup"><span data-stu-id="599ca-164">The product string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-165">**產品**</span><span class="sxs-lookup"><span data-stu-id="599ca-165">**ProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-166">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="599ca-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-168">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| idProduct」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idProduct")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-169">依製造商指派給裝置的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="599ca-169">The product ID assigned to the device by manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-170">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="599ca-170">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-171">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="599ca-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-173">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bDeviceProtocol」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-174">USB 通訊協定代碼。</span><span class="sxs-lookup"><span data-stu-id="599ca-174">The USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-175">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="599ca-175">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="599ca-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-178">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| iSerialNumber」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iSerialNumber")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-179">裝置的序號。</span><span class="sxs-lookup"><span data-stu-id="599ca-179">The serial number of the device.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-180">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="599ca-180">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-181">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="599ca-181">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-183">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bDeviceSubClass」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceSubClass")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-184">USB 子類別程式碼。</span><span class="sxs-lookup"><span data-stu-id="599ca-184">The USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-185">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="599ca-185">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-186">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="599ca-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="599ca-188">USB 裝置支援的最新 USB 版本。</span><span class="sxs-lookup"><span data-stu-id="599ca-188">The latest USB Version supported by the USB Device.</span></span> <span data-ttu-id="599ca-189">屬性會以二進位編碼的 decimal (BCD) ，其中包含第二和第3位數之間的小數點。</span><span class="sxs-lookup"><span data-stu-id="599ca-189">The property is expressed as a binary-coded decimal (BCD) that contains a decimal point between the 2nd and 3rd digits.</span></span> <span data-ttu-id="599ca-190">例如，0x201 的值表示支援2.01 版。</span><span class="sxs-lookup"><span data-stu-id="599ca-190">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-191">**USBVersionInBCD**</span><span class="sxs-lookup"><span data-stu-id="599ca-191">**USBVersionInBCD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-192">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="599ca-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-194">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bcdUSB」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdUSB")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-195">裝置符合的 USB 規格編號。</span><span class="sxs-lookup"><span data-stu-id="599ca-195">The USB specification number that the device complies with.</span></span> <span data-ttu-id="599ca-196">此屬性的格式為 BCD 格式。</span><span class="sxs-lookup"><span data-stu-id="599ca-196">This property is formatted with BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="599ca-197">**VendorID**</span><span class="sxs-lookup"><span data-stu-id="599ca-197">**VendorID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599ca-198">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="599ca-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="599ca-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599ca-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599ca-200">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| idVendor」 ) </span><span class="sxs-lookup"><span data-stu-id="599ca-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idVendor")</span></span>
</dt> </dl>

<span data-ttu-id="599ca-201">依 USB.org 指派給裝置的廠商識別碼。</span><span class="sxs-lookup"><span data-stu-id="599ca-201">The vendor ID assigned to the device by USB.org.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="599ca-202">規格需求</span><span class="sxs-lookup"><span data-stu-id="599ca-202">Requirements</span></span>



| <span data-ttu-id="599ca-203">需求</span><span class="sxs-lookup"><span data-stu-id="599ca-203">Requirement</span></span> | <span data-ttu-id="599ca-204">值</span><span class="sxs-lookup"><span data-stu-id="599ca-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="599ca-205">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="599ca-205">Minimum supported client</span></span><br/> | <span data-ttu-id="599ca-206">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="599ca-206">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="599ca-207">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="599ca-207">Minimum supported server</span></span><br/> | <span data-ttu-id="599ca-208">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="599ca-208">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="599ca-209">命名空間</span><span class="sxs-lookup"><span data-stu-id="599ca-209">Namespace</span></span><br/>                | <span data-ttu-id="599ca-210">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="599ca-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="599ca-211">MOF</span><span class="sxs-lookup"><span data-stu-id="599ca-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="599ca-212"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="599ca-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="599ca-213">DLL</span><span class="sxs-lookup"><span data-stu-id="599ca-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="599ca-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="599ca-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="599ca-215">另請參閱</span><span class="sxs-lookup"><span data-stu-id="599ca-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599ca-216">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="599ca-216">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

