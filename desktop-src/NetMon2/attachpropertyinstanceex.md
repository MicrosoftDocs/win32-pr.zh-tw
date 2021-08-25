---
description: AttachPropertyInstanceEx 函式會將現有的屬性對應至已辨識資料中的特定位置，並修改屬性資料的值。
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: 'AttachPropertyInstanceEx 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ec0b874d55d149c9d049b8c6b2cafd716fe82c66410e2d3e1550b397c366
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911278"
---
# <a name="attachpropertyinstanceex-function"></a>AttachPropertyInstanceEx 函式

**AttachPropertyInstanceEx** 函式會將現有的屬性對應至已辨識資料中的特定位置，並修改屬性資料的值。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
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

*LengthEx* \[在\]
</dt> <dd>

擴充資料長度的長度（以位元組為單位）。

</dd> <dt>

*lpDataEx* \[在\]
</dt> <dd>

擴充資料的指標，通常是包含擴充資料的堆疊變數。

</dd> <dt>

*H* \[在\]
</dt> <dd>

識別碼 (從0到 2047) 用來設定屬性的即時線上說明。

*H* 號碼相對於與通訊協定 [*屬性資料庫*](p.md)相關聯的說明檔。

</dd> <dt>

*IndentLevel* \[在\]
</dt> <dd>

縮排層級 (從0到 15) 用來以階層方式顯示內容。

網路監視器使用層級0到9。 層級15是特殊值，可讓剖析器附加不可見的隱藏屬性。

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

**AttachPropertyInstanceEx** 函式會在 [**AttachProperties**](attachproperties.md)匯出函數的執行期間呼叫。 使用 AttachPropertyInstanceEx 將屬性附加至資料時，網路監視器會建立 [**PROPERTYINST**](propertyinst.md) 結構，以定義附加屬性的實例，以及定義擴充資料的 [**PROPERTYINSTEX**](propertyinstex.md) 結構。

如果呼叫 **AttachPropertyInstanceEx** ，但未提供任何擴充資料， *LpDataEx* 參數為 **Null** 或 *LengthEx* 參數為0，則 **AttachPropertyInstanceEx** 呼叫的功能相當於 [**AttachPropertyInstance**](attachpropertyinstance.md) 呼叫。

在 [**AttachProperties**](attachproperties.md)的執行期間，呼叫 [**AttachPropertyInstance**](attachpropertyinstance.md) 以使用存在於捕捉中的資料。 您也可以呼叫 **AttachPropertyInstanceEx** 函數來修改屬性資料。 不過，建議您使用存在於捕捉中的資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




