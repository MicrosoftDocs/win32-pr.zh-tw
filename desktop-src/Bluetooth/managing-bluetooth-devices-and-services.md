---
title: 管理藍牙裝置和服務
description: 有兩種主要的藍牙程式設計方法，可讓您使用 Windows 通訊端介面進行 Windows 程式設計，以及直接使用 nonsocket 藍牙介面管理裝置。
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- 管理藍牙裝置和服務
- 藍牙裝置和服務，管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3657dff2091eda4b26d14f6504b74f943983
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092760"
---
# <a name="managing-bluetooth-devices-and-services"></a>管理藍牙裝置和服務

本節說明如何使用藍牙 API 來直接控制藍牙裝置和服務。

如需有關使用 Windows 通訊端介面在 Windows 上設計藍牙程式的詳細資訊，請參閱 [適用于藍牙的 Windows 通訊端支援](windows-sockets-support-for-bluetooth.md)。

> [!Note]  
> 藍牙無法防止電源管理功能中斷藍牙傳輸。 啟用 Bluetooth 的應用程式可以監視電源訊息，以防止這類中斷。 如需詳細資訊，請參閱 [使用電源管理](/windows/desktop/Power/using-power-management)。

 

此章節包含下列主題。

| 區段                                                                               | Content                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [選取藍牙裝置](selecting-a-bluetooth-device.md)                      | 說明如何選取藍牙裝置。                                   |
| [藍牙和 WM \_ DEVICECHANGE 訊息](bluetooth-and-wm-devicechange-messages.md) | 說明藍牙與 **WM \_ DEVICECHANGE** 訊息之間的互動。 |



 

 

 