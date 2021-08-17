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
ms.openlocfilehash: e1e9bea21cd4e21ca7549ce34343b42c50b293471e69576d7c1164f92a371c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004103"
---
# <a name="ldrdllnotification-callback-function"></a>LdrDllNotification 回呼函式

\[您可以從 Windows 中變更或移除此函式，而不需另行通知。\]

使用 [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) 函式指定的通知回呼函數。 第一次載入 DLL 時，載入器會呼叫這個函數。

**警告：** 通知回呼函數在任何 DLL 中呼叫函式是不安全的。

## <a name="syntax"></a>語法


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NotificationReason* \[在\]
</dt> <dd>

呼叫通知回呼函數的原因。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                                                                        | 意義                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <dt>**LDR \_DLL \_ 通知 \_ 原因已 \_ 載入**</dt> <dt>1</dt> </dl>       | 已載入 DLL。 *NotificationData* 參數指向 **LDR \_ DLL \_ 載入的 \_ 通知 \_ 資料** 結構。 <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <dt>**LDR \_DLL \_ 通知 \_ 原因 \_**</dt>已卸載 <dt>2</dt> </dl> | DLL 已卸載。 *NotificationData* 參數指向 **LDR DLL 卸載的 \_ \_ \_ 通知 \_ 資料** 結構。 <br/> |



 

</dd> <dt>

*NotificationData* \[在\]
</dt> <dd>

常數 **LDR \_ DLL \_ 通知** 聯集的指標，其中包含通知資料。 這個聯集具有下列定義：

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

**LDR \_ DLL 載入 \_ 的 \_ 通知 \_ 資料** 結構具有下列定義：

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

**LDR DLL 卸載的 \_ \_ \_ 通知 \_ 資料** 結構具有下列定義：

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

*內容* \[在中，選擇性\]
</dt> <dd>

回呼函數的內容資料指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個回呼函式不會傳回值。

## <a name="remarks"></a>備註

在動態連結發生之前，會呼叫通知回呼函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




