---
title: IWMPControls3 currentAudioLanguage 屬性
description: CurrentAudioLanguage 屬性會取得或設定用於播放之音訊語言 (LCID) 的地區設定識別碼。
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- currentAudioLanguage 屬性 Windows Media Player
- currentAudioLanguage 屬性 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，currentAudioLanguage 屬性
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1a4f668cec560528270d52a2abe4777ce32d3ceb38ce21345342ef87866c38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115875"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a>IWMPControls3：： currentAudioLanguage 屬性

**CurrentAudioLanguage** 屬性會取得或設定用於播放之音訊語言 (LCID) 的地區設定識別碼。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a>屬性值

System.string **，它** 是音訊語言的 LCID。

## <a name="remarks"></a>備註

LCID 可唯一識別特定語言方言，稱為地區設定。

針對 Windows 媒體型內容，與語言選取相關的屬性和方法只支援單一輸出。

使用 DVD 內容時，指定 LCID 將會導致第一個可用的音訊播放軌選取指定的語言識別項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPControls3 介面 (VB 和 c # )**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. audioLanguageCount (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguageIndex (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





