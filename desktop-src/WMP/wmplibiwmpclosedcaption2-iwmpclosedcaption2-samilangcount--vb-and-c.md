---
title: IWMPClosedCaption2 SAMILangCount 屬性
description: SAMILangCount 屬性會取得目前的薩米文檔案所支援的語言數目。
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- SAMILangCount 屬性 Windows Media Player
- SAMILangCount 屬性 Windows Media Player，IWMPClosedCaption2 介面
- IWMPClosedCaption2 介面 Windows Media Player，SAMILangCount 屬性
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b85ce04bd672f0219b8dd96f91172241689a80042a37a7680e2f8e26b65c85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899998"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a>IWMPClosedCaption2：： SAMILangCount 屬性

**SAMILangCount** 屬性會取得目前的薩米文檔案所支援的語言數目。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a>屬性值

支援的語言數目的 **system.object** 。

## <a name="remarks"></a>備註

除非 (AxWindowsMediaPlayer 開啟數位媒體檔案，否則此屬性會傳回0。 openState 等於 13) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**IWMPClosedCaption 介面 (VB 和 c # )**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. SAMILang (VB 和 c # )**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2 介面 (VB 和 c # )**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2. getSAMILangName (VB 和 c # )**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





