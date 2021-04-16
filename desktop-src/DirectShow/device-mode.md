---
description: 裝置模式
ms.assetid: d56021be-616b-41cd-8cf0-9e0d314f62cd
title: 裝置模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4657fbb49e2619d75911c18185109805116b9647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467937"
---
# <a name="device-mode"></a>裝置模式

IEEE 1394 和 USB 攝影機可以切換攝影機模式與視頻磁帶錄製器， (VTR) 模式。 當 IEEE 1394 攝影機切換模式時，裝置會重設，而應用程式必須再次列舉。 應用程式無法以程式設計方式切換模式。 另一方面，USB 攝影機可以在相機與 VTR 模式之間切換，而不需要重設，而且應用程式可以變更模式。

**MSDV 驅動程式**

若要取得 IEEE 1394 裝置上的目前模式，請使用值 ED DEVCAP 裝置類型來呼叫 [**IAMExtDevice：： GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) 方法 \_ \_ \_ 。 如果此方法傳回值 ED \_ DEVTYPE \_ VCR，則裝置會處於 VTR 模式，並具有像是 pause、stop、fast 向前和倒轉等的功能。 否則，如果方法傳回 ED \_ DEVTYPE \_ 攝影機，則裝置會處於相機模式。 下列程式碼範例顯示如何查詢裝置類型：


```C++
if (MyDevCap.bHasDevice) 
{
    LONG lDeviceType = 0;
    MyDevCap.pDevice->GetCapability(ED_DEVCAP_DEVICE_TYPE, &lDeviceType, 0);

    if (lDeviceType == ED_DEVTYPE_VCR) 
    {
        // Device is a VTR. Enable all VTR functions.
    }
    else 
    {
        // Device is a camera. 
        // Enable record and record-pause; disable other functions.
    }
}
```



如果攝影機離線，您應該在下一次變成可用時重新查詢。 當移除裝置時，篩選圖形管理員會張貼 [**EC \_ 裝置 \_ 遺失**](ec-device-lost.md) 事件。

**UVC 驅動程式**

由於 USB 影片裝置不需要重設就能切換模式，因此上述範例中所示的程式碼對 USB 裝置而言並不可靠。 請改用 [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) 介面取得目前的模式。 您也可以使用此介面，以程式設計方式切換模式（如果裝置支援的話）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制 DV 攝像機](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



