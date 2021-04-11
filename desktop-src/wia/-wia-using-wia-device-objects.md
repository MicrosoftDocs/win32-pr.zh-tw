---
description: 映射裝置會以 Windows 影像取得 (WIA) 作為 WIA 專案物件的階層式樹狀結構， (IWiaItem 介面) 。
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: 使用 WIA 裝置物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1af755b243d322feac746620cb9dd9bd9965d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113272"
---
# <a name="using-wia-device-objects"></a>使用 WIA 裝置物件

映射裝置會以 Windows 影像取得 (WIA) 作為 WIA 專案物件的階層式樹狀結構， ([**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 介面) 。 一般來說，這個專案樹狀結構的根目錄代表裝置本身，而樹狀結構上的其他專案則代表掃描器的影像、相機或掃描區域。

應用程式會使用 WIA 裝置管理員來建立和列舉 WIA 裝置。 下列各節說明如何建立和使用 WIA 裝置：

-   [選取裝置](-wia-selecting-a-device.md)
-   [WIA 攝影機裝置](-wia-wia-camera-devices.md)
-   [WIA 掃描器裝置](-wia-wia-scanner-devices.md)

 

 



