---
description: 抓取 Windows 映像取得 (WIA) 硬體裝置的類型。
ms.assetid: 5f10bcd1-03a0-4cd9-8886-e1f957312c3b
title: DeviceInfo。 Type 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Type
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 89a322890f035a1865c01be7c4bfb0bbab812fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972465"
---
# <a name="deviceinfotype-property"></a><span data-ttu-id="fd9df-103">DeviceInfo。 Type 屬性</span><span class="sxs-lookup"><span data-stu-id="fd9df-103">DeviceInfo.Type property</span></span>

<span data-ttu-id="fd9df-104">抓取 Windows 映像取得 (WIA) 硬體裝置的類型。</span><span class="sxs-lookup"><span data-stu-id="fd9df-104">Retrieves the type of Windows Image Acquisition (WIA) hardware device.</span></span> <span data-ttu-id="fd9df-105">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="fd9df-105">Possible values are:</span></span>

-   <span data-ttu-id="fd9df-106">DigitalCamera</span><span class="sxs-lookup"><span data-stu-id="fd9df-106">DigitalCamera</span></span>
-   <span data-ttu-id="fd9df-107">掃描器</span><span class="sxs-lookup"><span data-stu-id="fd9df-107">Scanner</span></span>
-   <span data-ttu-id="fd9df-108">StreamingVideo</span><span class="sxs-lookup"><span data-stu-id="fd9df-108">StreamingVideo</span></span>
-   <span data-ttu-id="fd9df-109">預設</span><span class="sxs-lookup"><span data-stu-id="fd9df-109">Default</span></span>

<span data-ttu-id="fd9df-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="fd9df-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9df-111">語法</span><span class="sxs-lookup"><span data-stu-id="fd9df-111">Syntax</span></span>


```JScript
propVal = DeviceInfo.Type
```



## <a name="property-value"></a><span data-ttu-id="fd9df-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="fd9df-112">Property value</span></span>

<span data-ttu-id="fd9df-113">接收裝置的字串。</span><span class="sxs-lookup"><span data-stu-id="fd9df-113">String that receives the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd9df-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd9df-114">Requirements</span></span>



| <span data-ttu-id="fd9df-115">需求</span><span class="sxs-lookup"><span data-stu-id="fd9df-115">Requirement</span></span> | <span data-ttu-id="fd9df-116">值</span><span class="sxs-lookup"><span data-stu-id="fd9df-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9df-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd9df-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fd9df-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd9df-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd9df-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd9df-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fd9df-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd9df-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fd9df-121">DLL</span><span class="sxs-lookup"><span data-stu-id="fd9df-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd9df-122"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="fd9df-122"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




