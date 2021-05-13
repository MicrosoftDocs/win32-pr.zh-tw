---
description: DeviceInfo 物件的集合，代表安裝在電腦上的所有裝置。
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: Wia. Devices 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b4d98bfe1552156071efde0b46899ad058e75aec
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841310"
---
# <a name="wiadevices-property"></a><span data-ttu-id="7602a-103">Wia. Devices 屬性</span><span class="sxs-lookup"><span data-stu-id="7602a-103">Wia.Devices property</span></span>

<span data-ttu-id="7602a-104">[**DeviceInfo**](-wia-deviceinfo.md)物件的集合，代表安裝在電腦上的所有裝置。</span><span class="sxs-lookup"><span data-stu-id="7602a-104">Collection of [**DeviceInfo**](-wia-deviceinfo.md) objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="7602a-105">唯讀。</span><span class="sxs-lookup"><span data-stu-id="7602a-105">Read-only.</span></span>

> [!Note]  
> <span data-ttu-id="7602a-106">這個集合是以0為基礎。</span><span class="sxs-lookup"><span data-stu-id="7602a-106">This collection is 0-based.</span></span>

 

<span data-ttu-id="7602a-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="7602a-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7602a-108">語法</span><span class="sxs-lookup"><span data-stu-id="7602a-108">Syntax</span></span>


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a><span data-ttu-id="7602a-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="7602a-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="7602a-110">範例</span><span class="sxs-lookup"><span data-stu-id="7602a-110">Examples</span></span>

<span data-ttu-id="7602a-111">下列範例說明如何使用 **裝置** 集合來列舉系統上的裝置。</span><span class="sxs-lookup"><span data-stu-id="7602a-111">The following example illustrates the use of the **Devices** collection to enumerate the devices on a system.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="7602a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7602a-112">Requirements</span></span>



| <span data-ttu-id="7602a-113">需求</span><span class="sxs-lookup"><span data-stu-id="7602a-113">Requirement</span></span> | <span data-ttu-id="7602a-114">值</span><span class="sxs-lookup"><span data-stu-id="7602a-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7602a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7602a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7602a-116">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7602a-116">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7602a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7602a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7602a-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7602a-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7602a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7602a-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7602a-120"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="7602a-120"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




