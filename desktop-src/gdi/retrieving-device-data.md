---
description: 應用程式可以使用下列函式，使用裝置內容來抓取裝置資料： GetDeviceCaps 和 DeviceCapabilities。
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: 正在抓取裝置資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fa4054170f9b66d73e3494928db312eb8aa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972525"
---
# <a name="retrieving-device-data"></a><span data-ttu-id="2ca3c-103">正在抓取裝置資料</span><span class="sxs-lookup"><span data-stu-id="2ca3c-103">Retrieving Device Data</span></span>

<span data-ttu-id="2ca3c-104">應用程式可以使用下列函式，使用裝置內容來抓取裝置資料： [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 和 [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)。</span><span class="sxs-lookup"><span data-stu-id="2ca3c-104">Applications can use the following functions to retrieve device data using a device context: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) and [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).</span></span>

<span data-ttu-id="2ca3c-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 會抓取下列裝置的一般裝置資料：</span><span class="sxs-lookup"><span data-stu-id="2ca3c-105">[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) retrieves general device data for the following devices:</span></span>

-   <span data-ttu-id="2ca3c-106">點陣顯示</span><span class="sxs-lookup"><span data-stu-id="2ca3c-106">Raster displays</span></span>
-   <span data-ttu-id="2ca3c-107">點矩陣印表機</span><span class="sxs-lookup"><span data-stu-id="2ca3c-107">Dot-matrix printers</span></span>
-   <span data-ttu-id="2ca3c-108">噴墨印表機</span><span class="sxs-lookup"><span data-stu-id="2ca3c-108">Ink-jet printers</span></span>
-   <span data-ttu-id="2ca3c-109">雷射印表機</span><span class="sxs-lookup"><span data-stu-id="2ca3c-109">Laser printers</span></span>
-   <span data-ttu-id="2ca3c-110">向量繪圖器</span><span class="sxs-lookup"><span data-stu-id="2ca3c-110">Vector plotters</span></span>
-   <span data-ttu-id="2ca3c-111">點陣攝影機</span><span class="sxs-lookup"><span data-stu-id="2ca3c-111">Raster cameras</span></span>

<span data-ttu-id="2ca3c-112">這些資料包含裝置支援的功能，包括影片顯示) 的裝置解析度 (、影片) 顯示的色彩格式 (、繪圖物件數目、光柵功能、曲線繪圖、線條繪製、多邊形繪圖和文字繪製。</span><span class="sxs-lookup"><span data-stu-id="2ca3c-112">The data includes the supported capabilities of the device, including device resolution (for video displays), color format (for video displays and color printers), number of graphic objects, raster capabilities, curve drawing, line drawing, polygon drawing, and text drawing.</span></span> <span data-ttu-id="2ca3c-113">應用程式會藉由提供識別適當之裝置內容的控制碼，以及指定函式要抓取之資料類型的索引，來抓取這項資料。</span><span class="sxs-lookup"><span data-stu-id="2ca3c-113">An application retrieves this data by supplying a handle identifying the appropriate device context, as well as an index specifying the type of data the function is to retrieve.</span></span>

<span data-ttu-id="2ca3c-114">[**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)函式會抓取印表機專屬的資料，包括可用的紙張數量、印表機的雙工功能、印表機支援的解析度、最大和最小支援的紙張大小等等。</span><span class="sxs-lookup"><span data-stu-id="2ca3c-114">The [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) function retrieves data specific to printers, including the number of available paper bins, the duplex capabilities of the printer, the resolutions supported by the printer, the maximum and minimum supported paper size, and so on.</span></span> <span data-ttu-id="2ca3c-115">應用程式會藉由提供指定印表機裝置和埠的字串，以及指定函式要抓取之資料類型的索引，來抓取這項資料。</span><span class="sxs-lookup"><span data-stu-id="2ca3c-115">An application retrieves this data by supplying strings specifying a printer device and port, as well as an index specifying the type of data that the function is to retrieve.</span></span>

 

 
