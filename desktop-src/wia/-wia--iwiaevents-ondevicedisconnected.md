---
description: 當新的 Windows 映像取得 (WIA) 硬體裝置中斷連線時所發生的事件。
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Wia. OnDeviceDisconnected 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192804"
---
# <a name="wiaondevicedisconnected-event"></a><span data-ttu-id="7fdf5-103">Wia. OnDeviceDisconnected 事件</span><span class="sxs-lookup"><span data-stu-id="7fdf5-103">Wia.OnDeviceDisconnected event</span></span>

<span data-ttu-id="7fdf5-104">當新的 Windows 映像取得 (WIA) 硬體裝置中斷連線時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="7fdf5-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is disconnected.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fdf5-105">語法</span><span class="sxs-lookup"><span data-stu-id="7fdf5-105">Syntax</span></span>


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="7fdf5-106">參數</span><span class="sxs-lookup"><span data-stu-id="7fdf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fdf5-107">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="7fdf5-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="7fdf5-108">字串，其中包含已連線裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7fdf5-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fdf5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7fdf5-109">Return value</span></span>

<span data-ttu-id="7fdf5-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7fdf5-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fdf5-111">備註</span><span class="sxs-lookup"><span data-stu-id="7fdf5-111">Remarks</span></span>

<span data-ttu-id="7fdf5-112">當硬體裝置與電腦中斷連線時，WIA 會通知腳本或應用程式。</span><span class="sxs-lookup"><span data-stu-id="7fdf5-112">WIA notifies the script or application whenever a hardware device is disconnected from the computer.</span></span> <span data-ttu-id="7fdf5-113">執行 **objWia** \_ **OnDeviceDisconnected ()** 副程式，以允許腳本或應用程式回應裝置中斷連接。</span><span class="sxs-lookup"><span data-stu-id="7fdf5-113">Implement the **objWia**\_**OnDeviceDisconnected()** subroutine to allow the script or application to respond to the device disconnection.</span></span>

<span data-ttu-id="7fdf5-114">例如，您可能想要在從電腦移除裝置時，重新整理 [**裝置**](-wia-iwia-devices.md) 集合的腳本。</span><span class="sxs-lookup"><span data-stu-id="7fdf5-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a device is removed from the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fdf5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fdf5-115">Requirements</span></span>



| <span data-ttu-id="7fdf5-116">需求</span><span class="sxs-lookup"><span data-stu-id="7fdf5-116">Requirement</span></span> | <span data-ttu-id="7fdf5-117">值</span><span class="sxs-lookup"><span data-stu-id="7fdf5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fdf5-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fdf5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7fdf5-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fdf5-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fdf5-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fdf5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7fdf5-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fdf5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7fdf5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7fdf5-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fdf5-123"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="7fdf5-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




