---
description: 在決定電話裝置的功能之後，應用程式必須先開啟裝置，才能存取該手機上的功能。
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: 開啟和關閉手機裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998465"
---
# <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="fe80b-103">開啟和關閉手機裝置</span><span class="sxs-lookup"><span data-stu-id="fe80b-103">Opening and Closing Phone Devices</span></span>

<span data-ttu-id="fe80b-104">在決定電話裝置的功能之後，應用程式必須先開啟裝置，才能存取該手機上的功能。</span><span class="sxs-lookup"><span data-stu-id="fe80b-104">After determining the capabilities of a phone device, an application must open the device before it can access functions on that phone.</span></span> <span data-ttu-id="fe80b-105">成功開啟手機裝置之後，應用程式會傳回代表開啟電話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe80b-105">After a phone device has been successfully opened, the application is returned a handle representing the open phone.</span></span> <span data-ttu-id="fe80b-106">您可以使用不同的模式開啟手機裝置，藉此提供共用電話裝置的結構化方式。</span><span class="sxs-lookup"><span data-stu-id="fe80b-106">A phone device can be opened in different modes, thus providing a structured way of sharing a phone device.</span></span>

<span data-ttu-id="fe80b-107">[**PhoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)函式會開啟指定的電話裝置，讓應用程式能夠存取電話上的功能。</span><span class="sxs-lookup"><span data-stu-id="fe80b-107">The [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) function opens the specified phone device to give the application access to functions on the phone.</span></span> <span data-ttu-id="fe80b-108">電話裝置會透過裝置識別碼（以 *dwDeviceID* 參數傳遞）來識別 **phoneOpen** 。</span><span class="sxs-lookup"><span data-stu-id="fe80b-108">A phone device is identified to **phoneOpen** by means of its device identifier, which is passed as the *dwDeviceID* parameter.</span></span>

 

 



