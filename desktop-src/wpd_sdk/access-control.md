---
description: 存取控制
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: " (WPD API) 的存取控制"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852156"
---
# <a name="access-control-wpd-api"></a><span data-ttu-id="4de05-103"> (WPD API) 的存取控制</span><span class="sxs-lookup"><span data-stu-id="4de05-103">Access Control (WPD API)</span></span>

<span data-ttu-id="4de05-104">Windows Driver Model (WDM) 支援在) 隨插即用 PnP (裝置節點上，透過存取控制清單來限制裝置存取 (Acl) 。</span><span class="sxs-lookup"><span data-stu-id="4de05-104">The Windows Driver Model (WDM) supports restricting device access via Access Control Lists (ACLs) on the Plug and Play (PnP) Device Nodes.</span></span> <span data-ttu-id="4de05-105">這表示廠商和網路系統管理員可以限制對任何裝置類型的存取。</span><span class="sxs-lookup"><span data-stu-id="4de05-105">This means that vendors and network administrators can restrict access to any device type.</span></span> <span data-ttu-id="4de05-106">當應用程式透過呼叫 [**IPortableDevice：： Open 開啟**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)驅動程式的控制碼時，驅動程式的 i/o 管理員會驗證指定的使用者是否具有必要的存取權，而且當 IOCTLs 從該控制碼傳送至驅動程式時，也會有同樣的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="4de05-106">When an application opens a handle to a driver by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), the driver's I/O Manager verifies whether the given user has the required access, and similarly does access checks when IOCTLs are sent to the driver from that handle.</span></span>

<span data-ttu-id="4de05-107">例如，網路系統管理員可以將來賓使用者限制為可存取可攜式裝置的唯讀存取權，並將其授與已驗證的使用者讀取/寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="4de05-107">For example, a network administrator could restrict Guest users to read-only access for portable devices, while they could grant Authenticated users read/write access.</span></span> <span data-ttu-id="4de05-108">在此情況下，這表示如果來賓發出需要讀取/寫入存取權的 WPD 命令 (例如刪除物件) ;它會因為拒絕存取而失敗，而如果已驗證的使用者發出相同的命令，則會成功。</span><span class="sxs-lookup"><span data-stu-id="4de05-108">In this case, it implies that if a Guest issued a WPD command that required read/write access (such as Delete Object); it would fail with Access Denied, whereas if an Authenticated user issued the same command, it would succeed.</span></span>

<span data-ttu-id="4de05-109">用來控制卸除式存放裝置和可攜式裝置存取權的群組原則專案，其實不是讓系統管理員輕鬆地將 PnP 裝置節點 Acl 套用到整個裝置類別的方法 (例如，套用「拒絕可攜式裝置的寫入權限」群組原則會調整所有 WPD 裝置的 Acl，以拒絕) 的寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="4de05-109">The Group Policy entries for controlling access to removable storage and portable devices is actually nothing more than an easy way for Administrators to apply PnP device node ACLs to a whole class of devices at a time (for example, applying the "Deny Write Access to Portable Devices" Group Policy would adjust the ACLs of all WPD devices to deny write access).</span></span>

## <a name="io-control-codes-in-wpd"></a><span data-ttu-id="4de05-110">WPD 中的 i/o 控制碼</span><span class="sxs-lookup"><span data-stu-id="4de05-110">I/O Control Codes in WPD</span></span>

<span data-ttu-id="4de05-111">WPD 應用程式會藉由開啟裝置控制碼和傳送 i/o 控制項碼 (IOCTLs) 來與驅動程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="4de05-111">WPD applications communicate with drivers by opening device handles and sending I/O Control Codes (IOCTLs).</span></span> <span data-ttu-id="4de05-112">這些 IOCTLs 包含四個區段：</span><span class="sxs-lookup"><span data-stu-id="4de05-112">These IOCTLs consist of four sections:</span></span>

1.  <span data-ttu-id="4de05-113">裝置類型</span><span class="sxs-lookup"><span data-stu-id="4de05-113">Device Type</span></span>
2.  <span data-ttu-id="4de05-114">函數代碼</span><span class="sxs-lookup"><span data-stu-id="4de05-114">Function Code</span></span>
3.  <span data-ttu-id="4de05-115">Buffer 方法</span><span class="sxs-lookup"><span data-stu-id="4de05-115">Buffer Method</span></span>
4.  <span data-ttu-id="4de05-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="4de05-116">Access Type</span></span>

<span data-ttu-id="4de05-117">第四個區段（存取類型）指定給定命令的特定存取需求。</span><span class="sxs-lookup"><span data-stu-id="4de05-117">The fourth section, the Access Type, specifies the specific access requirement for the given command.</span></span> <span data-ttu-id="4de05-118">驅動程式的 i/o 管理員會使用此資料來執行 (ACL) 檢查的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="4de05-118">The driver's I/O manager uses this data to perform the Access Control List (ACL) check.</span></span>

<span data-ttu-id="4de05-119">如果將 IOCTL 定義為：</span><span class="sxs-lookup"><span data-stu-id="4de05-119">So if an IOCTL were defined as:</span></span>


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



<span data-ttu-id="4de05-120">驅動程式的 i/o 管理員會在傳送此訊息時，檢查裝置控制碼的擁有者是否具有裝置的讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="4de05-120">The driver's I/O manager would check that the owner of the device handle has read access to the device when this message is sent.</span></span>

<span data-ttu-id="4de05-121">而且，如果將 IOCTL 定義為：</span><span class="sxs-lookup"><span data-stu-id="4de05-121">And, if an IOCTL were defined as:</span></span>


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



<span data-ttu-id="4de05-122">當傳送此訊息時，驅動程式的 i/o 管理員會檢查裝置控制碼的擁有者是否具有裝置的讀取/寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="4de05-122">The driver's I/O manager would check that the owner of the device handle has read/write access to the device when this message is sent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4de05-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="4de05-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4de05-124">**應用程式總覽**</span><span class="sxs-lookup"><span data-stu-id="4de05-124">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="4de05-125">**IPortableDevice：： Open**</span><span class="sxs-lookup"><span data-stu-id="4de05-125">**IPortableDevice::Open**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[<span data-ttu-id="4de05-126">**IPortableDevice：： SendCommand**</span><span class="sxs-lookup"><span data-stu-id="4de05-126">**IPortableDevice::SendCommand**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



