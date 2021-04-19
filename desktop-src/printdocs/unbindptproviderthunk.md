---
description: 關閉列印票證提供者的控制碼。
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: UnbindPTProviderThunk 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977895"
---
# <a name="unbindptproviderthunk-function"></a>UnbindPTProviderThunk 函式

\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。 [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) 會提供對等的功能，因此應該改用。\]

關閉列印票證提供者的控制碼。

## <a name="syntax"></a>語法


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProvider* \[在\]
</dt> <dd>

開啟的列印票證提供者的控制碼。 [**BindPTProviderThunk**](bindptproviderthunk.md)函數會傳回這個控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 **S \_ OK**，否則會傳回 **HRESULT** 錯誤碼。 如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印架構](./printschema.md)
</dt> <dt>

[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

