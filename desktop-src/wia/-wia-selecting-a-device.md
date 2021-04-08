---
description: 當應用程式連線到 Windows 映像取得 (WIA) 硬體裝置時，WIA 會建立專案樹狀結構 (IWiaItem 或 IWiaItem2 介面的階層式樹狀結構，) 代表裝置及其影像、資料夾和掃描張床。
ms.assetid: 2a7bcfd4-4075-48a4-9eff-5210b9a635e3
title: '選取裝置 (WIA) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a2eab41016397f6505e60efcbf78d1fdf82499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848067"
---
# <a name="selecting-a-device-wia"></a><span data-ttu-id="d47f6-103">選取裝置 (WIA) </span><span class="sxs-lookup"><span data-stu-id="d47f6-103">Selecting a Device (WIA)</span></span>

<span data-ttu-id="d47f6-104">當應用程式連線到 Windows 映像取得 (WIA) 硬體裝置時，WIA 會建立專案樹狀結構 ([**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 或 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的階層式樹狀結構，) 代表裝置及其影像、資料夾和掃描張床。</span><span class="sxs-lookup"><span data-stu-id="d47f6-104">When an application connects to a Windows Image Acquisition (WIA) hardware device, WIA creates an item tree (a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interfaces) that represents the device and its images, folders, and scanning beds.</span></span> <span data-ttu-id="d47f6-105">應用程式可以在沒有使用者輸入的情況下，選取並聯機到裝置，或顯示可讓使用者選取裝置的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d47f6-105">An application can select and connect to a device without user input, or it can display a dialog box that allows a user to select a device.</span></span>

-   [<span data-ttu-id="d47f6-106">在不使用 UI 的情況下選取裝置</span><span class="sxs-lookup"><span data-stu-id="d47f6-106">Selecting a Device Without the UI</span></span>](#selecting-a-device-without-the-ui)
-   [<span data-ttu-id="d47f6-107">使用 UI 選取裝置</span><span class="sxs-lookup"><span data-stu-id="d47f6-107">Selecting a Device With the UI</span></span>](#selecting-a-device-with-the-ui)

## <a name="selecting-a-device-without-the-ui"></a><span data-ttu-id="d47f6-108">在不使用 UI 的情況下選取裝置</span><span class="sxs-lookup"><span data-stu-id="d47f6-108">Selecting a Device Without the UI</span></span>

<span data-ttu-id="d47f6-109">請執行下列步驟來選取並連接至 WIA 硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="d47f6-109">Perform the following steps to select and connect to a WIA hardware device.</span></span>

-   <span data-ttu-id="d47f6-110">呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以取出 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) 或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d47f6-110">Call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to retrieve a pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface.</span></span>
-   <span data-ttu-id="d47f6-111">使用 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)介面的 [**IWiaDevMgr：： EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo)方法，取得 [**IEnumWIA \_ 開發人員 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d47f6-111">Use the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) method of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface to obtain a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span> <span data-ttu-id="d47f6-112">如需有關如何列舉裝置的指示，請參閱 [列舉系統裝置](-wia-enumerating-system-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="d47f6-112">For instructions on how to enumerate devices, see [Enumerating System Devices](-wia-enumerating-system-devices.md).</span></span>
-   <span data-ttu-id="d47f6-113">使用 [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) 介面，為每個已列舉的 WIA 裝置取得 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="d47f6-113">Use [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface to obtain [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface pointers for each WIA device enumerated.</span></span>
-   <span data-ttu-id="d47f6-114">使用 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面檢查每個裝置的裝置資訊屬性，並 \_ \_ 從所需的裝置儲存 WIA DIP 開發 \_ 識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="d47f6-114">Use [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface to inspect the device information properties of each device and save the WIA\_DIP\_DEV\_ID property from the desired device.</span></span>
-   <span data-ttu-id="d47f6-115">在 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)介面中使用 DeviceID 屬性搭配 [**IWiaDevMgr：： CREATEDEVICE**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice)方法，以建立 WIA 裝置物件。</span><span class="sxs-lookup"><span data-stu-id="d47f6-115">Use the DeviceID property with the [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) method in the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface to create a WIA device object.</span></span> <span data-ttu-id="d47f6-116">**IWiaDevMgr：： CreateDevice** 方法會為應用程式提供指定裝置之根項目的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)或 [**IWiaItem2**](-wia-iwiaitem2.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="d47f6-116">The **IWiaDevMgr::CreateDevice** method provides the application with the pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item of the specified device.</span></span>

<span data-ttu-id="d47f6-117">如需如何在應用程式中進行這項操作的範例，請參閱本指南的教學課程一節中的 [建立裝置](-wia-creating-a-device.md) 。</span><span class="sxs-lookup"><span data-stu-id="d47f6-117">For an example of how to do this in an application, see [Creating a Device](-wia-creating-a-device.md) in the tutorial section of this guide.</span></span>

## <a name="selecting-a-device-with-the-ui"></a><span data-ttu-id="d47f6-118">使用 UI 選取裝置</span><span class="sxs-lookup"><span data-stu-id="d47f6-118">Selecting a Device With the UI</span></span>

<span data-ttu-id="d47f6-119">在抓取 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)的指標之後，應用程式可以藉由略過上述步驟的其餘步驟並呼叫 [**IWiaDevMgr：： SelectDeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg)，讓使用者選取裝置。</span><span class="sxs-lookup"><span data-stu-id="d47f6-119">After retrieving a pointer to [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr), an application can allow a user to select a device by skipping the rest of the above steps and calling [**IWiaDevMgr::SelectDeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg).</span></span> <span data-ttu-id="d47f6-120">**IWiaDevMgr：： SelectDeviceDlg** 會顯示對話方塊，讓使用者可以在其中選取 WIA 裝置。</span><span class="sxs-lookup"><span data-stu-id="d47f6-120">The **IWiaDevMgr::SelectDeviceDlg** displays a dialog box in which the user can select a WIA device.</span></span>

<span data-ttu-id="d47f6-121">建議應用程式 **在 [檔案**] 功能表上，透過 [掃描器]**中** 名稱為的功能表項目，讓裝置和影像可供選擇。</span><span class="sxs-lookup"><span data-stu-id="d47f6-121">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

 
