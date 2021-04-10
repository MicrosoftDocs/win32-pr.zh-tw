---
description: 開啟列印票證提供者的實例。
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: BindPTProviderThunk 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192608"
---
# <a name="bindptproviderthunk-function"></a>BindPTProviderThunk 函式

\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。 [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) 會提供對等的功能，因此應該改用。\]

開啟列印票證提供者的實例。

## <a name="syntax"></a>語法


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszPrinterName* \[在\]
</dt> <dd>

列印佇列的完整名稱。

</dd> <dt>

*odata-maxversion* \[在\]
</dt> <dd>

呼叫端所支援的最新 [列印架構](./printschema.md) 版本。

</dd> <dt>

*prefVersion* \[在\]
</dt> <dd>

呼叫端所要求的 [列印架構](./printschema.md) 版本。

</dd> <dt>

*phProvider* \[擴展\]
</dt> <dd>

指向列印票證提供者之控制碼的指標。

</dd> <dt>

*usedVersion* \[擴展\]
</dt> <dd>

列印票證提供者將使用的 [列印架構](./printschema.md) 版本。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 **S \_ OK**，否則會傳回 **HRESULT** 錯誤碼。 如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。

## <a name="remarks"></a>備註

呼叫此函式之前，呼叫的執行緒必須呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)來初始化 COM。

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

[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

