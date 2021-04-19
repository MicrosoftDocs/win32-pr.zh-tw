---
description: 使用網路監視器提供的一般格式器來格式化屬性實例資料。
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: 'FormatPropertyInstance 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972597"
---
# <a name="formatpropertyinstance-function"></a>FormatPropertyInstance 函式

**FormatPropertyInstance** 函式會使用網路監視器提供的一般格式器來格式化屬性實例資料。

## <a name="syntax"></a>語法


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpPropertyInst* \[in、out\]
</dt> <dd>

包含實例資料之 [PROPERTYINST](propertyinst.md) 結構的指標。

在輸入時，泛型格式器會採用其中一個 **PROPERTYINST** 聯集成員的實例資料，並將該資料轉換成預先定義的格式化字串。

在輸出中，一般格式器會將 **PROPERTYINST** 結構的 **szPropertyText** 成員設定為格式化字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值是 NMerr 中的錯誤碼。

## <a name="remarks"></a>備註

當需要一般格式器來格式化資料以在網路監視器 UI 的詳細資料窗格中顯示時，剖析器 DLL 會間接呼叫 **FormatPropertyInstance** 函數。 當您定義屬性時，若要呼叫 **FormatPropertyInstance** ，請在 [PROPERTYINFO](propertyinfo.md)結構的 **InstanceData** 成員中指定它。

> [!Note]  
> 剖析器無法辨識當它必須格式化屬性的實例時，所呼叫的函式。 函式可以是 **FormatPropertyInstance** ，也可以是剖析器定義的自訂格式函數。 剖析器會呼叫屬性之 **PROPERTYINFO** 結構的 **InstanceData** 成員所指定的任何格式函數。

 

如需如何執行 [formatproperties](formatproperties.md)的詳細資訊和範例，請參閱 [執行 formatproperties](implementing-formatproperties.md)。 如需一般格式器如何格式化不同資料類型的詳細資訊，請參閱一般格式器 [輸出](generic-formatter-output.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




