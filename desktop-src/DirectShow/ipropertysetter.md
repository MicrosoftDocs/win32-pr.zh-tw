---
description: IPropertySetter 介面會設定 DirectShow 編輯服務 (DES) 效果或轉換的屬性。若要使用這個介面，請 (CLSID PropertySetter) 建立屬性 setter 物件的實例 \_ ，然後呼叫 IAMTimelineObj：： SetPropertySetter 方法，將它與效果或轉換產生關聯。 如需詳細資訊，請參閱使用效果和轉換。應用程式通常只需要呼叫 IPropertySetter：： ClearProps 方法來清除現有的屬性，並使用 IPropertySetter：： AddProp 方法來加入新的屬性。 其他 DES 元件會呼叫此介面上的其他方法。
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: 'IPropertySetter 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990684"
---
# <a name="ipropertysetter-interface"></a>IPropertySetter 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IPropertySetter`介面會設定[DirectShow 編輯服務](directshow-editing-services.md) (DES) 效果或轉換的屬性。

若要使用這個介面，請 (CLSID PropertySetter) 建立屬性 setter 物件的實例 \_ ，然後呼叫 [**IAMTimelineObj：： SetPropertySetter**](iamtimelineobj-setpropertysetter.md) 方法，將它與效果或轉換產生關聯。 如需詳細資訊，請參閱 [使用效果和轉換](working-with-effects-and-transitions.md)。

通常，應用程式只需要呼叫 [**IPropertySetter：： ClearProps**](ipropertysetter-clearprops.md) 方法來清除現有的屬性，並使用 [**IPropertySetter：： AddProp**](ipropertysetter-addprop.md) 方法來加入新的屬性。 其他 DES 元件會呼叫此介面上的其他方法。

## <a name="members"></a>成員

**IPropertySetter** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IPropertySetter** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IPropertySetter** 介面具有這些方法。



| 方法                                               | 描述                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddProp**](ipropertysetter-addprop.md)           | 將屬性加入至屬性 setter，以及定義時間範圍內屬性值的時間值配對陣列。<br/> |
| [**ClearProps**](ipropertysetter-clearprops.md)     | 清除屬性 setter 中的所有屬性資料。<br/>                                                                                 |
| [**CloneProps**](ipropertysetter-cloneprops.md)     | 從這個屬性 setter 複製一組屬性，並將其加入至新的屬性 setter。<br/>                                       |
| [**FreeProps**](ipropertysetter-freeprops.md)       | 釋放 [**IPropertySetter：： GetProps**](ipropertysetter-getprops.md) 方法所配置的資源。<br/>                             |
| [**GetProps**](ipropertysetter-getprops.md)         | 抓取這個物件上設定的屬性，以及其對應的值。<br/>                                                      |
| [**LoadFromBlob**](ipropertysetter-loadfromblob.md) | 從持續性格式載入屬性資料。<br/>                                                                                     |
| [**LoadXML**](ipropertysetter-loadxml.md)           | 載入以可延伸標記語言 (XML)  (XML) 表示的屬性資料。<br/>                                                                 |
| [**PrintXML**](ipropertysetter-printxml.md)         | 將屬性資料轉換成 XML 字串。<br/>                                                                                         |
| [**SaveToBlob**](ipropertysetter-savetoblob.md)     | 將屬性資料儲存至保存格式。<br/>                                                                                   |
| [**SetProps**](ipropertysetter-setprops.md)         | 將目標物件的屬性設定為指定時間的適當狀態。<br/>                                          |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
