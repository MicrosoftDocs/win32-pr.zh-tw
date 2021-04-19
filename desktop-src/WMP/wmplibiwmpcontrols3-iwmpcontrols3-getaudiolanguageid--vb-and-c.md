---
title: IWMPControls3 getAudioLanguageID 方法
description: GetAudioLanguageID 方法會針對指定的音訊語言索引，傳回 (LCID) 的地區設定識別碼。
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- getAudioLanguageID 方法 Windows Media Player
- getAudioLanguageID 方法 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，getAudioLanguageID 方法
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990998"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a>IWMPControls3：： getAudioLanguageID 方法

**GetAudioLanguageID** 方法會針對指定的音訊語言索引，傳回 (LCID) 的地區設定識別碼。

## <a name="syntax"></a>語法


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a>參數

<dl> <dt>

*lIndex* \[在\]
</dt> <dd>

以一為基礎之音訊語言的一種類型的 **system.object** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

為 LCID 的 **system.object** 。

## <a name="remarks"></a>備註

LCID 可唯一識別特定語言方言，稱為地區設定。

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

[**IWMPControls3. currentAudioLanguage (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguageIndex (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





