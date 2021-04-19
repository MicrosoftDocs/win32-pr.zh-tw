---
title: sh_event 關鍵字
description: '\ Sh \_ 事件 \ 關鍵字指定系統物件是事件的控制碼。'
keywords:
- sh_event 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1a9b6dc7cc9dc4de4abd5dcc88a53588167db59d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "106985790"
---
# <a name="sh_event-keyword"></a>sh \_ 事件關鍵字

**Sh \_ 事件** 關鍵字會指定 `system_handle` 保留事件的控制碼。

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
```

## <a name="parameters"></a>參數

這個關鍵字是 [**system_handle**](system-handle.md)的參數。

[**System_handle**](system-handle.md)檔也包含選擇性使用 *存取權限* 參數的詳細資料。 預設行為是 `DUPLICATE_SAME_ACCESS` 根據 [ **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)函式規格。

## <a name="remarks"></a>備註

若要使用這個關鍵字搭配 `system_handle` 屬性，在執行 `-target` midl.exe 時，旗標必須設定為 `NT100` (或更高的) 。

## <a name="examples"></a>範例

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
}
```

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
|-|-|
| 最低支援的用戶端 | Windows 10 年度更新版 (1607 版、組建 14393)  |
| 最低支援的伺服器 | Windows Server 2016 (build 14393)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[事件物件](../sync/event-objects.md)
</dt> <dt>

[同步處理物件安全性和存取權限](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateEvent** 函數](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**CreateEventEx** 函式](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
