---
description: 取得 TCP v6 驅動程式物件的參考。
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: ReferenceTcpDriverV6 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: d0a3f56ea59eb753dc7a49d6f6b1d0c48be8abca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996047"
---
# <a name="referencetcpdriverv6-function"></a>ReferenceTcpDriverV6 函式

取得 TCP v6 驅動程式物件的參考。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
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

這個函式會在可供下載的 Drvref 中執行。 請參閱 [Windows 網路驅動程式參考 API 程式庫](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Drvref .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ReferenceTcpDriver**](referencetcpdriver.md)
</dt> </dl>

 

 




