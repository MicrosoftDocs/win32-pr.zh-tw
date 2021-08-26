---
description: 抓取系統目前載入之模組集的相關資訊。
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: 'AuxKlibQueryModuleInformation function (Aux \_ klib .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: be734583c8b7d02be4c498bc75069a0c813565d48aea3db3826712d6375e72b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045308"
---
# <a name="auxklibquerymoduleinformation-function"></a>AuxKlibQueryModuleInformation 函式

抓取系統目前載入之模組集的相關資訊。

## <a name="syntax"></a>語法


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*BufferSize* \[in、out\]
</dt> <dd>

在輸入時， *QueryInfo* 緩衝區的大小（以位元組為單位）。 在輸出時，會接收實際所需的大小。 由於系統模組清單可以在呼叫之間變更，因此此值也可以在呼叫之間變更。

</dd> <dt>

*ElementSize* \[在\]
</dt> <dd>

陣列元素的大小（以位元組為單位）。 此大小會決定輸出的格式。

</dd> <dt>

*QueryInfo* \[out、optional\]
</dt> <dd>

接收模組資訊的緩衝區指標。 這項資訊會在陣列中傳回，而陣列的元素是下列其中一個結構： [**AUX \_ module \_ 基本 \_ 資訊**](aux-module-basic-info-struct.md) 或 [**aux \_ 模組 \_ 延伸 \_ 資訊**](aux-module-extended-info-struct.md)。 使用的特定結構取決於指定的元素大小。

如果此參數為 **Null**，則函式會傳回所需的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「狀態 \_ 成功」。

如果函式失敗，則傳回值可以是在 WDK 中定義的其中一個狀態碼，也就是在 WDK 中可用。

## <a name="remarks"></a>備註

呼叫此函式之前，您必須先呼叫 [**AuxKlibInitialize**](auxklibinitialize-func.md) 函數。

您可以從 [這裡](https://www.microsoft.com/?ref=go)下載可執行此 API 的物件程式庫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|------------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows輔助 API 程式庫1.0 版或更新版本<br/>                            |
| 標頭<br/>          | <dl> <dt>Aux \_ klib。h</dt> </dl>   |
| 程式庫<br/>         | <dl> <dt>Aux \_ klib .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AuxKlibInitialize**](auxklibinitialize-func.md)
</dt> <dt>

[**AUX \_ 模組 \_ 基本 \_ 資訊**](aux-module-basic-info-struct.md)
</dt> <dt>

[**AUX \_ 模組 \_ 擴充 \_ 資訊**](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




