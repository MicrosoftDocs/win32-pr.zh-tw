---
description: IWindowsDriverUpdateEntry 介面會定義下列屬性。
ms.assetid: a0ff6ec2-13fe-4c0c-b375-9df55e1c1bb4
title: IWindowsDriverUpdateEntry 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae63775bd7b13c67b4ec96c70107069730f828d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113492"
---
# <a name="iwindowsdriverupdateentry-properties"></a><span data-ttu-id="c88c9-103">IWindowsDriverUpdateEntry 屬性</span><span class="sxs-lookup"><span data-stu-id="c88c9-103">IWindowsDriverUpdateEntry Properties</span></span>

<span data-ttu-id="c88c9-104">[**IWindowsDriverUpdateEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdateentry)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c88c9-104">The [**IWindowsDriverUpdateEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdateentry) interface defines the following properties.</span></span>



| <span data-ttu-id="c88c9-105">屬性</span><span class="sxs-lookup"><span data-stu-id="c88c9-105">Property</span></span>                                                                     | <span data-ttu-id="c88c9-106">描述</span><span class="sxs-lookup"><span data-stu-id="c88c9-106">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c88c9-107">**DeviceProblemNumber**</span><span class="sxs-lookup"><span data-stu-id="c88c9-107">**DeviceProblemNumber**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_deviceproblemnumber) | <span data-ttu-id="c88c9-108">取得符合 Windows 驅動程式更新之裝置的問題號碼。</span><span class="sxs-lookup"><span data-stu-id="c88c9-108">Gets the problem number of the device that matches for the Windows driver update.</span></span>                                    |
| [<span data-ttu-id="c88c9-109">**DeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="c88c9-109">**DeviceStatus**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_devicestatus)               | <span data-ttu-id="c88c9-110">取得符合 Windows 驅動程式更新的裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="c88c9-110">Gets the status of the device that matches for the Windows driver update.</span></span>                                            |
| [<span data-ttu-id="c88c9-111">**DriverClass**</span><span class="sxs-lookup"><span data-stu-id="c88c9-111">**DriverClass**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverclass)                 | <span data-ttu-id="c88c9-112">取得 Windows 驅動程式更新的類別。</span><span class="sxs-lookup"><span data-stu-id="c88c9-112">Gets the class of the Windows driver update.</span></span>                                                                         |
| [<span data-ttu-id="c88c9-113">**DriverHardwareID**</span><span class="sxs-lookup"><span data-stu-id="c88c9-113">**DriverHardwareID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverhardwareid)       | <span data-ttu-id="c88c9-114">取得 Windows 驅動程式更新必須符合才能安裝的硬體或相容識別碼。</span><span class="sxs-lookup"><span data-stu-id="c88c9-114">Gets the hardware or the compatible identifier that the Windows driver update must match in order to be installable.</span></span> |
| [<span data-ttu-id="c88c9-115">**DriverManufacturer**</span><span class="sxs-lookup"><span data-stu-id="c88c9-115">**DriverManufacturer**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_drivermanufacturer)   | <span data-ttu-id="c88c9-116">取得 Windows 驅動程式更新之製造商的語言不變名稱。</span><span class="sxs-lookup"><span data-stu-id="c88c9-116">Gets the language-invariant name of the manufacturer of the Windows driver update.</span></span>                                   |
| [<span data-ttu-id="c88c9-117">**DriverModel**</span><span class="sxs-lookup"><span data-stu-id="c88c9-117">**DriverModel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_drivermodel)                 | <span data-ttu-id="c88c9-118">取得適用于 Windows 驅動程式更新之裝置的語言不變模型名稱。</span><span class="sxs-lookup"><span data-stu-id="c88c9-118">Gets the language-invariant model name of the device for which the Windows driver update is intended.</span></span>                |
| [<span data-ttu-id="c88c9-119">**DriverProvider**</span><span class="sxs-lookup"><span data-stu-id="c88c9-119">**DriverProvider**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverprovider)           | <span data-ttu-id="c88c9-120">取得 Windows 驅動程式更新的提供者的語言不變名稱。</span><span class="sxs-lookup"><span data-stu-id="c88c9-120">Gets the language-invariant name of the provider of the Windows driver update.</span></span>                                       |
| [<span data-ttu-id="c88c9-121">**DriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="c88c9-121">**DriverVerDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driververdate)             | <span data-ttu-id="c88c9-122">取得 Windows 驅動程式更新的驅動程式版本日期。</span><span class="sxs-lookup"><span data-stu-id="c88c9-122">Gets the driver version date of the Windows driver update.</span></span>                                                           |



 

 

 



