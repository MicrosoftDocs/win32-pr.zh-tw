---
description: IWindowsDriverUpdate 介面會定義下列屬性。
ms.assetid: 2177c5e0-47db-44ae-a0ce-2544ff2d0855
title: IWindowsDriverUpdate 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291d7933cf3e73dee6f47edab3240c4ebd14f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974055"
---
# <a name="iwindowsdriverupdate-properties"></a><span data-ttu-id="e33fd-103">IWindowsDriverUpdate 屬性</span><span class="sxs-lookup"><span data-stu-id="e33fd-103">IWindowsDriverUpdate Properties</span></span>

<span data-ttu-id="e33fd-104">[**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="e33fd-104">The [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) interface defines the following properties.</span></span>



| <span data-ttu-id="e33fd-105">屬性</span><span class="sxs-lookup"><span data-stu-id="e33fd-105">Property</span></span>                                                                                                    | <span data-ttu-id="e33fd-106">描述</span><span class="sxs-lookup"><span data-stu-id="e33fd-106">Description</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e33fd-107">[**DeviceProblemNumber**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**位址**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span><span class="sxs-lookup"><span data-stu-id="e33fd-107">[**DeviceProblemNumber**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**Address**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span></span> | <span data-ttu-id="e33fd-108">取得符合 Windows 驅動程式更新之裝置的問題號碼。</span><span class="sxs-lookup"><span data-stu-id="e33fd-108">Gets the problem number of the device that matches for the Windows driver update.</span></span>                     |
| [<span data-ttu-id="e33fd-109">**DeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="e33fd-109">**DeviceStatus**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_devicestatus)                                                   | <span data-ttu-id="e33fd-110">取得符合 Windows 驅動程式更新的裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="e33fd-110">Gets the status of the device that matches for the Windows driver update.</span></span>                             |
| [<span data-ttu-id="e33fd-111">**DriverClass**</span><span class="sxs-lookup"><span data-stu-id="e33fd-111">**DriverClass**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverclass)                                                     | <span data-ttu-id="e33fd-112">取得 Windows 驅動程式更新的類別。</span><span class="sxs-lookup"><span data-stu-id="e33fd-112">Gets the class of the Windows driver update.</span></span>                                                          |
| [<span data-ttu-id="e33fd-113">**DriverHardwareID**</span><span class="sxs-lookup"><span data-stu-id="e33fd-113">**DriverHardwareID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverhardwareid)                                           | <span data-ttu-id="e33fd-114">取得 Windows 驅動程式更新必須符合才能安裝的硬體識別碼或相容識別碼。</span><span class="sxs-lookup"><span data-stu-id="e33fd-114">Gets the hardware ID or compatible ID that the Windows driver update must match to be installable.</span></span>    |
| [<span data-ttu-id="e33fd-115">**DriverManufacturer**</span><span class="sxs-lookup"><span data-stu-id="e33fd-115">**DriverManufacturer**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermanufacturer)                                       | <span data-ttu-id="e33fd-116">取得 Windows 驅動程式更新之製造商的語言不變名稱。</span><span class="sxs-lookup"><span data-stu-id="e33fd-116">Gets the language-invariant name of the manufacturer of the Windows driver update.</span></span>                    |
| [<span data-ttu-id="e33fd-117">**DriverModel**</span><span class="sxs-lookup"><span data-stu-id="e33fd-117">**DriverModel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermodel)                                                     | <span data-ttu-id="e33fd-118">取得適用于 Windows 驅動程式更新之裝置的語言不變模型名稱。</span><span class="sxs-lookup"><span data-stu-id="e33fd-118">Gets the language-invariant model name of the device for which the Windows driver update is intended.</span></span> |
| [<span data-ttu-id="e33fd-119">**DriverProvider**</span><span class="sxs-lookup"><span data-stu-id="e33fd-119">**DriverProvider**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverprovider)                                               | <span data-ttu-id="e33fd-120">取得 Windows 驅動程式更新的提供者的語言不變名稱。</span><span class="sxs-lookup"><span data-stu-id="e33fd-120">Gets the language-invariant name of the provider of the Windows driver update.</span></span>                        |
| [<span data-ttu-id="e33fd-121">**DriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="e33fd-121">**DriverVerDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driververdate)                                                 | <span data-ttu-id="e33fd-122">取得 Windows 驅動程式更新的驅動程式版本日期。</span><span class="sxs-lookup"><span data-stu-id="e33fd-122">Gets the driver version date of the Windows driver update.</span></span>                                            |



 

 

 



