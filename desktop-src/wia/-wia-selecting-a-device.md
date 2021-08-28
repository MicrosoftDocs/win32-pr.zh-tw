---
description: 當應用程式連線至 Windows 映像取得 (WIA) 硬體裝置時，wia 會建立專案樹狀結構 (IWiaItem 或 IWiaItem2 介面的階層式樹狀結構，) 代表裝置及其影像、資料夾和掃描張床。
ms.assetid: 2a7bcfd4-4075-48a4-9eff-5210b9a635e3
title: '選取裝置 (WIA) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d068dc2501419b5748f199114fab15d72dc5fecc6c7e6881f63b8e47114b7d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813657"
---
# <a name="selecting-a-device-wia"></a>選取裝置 (WIA) 

當應用程式連線至 Windows 映像取得 (WIA) 硬體裝置時，wia 會建立專案樹狀結構 ([**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)或 [**IWiaItem2**](-wia-iwiaitem2.md)介面的階層式樹狀結構，) 代表裝置及其影像、資料夾和掃描張床。 應用程式可以在沒有使用者輸入的情況下，選取並聯機到裝置，或顯示可讓使用者選取裝置的對話方塊。

-   [在不使用 UI 的情況下選取裝置](#selecting-a-device-without-the-ui)
-   [使用 UI 選取裝置](#selecting-a-device-with-the-ui)

## <a name="selecting-a-device-without-the-ui"></a>在不使用 UI 的情況下選取裝置

請執行下列步驟來選取並連接至 WIA 硬體裝置。

-   呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以取出 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) 或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) 介面的指標。
-   使用 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)介面的 [**IWiaDevMgr：： EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo)方法，取得 [**IEnumWIA \_ 開發人員 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)介面的指標。 如需有關如何列舉裝置的指示，請參閱 [列舉系統裝置](-wia-enumerating-system-devices.md)。
-   使用 [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) 介面，為每個已列舉的 WIA 裝置取得 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面指標。
-   使用 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面檢查每個裝置的裝置資訊屬性，並 \_ \_ 從所需的裝置儲存 WIA DIP 開發 \_ 識別碼屬性。
-   在 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)介面中使用 DeviceID 屬性搭配 [**IWiaDevMgr：： CREATEDEVICE**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice)方法，以建立 WIA 裝置物件。 **IWiaDevMgr：： CreateDevice** 方法會為應用程式提供指定裝置之根項目的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)或 [**IWiaItem2**](-wia-iwiaitem2.md)介面指標。

如需如何在應用程式中進行這項操作的範例，請參閱本指南的教學課程一節中的 [建立裝置](-wia-creating-a-device.md) 。

## <a name="selecting-a-device-with-the-ui"></a>使用 UI 選取裝置

在抓取 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)的指標之後，應用程式可以藉由略過上述步驟的其餘步驟並呼叫 [**IWiaDevMgr：： SelectDeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-selectdevicedlg)，讓使用者選取裝置。 **IWiaDevMgr：： SelectDeviceDlg** 會顯示對話方塊，讓使用者可以在其中選取 WIA 裝置。

建議應用程式 **在 [檔案**] 功能表上，透過 [掃描器]**中** 名稱為的功能表項目，讓裝置和影像可供選擇。

 

 
