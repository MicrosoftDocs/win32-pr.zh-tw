---
description: 取得 TCP v4 驅動程式物件的參考。
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: ReferenceTcpDriver 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 36329ecb695c6fcc011f7e1fe4f44a149fbeac48b0125c34330b9bde51342f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690838"
---
# <a name="referencetcpdriver-function"></a>ReferenceTcpDriver 函式

取得 TCP v4 驅動程式物件的參考。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDriverObject* \[擴展\]
</dt> <dd>

**驅動程式 \_ 物件** 結構的指標。 如需詳細資訊，請參閱 WDK 的檔。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回 **狀態 \_ 成功**。 如果失敗，則會傳回適當的狀態碼。

## <a name="remarks"></a>備註

您只能從核心模式呼叫此函式。 呼叫端必須在物件完成時呼叫 **ObDereferenceObject** 函式，以遞減參考計數。

這個函式會在可供下載的 Drvref 中執行。 請參閱[Windows 網路驅動程式參考 API 程式庫](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Drvref .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ReferenceTcpDriverV6**](referencetcpdriverv6.md)
</dt> </dl>

 

 




