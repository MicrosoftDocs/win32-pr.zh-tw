---
title: 將裝置介面註冊為受特殊許可權的應用程式限制
description: 本主題說明如何新增受限制的屬性，指出只有特殊許可權的應用程式可以存取裝置介面類別別。
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: e23f8b7f2cc1884e2f878739f56507e79eb1bb69
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024290"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a><span data-ttu-id="36602-103">將裝置介面註冊為受特殊許可權的應用程式限制</span><span class="sxs-lookup"><span data-stu-id="36602-103">Register the device interface as restricted to privileged apps</span></span>

<span data-ttu-id="36602-104">除非應用程式被簽署的裝置中繼資料授與許可權，否則會拒絕應用程式存取自訂驅動程式功能。</span><span class="sxs-lookup"><span data-stu-id="36602-104">Applications are denied access to custom driver functionality, unless they're granted permissions through signed device metadata.</span></span> <span data-ttu-id="36602-105">本主題說明如何新增 **受限制** 的屬性，指出只有特殊許可權的應用程式可以存取裝置介面類別別。</span><span class="sxs-lookup"><span data-stu-id="36602-105">This topic shows how to add the **Restricted** property that indicates that only privileged apps can access a device interface class.</span></span> <span data-ttu-id="36602-106">自訂設備磁碟機必須有這個屬性。</span><span class="sxs-lookup"><span data-stu-id="36602-106">Custom device drivers must have this property.</span></span>

## <a name="instructions"></a><span data-ttu-id="36602-107">指示</span><span class="sxs-lookup"><span data-stu-id="36602-107">Instructions</span></span>

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a><span data-ttu-id="36602-108">在資訊 (INF) 檔中設定受限制的屬性</span><span class="sxs-lookup"><span data-stu-id="36602-108">Setting the Restricted property in an information (INF) file</span></span>

<span data-ttu-id="36602-109">在 `InterfaceInstall32` 區段中，會註冊裝置介面類別別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="36602-109">In the `InterfaceInstall32` section, the GUID of the device interface class is registered.</span></span>

<span data-ttu-id="36602-110">**AddProperty** 指示詞底下的行會設定裝置類別屬性。</span><span class="sxs-lookup"><span data-stu-id="36602-110">The lines under the **AddProperty** directive set the device class properties.</span></span> <span data-ttu-id="36602-111">第二行則是在自訂屬性分類中設定自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="36602-111">The second line sets a custom property in a custom property category.</span></span> <span data-ttu-id="36602-112">屬性類別 GUID 是 **14c83a99-0b3f-44b7-be4c-a178d3990564**，而屬性識別碼是 **2**。</span><span class="sxs-lookup"><span data-stu-id="36602-112">The property-category GUID is **14c83a99-0b3f-44b7-be4c-a178d3990564**, and the property identifier is **2**.</span></span> <span data-ttu-id="36602-113">選擇性的 `Flags` 專案值不存在，且類型為 **17** (**DEVPROP_TYPE_BOOLEAN**) 。</span><span class="sxs-lookup"><span data-stu-id="36602-113">The optional `Flags` entry value is not present, and the type is **17** (**DEVPROP_TYPE_BOOLEAN**).</span></span> <span data-ttu-id="36602-114">屬性的值為 **1**。</span><span class="sxs-lookup"><span data-stu-id="36602-114">The value of the property is **1**.</span></span>

```Text
; Below, {11111111-0000-1111-0000-111111111111} is the GUID of the
; new device interface class in an AddInterface directive



; -- Interface installation
[InterfaceInstall32]
{11111111-0000-1111-0000-111111111111}=NewInterfaceInstall

[NewInterfaceInstall]
AddProperty=PrivilegedProperties

[PrivilegedProperties]
; DEVPKey_DeviceInterfaceClass_Restricted
{14c83a99-0b3f-44b7-be4c-a178d3990564}, 2, 17,,1 ; -- non-zero indicates privileged
```

## <a name="remarks"></a><span data-ttu-id="36602-115">備註</span><span class="sxs-lookup"><span data-stu-id="36602-115">Remarks</span></span>

<span data-ttu-id="36602-116">驅動程式也可以呼叫 [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata)常式來註冊裝置介面類別別，而不是 **AddInterface** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="36602-116">Instead of the **AddInterface** directive, the driver can also call the [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine to register the device interface class.</span></span>

<span data-ttu-id="36602-117">您也可以藉由呼叫 [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) 常式來設定受限制的介面屬性。</span><span class="sxs-lookup"><span data-stu-id="36602-117">You can also set the restricted interface property by calling the [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36602-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="36602-118">Related topics</span></span>

<span data-ttu-id="36602-119">[自訂驅動程式存取範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)、 [適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)、 [硬體開發人員中心](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="36602-119">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
