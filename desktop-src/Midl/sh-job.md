---
title: sh_job 關鍵字
description: '\ Sh \_ job \ 關鍵字會指定系統物件是作業的控制碼。'
keywords:
- sh_job 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_job
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: dd71db0310b450db1d9c87879e8ac10ad998d1d21e48a60eb9d816c0a0718b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146281"
---
# <a name="sh_job-keyword"></a>sh \_ job 關鍵字

**Sh \_ job** 關鍵字會指定 `system_handle` 保留作業的控制碼。

``` syntax
[system_handle(sh_job)]

[system_handle(sh_job, access-rights)]
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
    HRESULT SetJob([in, system_handle(sh_job)] HANDLE job);

    HRESULT GetJobForAccounting([out, system_handle(sh_job, JOB_OBJECT_QUERY)] HANDLE* pJob);
}
```

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
|-|-|
| 最低支援的用戶端 | Windows 10年度更新 (版本1607、組建 14393)  |
| 最低支援的伺服器 | Windows Server 2016 (組建 14393)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[工作物件](../procthread/job-objects.md)
</dt> <dt>

[工作物件安全性和存取權限](../procthread/job-object-security-and-access-rights.md)
</dt> <dt>

[**CreateJobObject** 函式](/windows/win32/api/winbase/nf-winbase-createjobobjecta)
</dt> </dl>
