---
description: GetProps 方法會抓取這個物件上設定的屬性，以及其對應的值。
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'IPropertySetter：： GetProps 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990114"
---
# <a name="ipropertysettergetprops-method"></a>IPropertySetter：： GetProps 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetProps` 這個物件上設定的屬性，以及其對應的值。

## <a name="syntax"></a>語法


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcParams* \[擴展\]
</dt> <dd>

接收 *paParam* 中傳回的結構數目。

</dd> <dt>

*paParam* \[擴展\]
</dt> <dd>

[**DEXTER \_ PARAM**](dexter-param.md)結構陣列的指標位址。

</dd> <dt>

*paValue* \[擴展\]
</dt> <dd>

[**DEXTER \_ 值**](dexter-value.md)結構陣列的指標位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

針對 *paParam* 中傳回的每個屬性， **值成員表示** 與屬性相關聯的 [**DEXTER \_ 值**](dexter-value.md) 結構數目。 針對每個屬性，會以遞增的時間順序傳回配對。

當您完成使用傳回的結構時，請呼叫 [**IPropertySetter：： FreeProps**](ipropertysetter-freeprops.md) 來釋出這個方法所配置的資源。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="examples"></a>範例

下列程式碼範例示範如何逐一查看屬性 setter 實例上的所有值：


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPropertySetter 介面**](ipropertysetter.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




