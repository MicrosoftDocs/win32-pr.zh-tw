---
title: 軟體裝置 API 函式
description: 本節說明用戶端應用程式所呼叫的軟體裝置 API 函式，以及用戶端應用程式所執行的回呼函數。
ms.assetid: 68F142A9-08AD-4F74-A0C3-3DCC8F7449B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a3cc9f0cd8b018f40210c434ee22b3512b2e81
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382638"
---
# <a name="software-device-api-functions"></a><span data-ttu-id="f15d2-103">軟體裝置 API 函式</span><span class="sxs-lookup"><span data-stu-id="f15d2-103">Software Device API Functions</span></span>

<span data-ttu-id="f15d2-104">本節說明用戶端應用程式所呼叫的軟體裝置 API 函式，以及用戶端應用程式所執行的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="f15d2-104">This section describes Software Device API functions that a client app calls and a callback function that a client app implements.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f15d2-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="f15d2-105">In this section</span></span>



| <span data-ttu-id="f15d2-106">主題</span><span class="sxs-lookup"><span data-stu-id="f15d2-106">Topic</span></span>                                                                           | <span data-ttu-id="f15d2-107">描述</span><span class="sxs-lookup"><span data-stu-id="f15d2-107">Description</span></span>                                                                                                                                                      |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f15d2-108">**SwDeviceClose**</span><span class="sxs-lookup"><span data-stu-id="f15d2-108">**SwDeviceClose**</span></span>](/windows/win32/api/swdevice/nf-swdevice-swdeviceclose)<br/>                               | <span data-ttu-id="f15d2-109">關閉軟體裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="f15d2-109">Closes the software device handle.</span></span> <span data-ttu-id="f15d2-110">當控制碼關閉時，PnP 將會起始移除裝置的進程。</span><span class="sxs-lookup"><span data-stu-id="f15d2-110">When the handle is closed, PnP will initiate the process of removing the device.</span></span><br/>                                   |
| [<span data-ttu-id="f15d2-111">**SW \_ 裝置 \_ 建立 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="f15d2-111">**SW\_DEVICE\_CREATE\_CALLBACK**</span></span>](/windows/win32/api/swdevice/nc-swdevice-sw_device_create_callback)<br/>    | <span data-ttu-id="f15d2-112">提供在登錄中支援的裝置，並可讓呼叫者使用 *hSwDevice* 控制碼呼叫軟體裝置 API 函式。</span><span class="sxs-lookup"><span data-stu-id="f15d2-112">Provides a device with backing in the registry and allows the caller to then make calls to Software Device API functions with the *hSwDevice* handle.</span></span><br/> |
| [<span data-ttu-id="f15d2-113">**SwDeviceCreate**</span><span class="sxs-lookup"><span data-stu-id="f15d2-113">**SwDeviceCreate**</span></span>](/windows/win32/api/swdevice/nf-swdevice-swdevicecreate)<br/>                             | <span data-ttu-id="f15d2-114">起始軟體裝置的列舉。</span><span class="sxs-lookup"><span data-stu-id="f15d2-114">Initiates the enumeration of a software device.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="f15d2-115">**SwDeviceGetLifetime**</span><span class="sxs-lookup"><span data-stu-id="f15d2-115">**SwDeviceGetLifetime**</span></span>](/windows/win32/api/swdevice/nf-swdevice-swdevicegetlifetime)<br/>                   | <span data-ttu-id="f15d2-116">取得軟體裝置的存留期。</span><span class="sxs-lookup"><span data-stu-id="f15d2-116">Gets the lifetime of a software device.</span></span> <br/>                                                                                                              |
| [<span data-ttu-id="f15d2-117">**SwDeviceInterfacePropertySet**</span><span class="sxs-lookup"><span data-stu-id="f15d2-117">**SwDeviceInterfacePropertySet**</span></span>](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacepropertyset)<br/> | <span data-ttu-id="f15d2-118">設定軟體裝置介面上的屬性。</span><span class="sxs-lookup"><span data-stu-id="f15d2-118">Sets properties on a software device interface.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="f15d2-119">**SwDeviceInterfaceRegister**</span><span class="sxs-lookup"><span data-stu-id="f15d2-119">**SwDeviceInterfaceRegister**</span></span>](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfaceregister)<br/>       | <span data-ttu-id="f15d2-120">註冊軟體裝置的裝置介面，並選擇性地設定該介面上的屬性。</span><span class="sxs-lookup"><span data-stu-id="f15d2-120">Registers a device interface for a software device and optionally sets properties on that interface.</span></span> <br/>                                                 |
| [<span data-ttu-id="f15d2-121">**SwDeviceInterfaceSetState**</span><span class="sxs-lookup"><span data-stu-id="f15d2-121">**SwDeviceInterfaceSetState**</span></span>](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacesetstate)<br/>       | <span data-ttu-id="f15d2-122">啟用或停用軟體裝置的裝置介面。</span><span class="sxs-lookup"><span data-stu-id="f15d2-122">Enables or disables a device interface for a software device.</span></span> <br/>                                                                                        |
| [<span data-ttu-id="f15d2-123">**SwDevicePropertySet**</span><span class="sxs-lookup"><span data-stu-id="f15d2-123">**SwDevicePropertySet**</span></span>](/windows/win32/api/swdevice/nf-swdevice-swdevicepropertyset)<br/>                   | <span data-ttu-id="f15d2-124">設定軟體裝置上的屬性。</span><span class="sxs-lookup"><span data-stu-id="f15d2-124">Sets properties on a software device.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="f15d2-125">**SwDeviceSetLifetime**</span><span class="sxs-lookup"><span data-stu-id="f15d2-125">**SwDeviceSetLifetime**</span></span>](/windows/win32/api/swdevice/nf-swdevice-swdevicesetlifetime)<br/>                   | <span data-ttu-id="f15d2-126">管理軟體裝置的存留期。</span><span class="sxs-lookup"><span data-stu-id="f15d2-126">Manages the lifetime of a software device.</span></span> <br/>                                                                                                           |
| [<span data-ttu-id="f15d2-127">**SwMemFree**</span><span class="sxs-lookup"><span data-stu-id="f15d2-127">**SwMemFree**</span></span>](/windows/win32/api/swdevice/nf-swdevice-swmemfree)<br/>                                       | <span data-ttu-id="f15d2-128">釋出其他軟體裝置 API 功能所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f15d2-128">Frees memory that other Software Device API functions allocated.</span></span><br/>                                                                                      |



 

 

 

[<span data-ttu-id="f15d2-129">將關於本主題的意見傳送給 Microsoft</span><span class="sxs-lookup"><span data-stu-id="f15d2-129">Send comments about this topic to Microsoft</span></span>](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20Functions%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "將關於本主題的意見傳送給 Microsoft")