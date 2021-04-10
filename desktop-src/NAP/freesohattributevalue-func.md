---
title: 'FreeSoHAttributeValue 函式 (NapUtil) '
description: 釋放 SoHAttributeValue 資料結構。
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- FreeSoHAttributeValue 函數 NAP
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd56049eb727554227bd5eb509969f6795670a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025424"
---
# <a name="freesohattributevalue-function"></a>FreeSoHAttributeValue 函式

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**FreeSoHAttributeValue** 函式會釋出 [**SoHAttributeValue**](sohattributevalue-union.md)的資料結構。

## <a name="syntax"></a>語法


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* \[在\]
</dt> <dd>

[**SoHAttributeType**](sohattributetype-enum.md)值，指定要釋放的 SoH 屬性值類型。

</dd> <dt>

*值* \[在\]
</dt> <dd>

要釋放的 [**SoHAttributeValue**](sohattributevalue-union.md) 指標。

</dd> </dl>

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



 

 





