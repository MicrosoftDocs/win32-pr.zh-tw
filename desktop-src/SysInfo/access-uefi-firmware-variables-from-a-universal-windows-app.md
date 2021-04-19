---
description: 如何從通用 Windows 應用程式存取統一的可延伸韌體介面 (UEFI) 固件變數。
ms.assetid: 4131CCED-3B76-4569-B0A7-111E4E9215EF
title: 從通用 Windows 應用程式存取 UEFI 固件變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738b7042b4c650c74115760e6dcd2e93131d6780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980312"
---
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a><span data-ttu-id="d6a50-103">從通用 Windows 應用程式存取 UEFI 固件變數</span><span class="sxs-lookup"><span data-stu-id="d6a50-103">Access UEFI firmware variables from a Universal Windows App</span></span>

<span data-ttu-id="d6a50-104">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="d6a50-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d6a50-105">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="d6a50-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d6a50-106">如何從通用 Windows 應用程式存取統一的可延伸韌體介面 (UEFI) 固件變數。</span><span class="sxs-lookup"><span data-stu-id="d6a50-106">How to access Unified Extensible Firmware Interface (UEFI) firmware variables from a Universal Windows app.</span></span>

<span data-ttu-id="d6a50-107">從 Windows 10 開始，1803版的通用 Windows 應用程式可以使用 [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) 和 [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (及其 ' ex ' 變體，) 藉由執行下列動作來存取 UEFI 固件變數：</span><span class="sxs-lookup"><span data-stu-id="d6a50-107">Starting with Windows 10, version 1803, Universal Windows apps can use [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) and [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (and their 'ex' variants) to access UEFI firmware variables by doing the following:</span></span>

-   <span data-ttu-id="d6a50-108">在資訊清單中宣告 **firmwareRead \_ cw5n1h2txyewy** 自訂功能，以讀取固件變數和/或 **firmwareWrite \_ cw5n1h2txyewy** 功能來寫入固件變數。</span><span class="sxs-lookup"><span data-stu-id="d6a50-108">Declare the **Microsoft.firmwareRead\_cw5n1h2txyewy** custom capability in the manifest to read a firmware variable, and/or the **Microsoft.firmwareWrite\_cw5n1h2txyewy** capability to write a firmware variable.</span></span>
-   <span data-ttu-id="d6a50-109">也會在應用程式資訊清單中宣告 **protectedApp** 限制的功能。</span><span class="sxs-lookup"><span data-stu-id="d6a50-109">Also declare the **protectedApp** restricted capability in the app manifest.</span></span>
-   <span data-ttu-id="d6a50-110">例如，下列應用程式資訊清單新增可讓通用 Windows 應用程式讀取固件變數：</span><span class="sxs-lookup"><span data-stu-id="d6a50-110">For example, the following app manifest additions allow the Universal Windows app to read firmware variables:</span></span>

    ``` syntax
    <Package
      ...
      xmlns:uap4=http://schemas.microsoft.com/appx/manifest/uap/windows10/4
      xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
      IgnorableNamespaces="uap mp uap4 rescap">  
      ...
      <Capabilities>
        <rescap:Capability Name="protectedApp"/>
        <uap4:CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy" />
      </Capabilities>
    </Package>
    ```

<!-- -->

-   <span data-ttu-id="d6a50-111">在將應用程式提交給 Microsoft Store 之前，請先設定所有專案設定的連結器選項 **/INTEGRITYCHECK**。</span><span class="sxs-lookup"><span data-stu-id="d6a50-111">Set the linker option **/INTEGRITYCHECK**, for all project configurations, before submitting the app to the Microsoft Store.</span></span> <span data-ttu-id="d6a50-112">這可確保應用程式將以受保護的應用程式啟動。</span><span class="sxs-lookup"><span data-stu-id="d6a50-112">This ensures that the app will be launched as a protected app.</span></span> <span data-ttu-id="d6a50-113">如需詳細資料，請參閱 [/INTEGRITYCHECK (需要簽章檢查) ](/cpp/build/reference/integritycheck-require-signature-check) 。</span><span class="sxs-lookup"><span data-stu-id="d6a50-113">See [/INTEGRITYCHECK (Require Signature Check)](/cpp/build/reference/integritycheck-require-signature-check) for details.</span></span>
-   <span data-ttu-id="d6a50-114">從 Microsoft (SCCD) 檔案取得 [已簽署的自訂功能描述](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) 項。</span><span class="sxs-lookup"><span data-stu-id="d6a50-114">Obtain a [Signed Custom Capability Descriptor](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) file from Microsoft.</span></span> <span data-ttu-id="d6a50-115">請參閱 [建立自訂功能以將驅動程式與硬體支援應用程式配對 (HSA) ](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) 和 [使用自訂功能將硬體支援應用程式與硬體支援應用程式配對 (HSA) 與驅動程式](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) ，以取得如何從 MICROSOFT 取得簽署的 SCCD 檔、如何將它封裝到您的應用程式，以及如何啟用開發人員模式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d6a50-115">See [Creating a custom capability to pair a driver with a Hardware Support App (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) and [Using a custom capability to pair a Hardware Support App (HSA) with a driver](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) for information about how to obtain signed SCCD file from Microsoft, how to package it with your app, and how to enable developer mode.</span></span> <span data-ttu-id="d6a50-116">以下是 [CustomCapability 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability)中的範例 SSCD 檔案：</span><span class="sxs-lookup"><span data-stu-id="d6a50-116">Here is an example SSCD file from the [CustomCapability sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span></span>
    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <CustomCapabilityDescriptor xmlns="http://schemas.microsoft.com/appx/2016/sccd" xmlns:s="http://schemas.microsoft.com/appx/2016/sccd">
      <CustomCapabilities>
        <CustomCapability Name="microsoft.hsaTestCustomCapability_q536wpkpf5cy2"></CustomCapability>
        <CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy"></CustomCapability>
      </CustomCapabilities>
      <AuthorizedEntities>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="ca9fc964db7e0c2938778f4559946833e7a8cfde0f3eaa07650766d4764e86c4"></AuthorizedEntity>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="279cd652c4e252bfbe5217ac722205d7729ba409148cfa9e6d9e5b1cb94eaff1"></AuthorizedEntity>
      </AuthorizedEntities>
      <Catalog>xxxx</Catalog>
    </CustomCapabilityDescriptor>
    ```

    

-   <span data-ttu-id="d6a50-117">將應用程式提交給 Microsoft Store，以將其簽署。</span><span class="sxs-lookup"><span data-stu-id="d6a50-117">Submit the app to the Microsoft Store to get it signed.</span></span> <span data-ttu-id="d6a50-118">針對開發用途，您可以在開機設定資料庫中啟用測試簽署， (bcd) 來略過簽署。</span><span class="sxs-lookup"><span data-stu-id="d6a50-118">For development purposes, you can skip signing by enabling test-signing in the boot configuration database (bcd).</span></span> <span data-ttu-id="d6a50-119">如需詳細資訊，請參閱 [TESTSIGNING Boot Configuration 選項](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) 。</span><span class="sxs-lookup"><span data-stu-id="d6a50-119">See [The TESTSIGNING Boot Configuration Option](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) for details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6a50-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6a50-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6a50-121">特殊和受限制的功能</span><span class="sxs-lookup"><span data-stu-id="d6a50-121">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="d6a50-122">**GetFirmwareEnvironmentVariable**</span><span class="sxs-lookup"><span data-stu-id="d6a50-122">**GetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="d6a50-123">**GetFirmwareEnvironmentVariableEx**</span><span class="sxs-lookup"><span data-stu-id="d6a50-123">**GetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="d6a50-124">**SetFirmwareEnvironmentVariable**</span><span class="sxs-lookup"><span data-stu-id="d6a50-124">**SetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="d6a50-125">**SetFirmwareEnvironmentVariableEx**</span><span class="sxs-lookup"><span data-stu-id="d6a50-125">**SetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="d6a50-126">從通用 Windows 應用程式存取 SMBIOS 資訊</span><span class="sxs-lookup"><span data-stu-id="d6a50-126">Access SMBIOS information from a Universal Windows App</span></span>](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
