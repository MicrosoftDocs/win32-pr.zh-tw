---
title: sh_pipe 關鍵字
description: '\ Sh \_ pipe \ 關鍵字會指定系統物件是管道的控制碼。'
keywords:
- sh_pipe 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 9f9deab2bf5a751d3b2d5956d4d33a1d5b347e18
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "106981912"
---
# <a name="sh_pipe-keyword"></a>sh \_ pipe 關鍵字

**Sh \_ pipe** 關鍵字會指定 `system_handle` 保留管道的控制碼。

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
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
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
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

[關於管道](../ipc/about-pipes.md)
</dt> <dt>

[檔案安全性與存取權限](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[**CreatePipe** 函式](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[**CreateNamedPipe** 函式](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
