---
description: AttachPropertyInstance 函式會將現有的屬性對應到可辨識資料中的特定位置。
ms.assetid: b44cf8d1-939b-45da-8a9a-b4bdcf9faf43
title: 'AttachPropertyInstance 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c4d726b7500fd890dfe8c7fdc39f628c185dbe35f3a3bc14f0c05ab7f85cd673
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744678"
---
# <a name="attachpropertyinstance-function"></a>AttachPropertyInstance 函式

**AttachPropertyInstance** 函式會將現有的屬性對應到可辨識資料中的特定位置。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI AttachPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

要剖析之框架的控制碼。 在 [**AttachProperties**](attachproperties.md)函數的 *hFrame* 參數中，使用傳遞至剖析器 DLL 的控制碼。

</dd> <dt>

*hProperty* \[在\]
</dt> <dd>

定義屬性之 [**PROPERTYINFO**](propertyinfo.md) 結構的控制碼。 當您執行 [**Register**](register-parser.md) export 函式時，您會指定定義屬性的 **PROPERTYINFO** 結構。

</dd> <dt>

*長度* \[在\]
</dt> <dd>

這個屬性實例的資料長度。

</dd> <dt>

*lpData* \[在\]
</dt> <dd>

可辨識的資料中，屬性值所在位置的指標。 在 [**AttachProperties**](attachproperties.md)函數的 *lpProtocol* 參數中，使用傳遞至剖析器 DLL 的指標。

</dd> <dt>

*H* \[在\]
</dt> <dd>

識別碼 (從0到 2047) 用來設定屬性的即時線上說明。

識別碼是相對於與通訊協定 [*屬性資料庫*](p.md)相關聯的說明檔。

</dd> <dt>

*IndentLevel* \[在\]
</dt> <dd>

縮排層級 (從0到 15) 用來以階層方式顯示內容。

網路監視器使用層級0到14來縮排屬性。 層級15是特殊值，可讓剖析器附加不可見的隱藏屬性。

</dd> <dt>

*IFlags* \[在\]
</dt> <dd>

位域值，指出位在屬性中的順序。 將 *fError* 設定為0或1的先前剖析器，現在應該將 *FERROR* 設定為 IFLAG \_ 錯誤。 將此參數設定為下列其中一個值。



| 值                                                                                                                                                         | 意義                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**IFLAG \_ 錯誤**</dt> </dl>       | 框架中的資料發生錯誤。<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ 交換**</dt> </dl> | 在附加時， **文字** 位元組是非 Intel 格式。<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ UNICODE**</dt> </dl> | 在附加時間， **字串** 是 Unicode。<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

**AttachPropertyInstance** 函式會在 [**AttachProperties**](attachproperties.md)匯出函數的執行期間呼叫。 當屬性附加至資料時，網路監視器會建立 [**PROPERTYINST**](propertyinst.md) 結構，以定義附加屬性的實例。

在 [**AttachProperties**](attachproperties.md)的執行期間，呼叫 **AttachPropertyInstance** 以使用存在於捕捉中的資料。 您也可以呼叫 [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) 函數來修改屬性資料。 不過，建議您使用存在於捕捉中的資料。



| 的相關資訊                                        | 請參閱                                                                |
|-----------------------------------------------------------|--------------------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。 | [**解析 器**](parsers.md)                                         |
| 如何呼叫 **AttachPropertyInstance**。                   | [執行 AttachProperties](implementing-attachproperties.md) |



 

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

[**AttachProperties**](attachproperties.md)
</dt> <dt>

[**AttachPropertyInstanceEx**](attachpropertyinstanceex.md)
</dt> <dt>

[**PROPERTYINST**](propertyinst.md)
</dt> </dl>

 

 




