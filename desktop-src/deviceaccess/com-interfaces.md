---
title: COM 介面-裝置存取
description: 元件物件模型 (裝置存取 API 中的 COM) 介面。
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 07abbfd15f8383bbbd9cd9d1f5fc4c9fb1f42b9e
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024289"
---
# <a name="com-interfaces---device-access"></a><span data-ttu-id="1773b-103">COM 介面-裝置存取</span><span class="sxs-lookup"><span data-stu-id="1773b-103">COM Interfaces - Device Access</span></span>

<span data-ttu-id="1773b-104">元件物件模型 (裝置存取 API 中的 COM) 介面。</span><span class="sxs-lookup"><span data-stu-id="1773b-104">Component Object Model (COM)interfaces in the Device Access API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1773b-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="1773b-105">In this section</span></span>

| <span data-ttu-id="1773b-106">主題</span><span class="sxs-lookup"><span data-stu-id="1773b-106">Topic</span></span> | <span data-ttu-id="1773b-107">描述</span><span class="sxs-lookup"><span data-stu-id="1773b-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="1773b-108">**ICreateDeviceAccessAsync**</span><span class="sxs-lookup"><span data-stu-id="1773b-108">**ICreateDeviceAccessAsync**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | <span data-ttu-id="1773b-109">[**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)介面會從對 CreateDeviceAccessInstance 的呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="1773b-109">The [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) interface is returned from a call to CreateDeviceAccessInstance.</span></span> <span data-ttu-id="1773b-110">它可讓呼叫端控制系結至裝置實例的作業，以抓取可用於與該裝置互動的另一個介面。</span><span class="sxs-lookup"><span data-stu-id="1773b-110">It enables the caller to control the operation of binding to an instance of a device in order to retrieve another interface that can be used to interact with that device.</span></span><br/> |
| [<span data-ttu-id="1773b-111">**IDeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="1773b-111">**IDeviceIoControl**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | <span data-ttu-id="1773b-112">將控制程式代碼傳送至設備磁碟機。此動作會導致裝置執行對應的操作。</span><span class="sxs-lookup"><span data-stu-id="1773b-112">Sends a control code to a device driver.This action causes the device to perform the corresponding operation.</span></span> <br/> |
| [<span data-ttu-id="1773b-113">**IDeviceRequestCompletionCallback**</span><span class="sxs-lookup"><span data-stu-id="1773b-113">**IDeviceRequestCompletionCallback**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | <span data-ttu-id="1773b-114">提供方法來處理 [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)方法的呼叫完成。</span><span class="sxs-lookup"><span data-stu-id="1773b-114">Provides a method to handle the completion of calls to the [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)method.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="1773b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="1773b-115">Related topics</span></span>

<span data-ttu-id="1773b-116">[自訂驅動程式存取範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)、 [適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)、 [硬體開發人員中心](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="1773b-116">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
