---
title: IWMPSettings2 defaultAudioLanguage 屬性
description: DefaultAudioLanguage 屬性會取得 Windows Media Player 中指定之預設音訊語言 (LCID) 的地區設定識別碼。
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- defaultAudioLanguage 屬性 Windows Media Player
- defaultAudioLanguage 屬性 Windows Media Player，IWMPSettings2 介面
- IWMPSettings2 介面 Windows Media Player，defaultAudioLanguage 屬性
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ac9120437005d9f32388e4d639d2d5893675e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983016"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a>IWMPSettings2：:d efaultAudioLanguage 屬性

**DefaultAudioLanguage** 屬性會取得 Windows Media Player 中指定之預設音訊語言 (LCID) 的地區設定識別碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a>屬性值

為 LCID 的 **system.object** 。

## <a name="remarks"></a>備註

LCID 可唯一識別特定語言方言，稱為地區設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPControls3. currentAudioLanguage (VB 和 c # )**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2 介面 (VB 和 c # )**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





