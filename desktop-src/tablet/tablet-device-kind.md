---
description: 表示 tablet 裝置的類型，例如畫筆、滑鼠或觸控式的數位化數位板。
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: TABLET_DEVICE_KIND 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982748"
---
# <a name="tablet_device_kind-enumeration"></a><span data-ttu-id="edca8-103">平板電腦 \_ 裝置 \_ 種類列舉</span><span class="sxs-lookup"><span data-stu-id="edca8-103">TABLET\_DEVICE\_KIND enumeration</span></span>

<span data-ttu-id="edca8-104">表示 tablet 裝置的類型，例如畫筆、滑鼠或觸控式的數位化數位板。</span><span class="sxs-lookup"><span data-stu-id="edca8-104">Indicates the type of tablet device such as a pen, mouse or touch sensitive digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="edca8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="edca8-105">Syntax</span></span>


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a><span data-ttu-id="edca8-106">常數</span><span class="sxs-lookup"><span data-stu-id="edca8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="edca8-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**TABLET \_ 裝置 \_ 滑鼠**</span><span class="sxs-lookup"><span data-stu-id="edca8-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**TABLET\_DEVICE\_MOUSE**</span></span>
</dt> <dd>

<span data-ttu-id="edca8-108">Tablet 是老鼠。</span><span class="sxs-lookup"><span data-stu-id="edca8-108">The tablet is a mouse.</span></span> <span data-ttu-id="edca8-109">這包括在許多膝上型電腦上找到的 touchpads。</span><span class="sxs-lookup"><span data-stu-id="edca8-109">This includes touchpads found on many laptop computers.</span></span>

</dd> <dt>

<span data-ttu-id="edca8-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**TABLET \_ 裝置 \_ 畫筆**</span><span class="sxs-lookup"><span data-stu-id="edca8-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**TABLET\_DEVICE\_PEN**</span></span>
</dt> <dd>

<span data-ttu-id="edca8-111">Tablet 會利用電磁輻射和數位板。</span><span class="sxs-lookup"><span data-stu-id="edca8-111">The tablet utilizes an electromagnetic pen and digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="edca8-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TABLET \_ 裝置 \_ 觸控**</span><span class="sxs-lookup"><span data-stu-id="edca8-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TABLET\_DEVICE\_TOUCH**</span></span>
</dt> <dd>

<span data-ttu-id="edca8-113">Tablet 會利用觸控式的數位化數位板。</span><span class="sxs-lookup"><span data-stu-id="edca8-113">The tablet utilizes a touch sensitive digitizer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="edca8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="edca8-114">Requirements</span></span>



| <span data-ttu-id="edca8-115">需求</span><span class="sxs-lookup"><span data-stu-id="edca8-115">Requirement</span></span> | <span data-ttu-id="edca8-116">值</span><span class="sxs-lookup"><span data-stu-id="edca8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="edca8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edca8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="edca8-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edca8-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="edca8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edca8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="edca8-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="edca8-120">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="edca8-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edca8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edca8-122">**ITablet2：： GetDeviceKind 方法**</span><span class="sxs-lookup"><span data-stu-id="edca8-122">**ITablet2::GetDeviceKind Method**</span></span>](itablet2-getdevicekind.md)
</dt> </dl>

 

 




