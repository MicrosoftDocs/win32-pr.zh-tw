---
description: IPortableDeviceValues 介面會保存一組 PROPERTYKEY/PROPVARIANT 配對。
ms.assetid: a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f
title: 'IPortableDeviceValues 介面 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ecdfd91c9ea4ab5202a72015f579d560b37fbffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988653"
---
# <a name="iportabledevicevalues-interface"></a>IPortableDeviceValues 介面

**IPortableDeviceValues** 介面會保存 **PROPERTYKEY** / **PROPVARIANT** 配對的集合。 集合中的值不需要是相同的 VARTYPE。

值會儲存為索引鍵/值組;集合中的每個索引鍵都必須是唯一的。 用戶端可以依 **PROPERTYKEY** 或以零為基底的索引來搜尋專案。 資料值會儲存為 **PROPVARIANT** 結構。 您可以使用泛型方法 **SetValue** 和 **GetValue** 來新增或抓取任何類型的值，或使用所加入之資料類型的特定方法來加入專案。

**Get ...** 方法需要呼叫者適當地釋放任何抓取的值。 **Set ...** 方法會將值複製到集合中。

釋放 **IPortableDeviceValues** 介面時，它會呼叫 **Clear**，以釋出已適當配置給其所有成員的記憶體。

您可以從方法中取出這個介面，或者，如果需要新的物件，請使用 **CLSID \_ PortableDeviceValues** 呼叫 **CoCreate** 。

## <a name="members"></a>成員

**IPortableDeviceValues** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IPortableDeviceValues** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IPortableDeviceValues** 介面具有這些方法。



