---
title: WMDMMessage 列舉
description: WMDMMessage 列舉型別會定義訊息類型和狀態。
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- WMDMMessage 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977419"
---
# <a name="wmdmmessage-enumeration"></a><span data-ttu-id="ecf80-104">WMDMMessage 列舉</span><span class="sxs-lookup"><span data-stu-id="ecf80-104">WMDMMessage enumeration</span></span>

<span data-ttu-id="ecf80-105">**WMDMMessage** 列舉型別會定義訊息類型和狀態。</span><span class="sxs-lookup"><span data-stu-id="ecf80-105">The **WMDMMessage** enumeration type defines message types and states.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf80-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecf80-106">Syntax</span></span>


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a><span data-ttu-id="ecf80-107">常數</span><span class="sxs-lookup"><span data-stu-id="ecf80-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ecf80-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM \_ MSG \_ 裝置 \_ 抵達**</span><span class="sxs-lookup"><span data-stu-id="ecf80-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM\_MSG\_DEVICE\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="ecf80-109">已插入 Windows Media 裝置管理員裝置。</span><span class="sxs-lookup"><span data-stu-id="ecf80-109">A Windows Media Device Manager device has been plugged in.</span></span>

</dd> <dt>

<span data-ttu-id="ecf80-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM \_ MSG \_ 裝置 \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="ecf80-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM\_MSG\_DEVICE\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="ecf80-111">Windows Media 裝置管理員裝置已移除。</span><span class="sxs-lookup"><span data-stu-id="ecf80-111">A Windows Media Device Manager device has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="ecf80-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM \_ MSG \_ 媒體 \_ 抵達**</span><span class="sxs-lookup"><span data-stu-id="ecf80-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM\_MSG\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="ecf80-113">媒體已插入 Windows Media 裝置管理員裝置。</span><span class="sxs-lookup"><span data-stu-id="ecf80-113">Media has been inserted in a Windows Media Device Manager device.</span></span>

</dd> <dt>

<span data-ttu-id="ecf80-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**WMDM \_ MSG \_ 媒體 \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="ecf80-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**WMDM\_MSG\_MEDIA\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="ecf80-115">媒體已從 Windows Media 裝置管理員裝置中移除。</span><span class="sxs-lookup"><span data-stu-id="ecf80-115">Media has been removed from a Windows Media Device Manager device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecf80-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecf80-116">Requirements</span></span>



| <span data-ttu-id="ecf80-117">需求</span><span class="sxs-lookup"><span data-stu-id="ecf80-117">Requirement</span></span> | <span data-ttu-id="ecf80-118">值</span><span class="sxs-lookup"><span data-stu-id="ecf80-118">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf80-119">標頭</span><span class="sxs-lookup"><span data-stu-id="ecf80-119">Header</span></span><br/> | <dl> <span data-ttu-id="ecf80-120"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ecf80-120"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf80-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecf80-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf80-122">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="ecf80-122">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





