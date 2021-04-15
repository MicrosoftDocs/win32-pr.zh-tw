---
description: IKsPropertySet 介面最初是設計為在 WDM 驅動程式上設定和抓取裝置屬性的有效方式，使用 KSProxy 將使用者模式 COM 方法呼叫轉譯為 WDM 串流類別驅動程式所使用的核心模式屬性集。 這個介面現在也用來嚴格傳遞軟體元件之間的資訊。在某些情況下，軟體元件必須執行此介面，否則 IKsControl 介面 (記載于 DirectShow DDK) 中。 例如，如果您要撰寫軟體 MPEG-2 解碼器以與 DVD 導覽器搭配使用，您必須執行這些介面的其中一個，也支援導覽器將傳送至該解碼器的 DVD 相關屬性集。 Pin 可能會支援其中一個介面，以允許其他 pin 或篩選器設定或抓取其屬性。請注意，此名稱的另一個介面存在於 dsound .h 標頭檔中。 這兩個介面不相容。 IKsControl 介面（記載于 DirectShow DDK）現在是在 WDM 驅動程式和使用者模式元件之間傳遞屬性集的建議介面。 .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: 'IKsPropertySet 介面 (Ksproxy .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467454"
---
# <a name="ikspropertyset-interface"></a>IKsPropertySet 介面

`IKsPropertySet`介面原本是設計為在 wdm 驅動程式上設定和取出裝置屬性的有效方式，使用 KSProxy 將使用者模式 COM 方法呼叫轉譯為 wdm 串流類別驅動程式所使用的核心模式屬性集。 這個介面現在也用來嚴格傳遞軟體元件之間的資訊。

在某些情況下，軟體元件必須執行此介面，否則 **IKsControl** 介面 (記載于 DirectShow DDK) 中。 例如，如果您要撰寫軟體 MPEG-2 解碼器以與 [DVD 導覽器](dvd-navigator-filter.md)搭配使用，您必須執行這些介面的其中一個，也支援導覽器將傳送至該解碼器的 DVD 相關屬性集。 Pin 可能會支援其中一個介面，以允許其他 pin 或篩選器設定或抓取其屬性。

> [!Note]  
> 這個名稱的另一個介面存在於 dsound .h 標頭檔中。 這兩個介面不相容。 **IKsControl** 介面（記載于 DirectShow DDK）現在是在 WDM 驅動程式和使用者模式元件之間傳遞屬性集的建議介面。

 

## <a name="members"></a>成員

**IKsPropertySet** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IKsPropertySet** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IKsPropertySet** 介面具有這些方法。



| 方法                                                  | 描述                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**獲取**](ikspropertyset-get.md)                       | 抓取屬性集 GUID 和屬性識別碼所識別的屬性。<br/> |
| [**QuerySupported**](ikspropertyset-querysupported.md) | 判斷物件是否支援指定的屬性集。<br/>           |
| [**設定**](ikspropertyset-set.md)                       | 設定屬性集 GUID 和屬性識別碼所識別的屬性。<br/>      |



 

## <a name="remarks"></a>備註

您必須在 Ksproxy 之前包含 Ks。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Ksproxy。h</dt> </dl>    |
| 程式庫<br/>                  | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性集](property-sets.md)
</dt> </dl>

 

 
