---
title: sh_token 關鍵字
description: '\ Sh \_ token \ 關鍵字指定系統物件是 token 的控制碼。'
keywords:
- sh_token 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_token keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8305a8073d03eb90bbd214f1b56cb1174ffef66953bb170fb7f28ebf1b84d35c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066769"
---
# <a name="sh_token-keyword"></a>sh \_ token 關鍵字

**Sh \_ token** 關鍵字會指定 `system_handle` 保留權杖的控制碼。

``` syntax
[system_handle(sh_token)]

[system_handle(sh_token, access-rights)]
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
    HRESULT SetToken([in, system_handle(sh_token)] HANDLE token);

    HRESULT GetToken([out, system_handle(sh_token, TOKEN_QUERY)] HANDLE* pToken);
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

[存取權杖](../secauthz/access-tokens.md)
</dt> <dt>

[Access-Token 物件的存取權限](../secauthz/access-rights-for-access-token-objects.md)
</dt> </dl>
