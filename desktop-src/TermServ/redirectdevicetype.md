---
title: RedirectDeviceType 列舉
description: 用來指定裝置的類型。
ms.assetid: B6356217-814E-462F-9DBC-F6D3C0CE129F
ms.tgt_platform: multiple
keywords:
- RedirectDeviceType 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- RedirectDeviceType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7058313e7f987589ae17924cce6a95610d997ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966108"
---
# <a name="redirectdevicetype-enumeration"></a><span data-ttu-id="81259-104">RedirectDeviceType 列舉</span><span class="sxs-lookup"><span data-stu-id="81259-104">RedirectDeviceType enumeration</span></span>

<span data-ttu-id="81259-105">用來指定裝置的類型。</span><span class="sxs-lookup"><span data-stu-id="81259-105">Used to specify the type of a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="81259-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="81259-106">Syntax</span></span>


```C++
typedef enum  { 
  UsbDevice  = 0
} RedirectDeviceType;
```



## <a name="constants"></a><span data-ttu-id="81259-107">常數</span><span class="sxs-lookup"><span data-stu-id="81259-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="81259-108"><span id="UsbDevice"></span><span id="usbdevice"></span><span id="USBDEVICE"></span>**UsbDevice**</span><span class="sxs-lookup"><span data-stu-id="81259-108"><span id="UsbDevice"></span><span id="usbdevice"></span><span id="USBDEVICE"></span>**UsbDevice**</span></span>
</dt> <dd>

<span data-ttu-id="81259-109">USB 裝置。</span><span class="sxs-lookup"><span data-stu-id="81259-109">A USB device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81259-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="81259-110">Requirements</span></span>



| <span data-ttu-id="81259-111">需求</span><span class="sxs-lookup"><span data-stu-id="81259-111">Requirement</span></span> | <span data-ttu-id="81259-112">值</span><span class="sxs-lookup"><span data-stu-id="81259-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81259-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="81259-113">Minimum supported client</span></span><br/> | <span data-ttu-id="81259-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="81259-114">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="81259-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="81259-115">Minimum supported server</span></span><br/> | <span data-ttu-id="81259-116">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81259-116">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="81259-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="81259-117">Type library</span></span><br/>             | <dl> <span data-ttu-id="81259-118"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81259-118"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81259-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81259-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81259-120">**AddDeviceByInstanceId**</span><span class="sxs-lookup"><span data-stu-id="81259-120">**AddDeviceByInstanceId**</span></span>](imsrdpdevicecollection2-adddevicebyinstanceid.md)
</dt> <dt>

[<span data-ttu-id="81259-121">**RedirectNow**</span><span class="sxs-lookup"><span data-stu-id="81259-121">**RedirectNow**</span></span>](imsrdpdevicecollection2-redirectnow.md)
</dt> </dl>

 

 





