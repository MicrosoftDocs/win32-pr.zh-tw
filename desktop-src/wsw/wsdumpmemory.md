---
title: 'WsDumpMemory 函式 (WebServicesDebug) '
description: 此函數會將所有記憶體配置傾印到主控台。
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- 適用于 Windows 的 WsDumpMemory 函式 Web 服務
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934850"
---
# <a name="wsdumpmemory-function"></a>WsDumpMemory 函式

此函數會將所有記憶體配置傾印到主控台。

> [!Note]  
> 此函式僅適用于 DEBUG。

 

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*錯誤* \[在中，選擇性\]
</dt> <dd>

[WS \_ ERROR](ws-error.md)物件的指標，如果函式失敗，則應儲存錯誤的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>WebServicesDebug。h</dt> </dl> |



 

 





