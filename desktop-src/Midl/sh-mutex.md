---
title: sh_mutex 關鍵字
description: '\ Sh \_ mutex \ 關鍵字會指定系統物件是 mutex 的控制碼。'
keywords:
- sh_mutex 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106989134"
---
# <a name="sh_mutex-keyword"></a>sh \_ mutex 關鍵字

**Sh \_ mutex** 關鍵字會指定 `system_handle` 保留 mutex 的控制碼。

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
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
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
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

[Mutex 物件](../sync/mutex-objects.md)
</dt> <dt>

[同步處理物件安全性和存取權限](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateMutex** 函式](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[**CreateMutexEx** 函式](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>