| 方法                                                                                                                     | 描述                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**清楚**](iportabledevicevalues-clear.md)                                                                               | 刪除集合中的所有專案。<br/>                                                                      |
| [**CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)                                   | 將 **IPropertyStore** 的內容複寫到集合中。<br/>                                           |
| [**CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)                                       | 將集合中的所有值複製到 **IPropertyStore** 介面。<br/>                               |
| [**GetAt**](iportabledevicevalues-getat.md)                                                                               | 使用提供的以零為基底的索引，從集合中抓取值。<br/>                                  |
| [**GetBoolValue**](iportabledevicevalues-getboolvalue.md)                                                                 | 抓取 (型別 VT \_ bool) 由索引鍵指定的布林值。<br/>                                              |
| [**GetBufferValue**](iportabledevicevalues-getbuffervalue.md)                                                             | 抓取位元組陣列值， (類型 \_ 由索引鍵指定的 vt 向量 \| VT \_ UI1) 。<br/>                               |
| [**GetCount**](iportabledevicevalues-getcount.md)                                                                         | 抓取集合中的專案數。<br/>                                                            |
| [**GetErrorValue**](iportabledevicevalues-geterrorvalue.md)                                                               | 抓取 (型別 VT \_ 錯誤) 由索引鍵指定的 HRESULT 值。<br/>                                         |
| [**GetFloatValue**](iportabledevicevalues-getfloatvalue.md)                                                               | 抓取 (型別為 VT 的 **FLOAT** 值 \_) 由索引鍵指定。<br/>                                               |
| [**GetGuidValue**](iportabledevicevalues-getguidvalue.md)                                                                 | 以索引鍵指定的 (型別 VT \_ CLSID) 來抓取 GUID 值。<br/>                                             |
| [**GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)                 | 抓取 **IPortableDeviceKeyCollection** 值， (輸入 \_ 由索引鍵指定的 VT 未知) 。<br/>                  |
| [**GetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md) | 抓取 **IPortableDevicePropVariantCollection** 值， (輸入 \_ 由索引鍵指定的 VT 未知) 。<br/>          |
| [**GetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)           | 抓取 **IPortableDeviceValuesCollection** 值， (輸入 \_ 由索引鍵指定的 VT 未知) 。<br/>               |
| [**GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md)                               | 抓取 **IPortableDeviceValues** 值， (輸入 \_ 由索引鍵指定的 VT 未知) 。<br/>                         |
| [**GetIUnknownValue**](iportabledevicevalues-getiunknownvalue.md)                                                         | 抓取 **IUnknown** 介面值， (類型 \_ 由金鑰指定的 VT 未知) 。<br/>                            |
| [**GetKeyValue**](iportabledevicevalues-getkeyvalue.md)                                                                   | 抓取索引鍵所指定的 **PROPERTYKEY** 值。<br/>                                                       |
| [**GetSignedIntegerValue**](iportabledevicevalues-getsignedintegervalue.md)                                               | 抓取索引鍵指定的 **LONG** 值 (type VT \_ I4) 。<br/>                                                |
| [**GetSignedLargeIntegerValue**](iportabledevicevalues-getsignedlargeintegervalue.md)                                     | 抓取索引鍵所指定的 **LONGLONG** 值 (type VT \_ I8) 。<br/>                                            |
| [**GetStringValue**](iportabledevicevalues-getstringvalue.md)                                                             | 抓取索引鍵 (type VT LPWSTR) 的字串值 \_ 。<br/>                                              |
| [**GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)                                           | 抓取由索引鍵指定的 (類型 VT UI4) 的 **ULONG** 值 \_ 。<br/>                                              |
| [**GetUnsignedLargeIntegerValue**](iportabledevicevalues-getunsignedlargeintegervalue.md)                                 | 抓取索引鍵所指定的 **ULONGLONG** 值 (type VT \_ UI8) 。<br/>                                          |
| [**GetValue**](iportabledevicevalues-getvalue.md)                                                                         | 抓取索引鍵所指定的 **PROPVARIANT** 值。<br/>                                                       |
| [**RemoveValue**](iportabledevicevalues-removevalue.md)                                                                   | 從集合中移除項目。<br/>                                                                        |
| [**SetBoolValue**](iportabledevicevalues-setboolvalue.md)                                                                 | 將新的 **布林** 值新增 (型別 VT \_ BOOL) 或覆寫現有的布林值。<br/>                                 |
| [**SetBufferValue**](iportabledevicevalues-setbuffervalue.md)                                                             | 將新的 **位元組** \* 值新增 (類型 VT \_ 向量 \| VT \_ UI1) 或覆寫現有的位元組值。<br/>                     |
| [**SetErrorValue**](iportabledevicevalues-seterrorvalue.md)                                                               | 新增 **HRESULT** 值 (type VT \_ ERROR) 或覆寫現有的值。<br/>                                |
| [**SetFloatValue**](iportabledevicevalues-setfloatvalue.md)                                                               | 將新的 **FLOAT** 值新增 (類型 VT \_ R4) 或覆寫現有的值。<br/>                                     |
| [**SetGuidValue**](iportabledevicevalues-setguidvalue.md)                                                                 | 將新的 **GUID** 值 (類型的 VT \_ CLSID) 或覆寫現有的。<br/>                                   |
| [**SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)                 | 將新的 **IPortableDeviceKeyCollectionValue** 值新增 (類型 VT \_ 未知) 或覆寫現有的值。<br/>    |
| [**SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md) | 將新的 **IPortableDevicePropVariantCollection** 值新增 (類型 VT \_ 未知) 或覆寫現有的值。<br/> |
| [**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)           | 將新的 **IPortableDeviceValuesCollection** 值新增 (類型 VT \_ 未知) 或覆寫現有的值。<br/>      |
| [**SetIPortableDeviceValuesValue**](iportabledevicevalues-setiportabledevicevaluesvalue.md)                               | 將新的 **IPortableDeviceValues** 值新增 (類型 VT \_ 未知) 或覆寫現有的值。<br/>                |
| [**SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)                                                         | 加入新的 **IUnknown** 值 (類型 VT \_ 未知) 或覆寫現有的值。<br/>                             |
| [**SetKeyValue**](iportabledevicevalues-setkeyvalue.md)                                                                   | 新增 **PROPERTYKEY** ， (類型 VT \_ 未知) 值或覆寫現有的值。<br/>                          |
| [**SetSignedIntegerValue**](iportabledevicevalues-setsignedintegervalue.md)                                               | 將新的 **LONG** 值新增 (type VT \_ I4) 或覆寫現有的值。<br/>                                      |
| [**SetSignedLargeIntegerValue**](iportabledevicevalues-setsignedlargeintegervalue.md)                                     | 將新的 **LONGLONG** 值新增 (型別 VT \_ I8) 或覆寫現有的值。<br/>                                  |
| [**SetStringValue**](iportabledevicevalues-setstringvalue.md)                                                             | 新增字串值 (type VT \_ LPWSTR) 或覆寫現有的字串值。<br/>                                    |
| [**SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)                                           | 將新的 **ULONG** 值新增 (type VT \_ UI4) 或覆寫現有的值。<br/>                                    |
| [**SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)                                 | 將新的 **ULONGLONG** 值新增 (型別 VT \_ UI8) 或覆寫現有的值。<br/>                                |
| [**SetValue**](iportabledevicevalues-setvalue.md)                                                                         | 加入新的 **PROPVARIANT** 值，或覆寫現有值。<br/>                                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**集合介面**](collection-interfaces.md)
</dt> </dl>

 

