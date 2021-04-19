---
title: sh_semaphore 關鍵字
description: '\ Sh \_ 信號 \ 關鍵字指定系統物件是信號的控制碼。'
keywords:
- sh_semaphore 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2a5c33e4c44b67e3106a48cde244abaf13f41ad5
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "106991383"
---
# <a name="sh_semaphore-keyword"></a>sh \_ 信號關鍵字

**Sh \_ 信號** 關鍵字會指定 `system_handle` 保留信號的控制碼。

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
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
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
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

[信號物件](../sync/semaphore-objects.md)
</dt> <dt>

[同步處理物件安全性和存取權限](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateSemaphore** 函式](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[**CreateSemaphoreEx** 函式](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
