---
description: DeviceInfo 物件的 Create 方法會連線到 DeviceInfo 物件所指定的 Windows 映像取得 (WIA) 裝置，並傳回代表該裝置的專案物件。
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: DeviceInfo. Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974139"
---
# <a name="deviceinfocreate-method"></a><span data-ttu-id="1ad0a-103">DeviceInfo. Create 方法</span><span class="sxs-lookup"><span data-stu-id="1ad0a-103">DeviceInfo.Create method</span></span>

<span data-ttu-id="1ad0a-104">[**DeviceInfo**](-wia-deviceinfo.md)物件的 **Create** 方法會連線到 **DeviceInfo** 物件所指定的 Windows 映像取得 (WIA) 裝置，並傳回代表該裝置的 [**專案**](-wia-item.md)物件。</span><span class="sxs-lookup"><span data-stu-id="1ad0a-104">The **Create** method of the [**DeviceInfo**](-wia-deviceinfo.md) object makes a connection to the Windows Image Acquisition (WIA) device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad0a-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ad0a-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a><span data-ttu-id="1ad0a-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ad0a-106">Parameters</span></span>

<span data-ttu-id="1ad0a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1ad0a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ad0a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ad0a-108">Return value</span></span>

<span data-ttu-id="1ad0a-109">類型： **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="1ad0a-109">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="1ad0a-110">這個方法會傳回代表所建立裝置的 [**專案**](-wia-item.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="1ad0a-110">This method returns the [**Item**](-wia-item.md) object that represents the device that is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad0a-111">備註</span><span class="sxs-lookup"><span data-stu-id="1ad0a-111">Remarks</span></span>

<span data-ttu-id="1ad0a-112">列舉 [**裝置**](-wia-iwia-devices.md)集合之後，請使用 **create** 方法來建立與 WIA 硬體裝置的連接。</span><span class="sxs-lookup"><span data-stu-id="1ad0a-112">Use the **Create** method to create a connection to a WIA hardware device after enumerating the [**Devices**](-wia-iwia-devices.md) collection.</span></span> <span data-ttu-id="1ad0a-113">方法會傳回代表 (根專案) 之裝置的 [**專案**](-wia-item.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="1ad0a-113">The method returns an [**Item**](-wia-item.md) object that represents the device (a root item).</span></span>

## <a name="examples"></a><span data-ttu-id="1ad0a-114">範例</span><span class="sxs-lookup"><span data-stu-id="1ad0a-114">Examples</span></span>

<span data-ttu-id="1ad0a-115">下列範例將示範 **Create** 方法的使用方式。</span><span class="sxs-lookup"><span data-stu-id="1ad0a-115">The following example demonstrates the use of the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="1ad0a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ad0a-116">Requirements</span></span>



| <span data-ttu-id="1ad0a-117">需求</span><span class="sxs-lookup"><span data-stu-id="1ad0a-117">Requirement</span></span> | <span data-ttu-id="1ad0a-118">值</span><span class="sxs-lookup"><span data-stu-id="1ad0a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad0a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ad0a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1ad0a-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ad0a-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ad0a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ad0a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1ad0a-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ad0a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1ad0a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1ad0a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ad0a-124"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="1ad0a-124"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




