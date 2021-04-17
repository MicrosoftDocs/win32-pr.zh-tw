---
description: 從 BLOB NPP 區段的 NetworkInfo 類別中抓取 MAC 類型，並將類型資料轉換成 MAC 類型號碼。
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: 'GetNPPMacTypeAsNumber 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510973"
---
# <a name="getnppmactypeasnumber-function"></a>GetNPPMacTypeAsNumber 函式

**GetNPPMacTypeAsNumber** 函式會從 BLOB 的 NPP 區段的 NetworkInfo 類別中抓取 mac 類型，並將類型資料轉換成 MAC 類型號碼。

## <a name="syntax"></a>語法


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hBlob* \[在\]
</dt> <dd>

指定之 BLOB 的控制碼。

</dd> <dt>

*lpMacType* \[擴展\]
</dt> <dd>

MAC 型別的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果標記無法使用，則傳回值為 MAC \_ 類型 \_ 未知。

## <a name="remarks"></a>備註

此函式會將標記 **NPP： NetworkInfo： MacType** 對應至 Npptypes .h 檔案中定義的 **MAC \_ 類型 \_ \*** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Npptools .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




