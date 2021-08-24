---
title: COM 介面-裝置存取
description: 元件物件模型 (裝置存取 API 中的 COM) 介面。
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 22447151b944a2ac5515222eebd528fed11e2479d8a8c4db59e2da46dd07a130
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793379"
---
# <a name="com-interfaces---device-access"></a>COM 介面-裝置存取

元件物件模型 (裝置存取 API 中的 COM) 介面。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|---|---|
| [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)介面會從對 CreateDeviceAccessInstance 的呼叫傳回。 它可讓呼叫端控制系結至裝置實例的作業，以抓取可用於與該裝置互動的另一個介面。<br/> |
| [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | 將控制程式代碼傳送至設備磁碟機。此動作會導致裝置執行對應的操作。 <br/> |
| [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | 提供方法來處理 [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)方法的呼叫完成。<br/> |

## <a name="related-topics"></a>相關主題

[自訂驅動程式存取範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)、[適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)、[硬體開發人員中心](/windows-hardware/drivers/)
