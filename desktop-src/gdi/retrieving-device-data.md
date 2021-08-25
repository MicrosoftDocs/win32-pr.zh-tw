---
description: 應用程式可以使用下列函式，使用裝置內容來抓取裝置資料： GetDeviceCaps 和 DeviceCapabilities。
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: 正在抓取裝置資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf956a04c733883cb5fb374e4e75dc4e93e8029f9968deb90cc113cef460864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717988"
---
# <a name="retrieving-device-data"></a>正在抓取裝置資料

應用程式可以使用下列函式，使用裝置內容來抓取裝置資料： [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 和 [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)。

[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 會抓取下列裝置的一般裝置資料：

-   點陣顯示
-   點矩陣印表機
-   噴墨印表機
-   雷射印表機
-   向量繪圖器
-   點陣攝影機

這些資料包含裝置支援的功能，包括影片顯示) 的裝置解析度 (、影片) 顯示的色彩格式 (、繪圖物件數目、光柵功能、曲線繪圖、線條繪製、多邊形繪圖和文字繪製。 應用程式會藉由提供識別適當之裝置內容的控制碼，以及指定函式要抓取之資料類型的索引，來抓取這項資料。

[**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)函式會抓取印表機專屬的資料，包括可用的紙張數量、印表機的雙工功能、印表機支援的解析度、最大和最小支援的紙張大小等等。 應用程式會藉由提供指定印表機裝置和埠的字串，以及指定函式要抓取之資料類型的索引，來抓取這項資料。

 

 
