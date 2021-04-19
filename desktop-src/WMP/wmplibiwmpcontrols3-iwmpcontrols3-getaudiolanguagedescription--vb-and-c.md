---
title: IWMPControls3 getAudioLanguageDescription 方法
description: GetAudioLanguageDescription 方法會傳回對應至指定之以一為基礎之索引的音訊語言描述。
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- getAudioLanguageDescription 方法 Windows Media Player
- getAudioLanguageDescription 方法 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，getAudioLanguageDescription 方法
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb45ceb166ca9c948823e516029569e457f35e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991208"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a>IWMPControls3：： getAudioLanguageDescription 方法

**GetAudioLanguageDescription** 方法會傳回對應至指定之以一為基礎之索引的音訊語言描述。

## <a name="syntax"></a>語法


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a>參數

<dl> <dt>

*lIndex* \[在\]
</dt> <dd>

以一為基礎的音訊語言索引的 **system.object** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

**System.string** ，這是音訊語言的描述。

## <a name="remarks"></a>備註

針對以 Windows Media 為基礎的內容，與語言選取相關的屬性和方法只支援單一輸出。

使用 **audioLanguageCount** 屬性來取得支援的音訊語言數目，然後使用以一為基礎的索引個別存取音訊語言。

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

[**IWMPControls3. currentAudioLanguage (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





