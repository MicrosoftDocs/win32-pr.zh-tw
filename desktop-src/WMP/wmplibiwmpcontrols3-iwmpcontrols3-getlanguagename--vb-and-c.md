---
title: IWMPControls3 getLanguageName 方法
description: GetLanguageName 方法會傳回具有指定地區設定識別碼 (LCID) 的音訊語言名稱。
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- getLanguageName 方法 Windows Media Player
- getLanguageName 方法 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，getLanguageName 方法
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93bf97c7b5213e3d196897de1c3ebcfa6e6d2c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980202"
---
# <a name="iwmpcontrols3getlanguagename-method"></a>IWMPControls3：： getLanguageName 方法

**GetLanguageName** 方法會傳回具有指定地區設定識別碼 (LCID) 的音訊語言名稱。

## <a name="syntax"></a>語法


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a>參數

<dl> <dt>

*lLangID* \[在\]
</dt> <dd>

為 LCID 的 **system.object** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

**System.string** ，這是音訊語言的名稱。

## <a name="remarks"></a>備註

LCID 可唯一識別特定語言方言，稱為地區設定。

針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。

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

[**IWMPControls3. getAudioLanguageID (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





