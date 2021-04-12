---
description: 連接新的 Windows 映像取得 (WIA) 硬體裝置時所發生的事件。
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Wia. OnDeviceConnected 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192805"
---
# <a name="wiaondeviceconnected-event"></a><span data-ttu-id="22235-103">Wia. OnDeviceConnected 事件</span><span class="sxs-lookup"><span data-stu-id="22235-103">Wia.OnDeviceConnected event</span></span>

<span data-ttu-id="22235-104">連接新的 Windows 映像取得 (WIA) 硬體裝置時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="22235-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="22235-105">語法</span><span class="sxs-lookup"><span data-stu-id="22235-105">Syntax</span></span>


```JScript
Wia.OnDeviceConnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="22235-106">參數</span><span class="sxs-lookup"><span data-stu-id="22235-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22235-107">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="22235-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="22235-108">字串，其中包含已連線裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="22235-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22235-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="22235-109">Return value</span></span>

<span data-ttu-id="22235-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="22235-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22235-111">備註</span><span class="sxs-lookup"><span data-stu-id="22235-111">Remarks</span></span>

<span data-ttu-id="22235-112">每當有新的硬體裝置連接到電腦時，WIA 都會通知腳本或應用程式。</span><span class="sxs-lookup"><span data-stu-id="22235-112">WIA notifies the script or application whenever a new hardware device is connected to the computer.</span></span> <span data-ttu-id="22235-113">執行 **objWia** \_ **OnDeviceConnected ()** 副程式，以允許腳本或應用程式回應裝置連線。</span><span class="sxs-lookup"><span data-stu-id="22235-113">Implement the **objWia**\_**OnDeviceConnected()** subroutine to allow the script or application to respond to the device connection.</span></span>

<span data-ttu-id="22235-114">例如，您可能想要在安裝新裝置時，重新整理 [**裝置**](-wia-iwia-devices.md) 集合的腳本。</span><span class="sxs-lookup"><span data-stu-id="22235-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a new device is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="22235-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="22235-115">Requirements</span></span>



| <span data-ttu-id="22235-116">需求</span><span class="sxs-lookup"><span data-stu-id="22235-116">Requirement</span></span> | <span data-ttu-id="22235-117">值</span><span class="sxs-lookup"><span data-stu-id="22235-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22235-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22235-118">Minimum supported client</span></span><br/> | <span data-ttu-id="22235-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22235-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22235-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22235-120">Minimum supported server</span></span><br/> | <span data-ttu-id="22235-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22235-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="22235-122">DLL</span><span class="sxs-lookup"><span data-stu-id="22235-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22235-123"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="22235-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




