---
description: 表示用於監視和報告的服務狀態變更類型。
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: 'SC_EVENT_TYPE 列舉 (Winsvcp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989009"
---
# <a name="sc_event_type-enumeration"></a><span data-ttu-id="152fe-103">SC \_ 事件 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="152fe-103">SC\_EVENT\_TYPE enumeration</span></span>

<span data-ttu-id="152fe-104">表示用於監視和報告的服務狀態變更類型。</span><span class="sxs-lookup"><span data-stu-id="152fe-104">Indicates a type of service status change for monitoring and reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="152fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="152fe-105">Syntax</span></span>


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="152fe-106">常數</span><span class="sxs-lookup"><span data-stu-id="152fe-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="152fe-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**SC \_ 事件 \_ 資料庫 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="152fe-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**SC\_EVENT\_DATABASE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="152fe-108">已新增或刪除服務。</span><span class="sxs-lookup"><span data-stu-id="152fe-108">A service has been added or deleted.</span></span> <span data-ttu-id="152fe-109">[**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)函數的 *hService* 參數必須是 SCM 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="152fe-109">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the SCM.</span></span>

</dd> <dt>

<span data-ttu-id="152fe-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**SC \_ 事件 \_ 屬性 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="152fe-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**SC\_EVENT\_PROPERTY\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="152fe-111">已更新一或多個服務屬性。</span><span class="sxs-lookup"><span data-stu-id="152fe-111">One or more of service properties have been updated.</span></span> <span data-ttu-id="152fe-112">[**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)函數的 *hService* 參數必須是服務的控制碼。</span><span class="sxs-lookup"><span data-stu-id="152fe-112">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> <dt>

<span data-ttu-id="152fe-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**SC \_ 事件 \_ 狀態 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="152fe-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**SC\_EVENT\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="152fe-114">服務的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="152fe-114">The status of a service has changed.</span></span> <span data-ttu-id="152fe-115">[**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md)函數的 *hService* 參數必須是服務的控制碼。</span><span class="sxs-lookup"><span data-stu-id="152fe-115">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="152fe-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="152fe-116">Requirements</span></span>



| <span data-ttu-id="152fe-117">需求</span><span class="sxs-lookup"><span data-stu-id="152fe-117">Requirement</span></span> | <span data-ttu-id="152fe-118">值</span><span class="sxs-lookup"><span data-stu-id="152fe-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="152fe-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="152fe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="152fe-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="152fe-120">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="152fe-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="152fe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="152fe-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="152fe-122">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="152fe-123">標頭</span><span class="sxs-lookup"><span data-stu-id="152fe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="152fe-124"><dt>Winsvcp。h</dt></span><span class="sxs-lookup"><span data-stu-id="152fe-124"><dt>Winsvcp.h</dt></span></span> </dl> |



 

 




