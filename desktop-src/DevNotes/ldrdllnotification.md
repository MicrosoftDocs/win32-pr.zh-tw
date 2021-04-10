---
description: 使用 LdrRegisterDllNotification 函式指定的通知回呼函數。
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: LdrDllNotification 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846991"
---
# <a name="ldrdllnotification-callback-function"></a><span data-ttu-id="85a84-103">LdrDllNotification 回呼函式</span><span class="sxs-lookup"><span data-stu-id="85a84-103">LdrDllNotification callback function</span></span>

<span data-ttu-id="85a84-104">\[您可以在不另行通知的情況下，從 Windows 變更或移除此功能。\]</span><span class="sxs-lookup"><span data-stu-id="85a84-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="85a84-105">使用 [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) 函式指定的通知回呼函數。</span><span class="sxs-lookup"><span data-stu-id="85a84-105">A notification callback function specified with the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span> <span data-ttu-id="85a84-106">第一次載入 DLL 時，載入器會呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="85a84-106">The loader calls this function when a DLL is first loaded.</span></span>

<span data-ttu-id="85a84-107">**警告：** 通知回呼函數在任何 DLL 中呼叫函式是不安全的。</span><span class="sxs-lookup"><span data-stu-id="85a84-107">**Warning:** It is unsafe for the notification callback function to call functions in any DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a84-108">語法</span><span class="sxs-lookup"><span data-stu-id="85a84-108">Syntax</span></span>


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a><span data-ttu-id="85a84-109">參數</span><span class="sxs-lookup"><span data-stu-id="85a84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85a84-110">*NotificationReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85a84-110">*NotificationReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a84-111">呼叫通知回呼函數的原因。</span><span class="sxs-lookup"><span data-stu-id="85a84-111">The reason that the notification callback function was called.</span></span> <span data-ttu-id="85a84-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="85a84-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="85a84-113">值</span><span class="sxs-lookup"><span data-stu-id="85a84-113">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="85a84-114">意義</span><span class="sxs-lookup"><span data-stu-id="85a84-114">Meaning</span></span>                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <span data-ttu-id="85a84-115"><dt>**LDR \_DLL \_ 通知 \_ 原因已 \_ 載入**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="85a84-115"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_LOADED**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="85a84-116">已載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="85a84-116">The DLL was loaded.</span></span> <span data-ttu-id="85a84-117">*NotificationData* 參數指向 **LDR \_ DLL \_ 載入的 \_ 通知 \_ 資料** 結構。</span><span class="sxs-lookup"><span data-stu-id="85a84-117">The *NotificationData* parameter points to an **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <span data-ttu-id="85a84-118"><dt>**LDR \_DLL \_ 通知 \_ 原因 \_**</dt>已卸載 <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="85a84-118"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_UNLOADED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="85a84-119">DLL 已卸載。</span><span class="sxs-lookup"><span data-stu-id="85a84-119">The DLL was unloaded.</span></span> <span data-ttu-id="85a84-120">*NotificationData* 參數指向 **LDR DLL 卸載的 \_ \_ \_ 通知 \_ 資料** 結構。</span><span class="sxs-lookup"><span data-stu-id="85a84-120">The *NotificationData* parameter points to an **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="85a84-121">*NotificationData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85a84-121">*NotificationData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a84-122">常數 **LDR \_ DLL \_ 通知** 聯集的指標，其中包含通知資料。</span><span class="sxs-lookup"><span data-stu-id="85a84-122">A pointer to a constant **LDR\_DLL\_NOTIFICATION** union that contains notification data.</span></span> <span data-ttu-id="85a84-123">這個聯集具有下列定義：</span><span class="sxs-lookup"><span data-stu-id="85a84-123">This union has the following definition:</span></span>

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

<span data-ttu-id="85a84-124">**LDR \_ DLL 載入 \_ 的 \_ 通知 \_ 資料** 結構具有下列定義：</span><span class="sxs-lookup"><span data-stu-id="85a84-124">The **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

<span data-ttu-id="85a84-125">**LDR DLL 卸載的 \_ \_ \_ 通知 \_ 資料** 結構具有下列定義：</span><span class="sxs-lookup"><span data-stu-id="85a84-125">The **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

<span data-ttu-id="85a84-126">*內容* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="85a84-126">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85a84-127">回呼函數的內容資料指標。</span><span class="sxs-lookup"><span data-stu-id="85a84-127">A pointer to context data for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85a84-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="85a84-128">Return value</span></span>

<span data-ttu-id="85a84-129">這個回呼函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="85a84-129">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85a84-130">備註</span><span class="sxs-lookup"><span data-stu-id="85a84-130">Remarks</span></span>

<span data-ttu-id="85a84-131">在動態連結發生之前，會呼叫通知回呼函式。</span><span class="sxs-lookup"><span data-stu-id="85a84-131">The notification callback function is called before dynamic linking takes place.</span></span>

## <a name="requirements"></a><span data-ttu-id="85a84-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="85a84-132">Requirements</span></span>



| <span data-ttu-id="85a84-133">需求</span><span class="sxs-lookup"><span data-stu-id="85a84-133">Requirement</span></span> | <span data-ttu-id="85a84-134">值</span><span class="sxs-lookup"><span data-stu-id="85a84-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85a84-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85a84-135">Minimum supported client</span></span><br/> | <span data-ttu-id="85a84-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85a84-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="85a84-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85a84-137">Minimum supported server</span></span><br/> | <span data-ttu-id="85a84-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85a84-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85a84-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85a84-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85a84-140">**LdrRegisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="85a84-140">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> <dt>

[<span data-ttu-id="85a84-141">**LdrUnregisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="85a84-141">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




