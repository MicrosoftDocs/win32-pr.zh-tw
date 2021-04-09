---
title: 'AllocFixupInfo 函式 (NapUtil) '
description: 為指定大小的 FixupInfo 結構配置記憶體。
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- AllocFixupInfo 函數 NAP
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dffda7e5e44302173ac06e460414455eb19c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843184"
---
# <a name="allocfixupinfo-function"></a>AllocFixupInfo 函式

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**AllocFixupInfo** 函數會為指定大小的 [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo)結構配置記憶體。

## <a name="syntax"></a>語法


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fixupInfo* \[in、out\]
</dt> <dd>

新配置之 [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) 結構的位址指標。

</dd> <dt>

*countResultCodes* \[在\]
</dt> <dd>

要配置給 *fixupInfo* 的結果碼數目。

</dd> </dl>

## <a name="return-value"></a>傳回值



| 傳回碼                                                                                   | Description                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業已順利完成。<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 傳遞了無效的引數。<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 系統的虛擬記憶體不足。 此操作失敗。<br/> |



 

## <a name="remarks"></a>備註

NAP 系統支援的所有 COM 介面都會使用標準 COM 記憶體管理規則和 COM 記憶體配置器 (**CoTaskMemAlloc** 和 **CoTaskMemFree**) ：

-   呼叫端會配置和釋放 **In** 參數。
-   **Out** 參數是由被呼叫端所配置，且由呼叫者使用 **CoTaskMem** 釋放。
-   **In/out** 參數是由呼叫端所配置、由被呼叫端釋出和重新配置，最後由呼叫端釋放，並使用 **CoTaskMem**。

釋放記憶體的所有 NAP 函式也會釋放所有內嵌指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>NapUtil。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FreeFixupInfo**](freefixupinfo-func.md)
</dt> </dl>

 

 





