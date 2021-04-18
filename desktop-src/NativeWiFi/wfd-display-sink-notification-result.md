---
description: 描述在 [WFD \_ 顯示 \_ 接收] \_ 通知回呼函式中處理顯示接收器通知之後，您可以選擇性地設定的結果 \_ 。
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: 'WFD_DISPLAY_SINK_NOTIFICATION_RESULT 結構 (Wfdsink .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: dc23416d4d13284862aea652dd71909e71879afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971607"
---
# <a name="wfd_display_sink_notification_result-structure"></a><span data-ttu-id="cc4ae-103">WFD \_ 顯示 \_ 接收 \_ 通知 \_ 結果結構</span><span class="sxs-lookup"><span data-stu-id="cc4ae-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT structure</span></span>

<span data-ttu-id="cc4ae-104">[ **Wfd \_ 顯示 \_ 接收 \_ 通知] \_ 結果** 結構描述您可以選擇性地在 [ [**wfd \_ 顯示接收] \_ \_ 通知 \_ 回檔**](wfd-display-sink-notification-callback.md) 函式中處理顯示接收器通知之後設定的結果。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT** structure describes the result that you can optionally set after processing a display sink notfication in the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc4ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="cc4ae-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="cc4ae-106">成員</span><span class="sxs-lookup"><span data-stu-id="cc4ae-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc4ae-107">**標頭**</span><span class="sxs-lookup"><span data-stu-id="cc4ae-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="cc4ae-108">可描述通知結果中所含資料的 [**WFD \_ 顯示 \_ 接收器 \_ 物件 \_ 標頭**](wfd-display-sink-object-header.md) 。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification result.</span></span>

</dd> <dt>

<span data-ttu-id="cc4ae-109">**type**</span><span class="sxs-lookup"><span data-stu-id="cc4ae-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="cc4ae-110">指出通知結果類型的 [ [**WFD \_ 顯示 \_ 接收] \_ 通知 \_ 類型**](wfd-display-sink-notification-type.md) 值。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification result.</span></span> <span data-ttu-id="cc4ae-111">此參數也會決定要在下聯集內使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="cc4ae-112">**ProvisioningData**</span><span class="sxs-lookup"><span data-stu-id="cc4ae-112">**ProvisioningData**</span></span>
</dt> <dd>

<span data-ttu-id="cc4ae-113">布建要求結果的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-113">Info about the result of a provisioning request.</span></span> <span data-ttu-id="cc4ae-114">如果 *類型* 具有值 **ProvisioningRequestNotification**，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-114">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="cc4ae-115">**ConfigMethod**</span><span class="sxs-lookup"><span data-stu-id="cc4ae-115">**ConfigMethod**</span></span>
</dt> <dd>

<span data-ttu-id="cc4ae-116">用於顯示互動式接受之 UI 的方法。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-116">The method for showing UI for interactive acceptance.</span></span>

</dd> <dt>

<span data-ttu-id="cc4ae-117">**uPassKeyLength**</span><span class="sxs-lookup"><span data-stu-id="cc4ae-117">**uPassKeyLength**</span></span>
</dt> <dd>

<span data-ttu-id="cc4ae-118">*密碼* 中的寬字元數，不計入任何 Null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-118">The number of wide characters in *Passkey*, not counting any NULL-terminator.</span></span>

</dd> <dt>

<span data-ttu-id="cc4ae-119">**金鑰**</span><span class="sxs-lookup"><span data-stu-id="cc4ae-119">**Passkey**</span></span>
</dt> <dd>

<span data-ttu-id="cc4ae-120">以寬字元陣列的形式包含傳遞索引鍵。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-120">Contains the pass key as an array of wide characters.</span></span> <span data-ttu-id="cc4ae-121">WFD \_ 接收 \_ WPS \_ 資訊 \_ 最大 \_ 密碼 \_ 長度會定義為 (8) 的值。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-121">WFD\_SINK\_WPS\_INFO\_MAX\_PASSKEY\_LENGTH is defined as the value (8).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cc4ae-122">**ReconnectData**</span><span class="sxs-lookup"><span data-stu-id="cc4ae-122">**ReconnectData**</span></span>
</dt> <dd>

<span data-ttu-id="cc4ae-123">重新連接要求結果的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-123">Info about the result of a reconnect request.</span></span> <span data-ttu-id="cc4ae-124">如果 *類型* 具有值 **ReconnectRequestNotification**，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-124">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="cc4ae-125">**strProfile**</span><span class="sxs-lookup"><span data-stu-id="cc4ae-125">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="cc4ae-126">描述設定檔之以 Null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="cc4ae-126">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc4ae-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc4ae-127">Requirements</span></span>



| <span data-ttu-id="cc4ae-128">需求</span><span class="sxs-lookup"><span data-stu-id="cc4ae-128">Requirement</span></span> | <span data-ttu-id="cc4ae-129">值</span><span class="sxs-lookup"><span data-stu-id="cc4ae-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4ae-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc4ae-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cc4ae-131">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc4ae-131">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cc4ae-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc4ae-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cc4ae-133">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc4ae-133">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cc4ae-134">標頭</span><span class="sxs-lookup"><span data-stu-id="cc4ae-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc4ae-135"><dt>Wfdsink。h</dt></span><span class="sxs-lookup"><span data-stu-id="cc4ae-135"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




