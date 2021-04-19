---
title: IWMPClosedCaption SAMIFileName 屬性
description: SAMIFileName 屬性會取得或設定包含隱藏式輔助字幕所需資訊的檔案名。
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- SAMIFileName 屬性 Windows Media Player
- SAMIFileName 屬性 Windows Media Player，IWMPClosedCaption 介面
- IWMPClosedCaption 介面 Windows Media Player，SAMIFileName 屬性
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992962"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a>IWMPClosedCaption：： SAMIFileName 屬性

**SAMIFileName** 屬性會取得或設定包含隱藏式輔助字幕所需資訊的檔案名。

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a>屬性值

表示 **已** 同步處理之可存取媒體的名稱 (薩米) 的檔案。

## <a name="remarks"></a>備註

薩米文檔案必須使用 smi-s 或薩米的副檔名。

如果您未使用 **SAMIFileName** 設定值，這個屬性會取得 **字串** ，其中包含與目前媒體專案相關聯的預設檔案名或 URL。 當您使用 *薩米* 文 URL 參數指定薩米文的檔案時，或當薩米文的檔案與數位媒體檔案的名稱相同時，就可能會發生此關聯 (但副檔名) 除外。 如果目前媒體沒有相關聯的預設薩米文檔案，這個屬性會取得長度為零的字串 ( "" ) 。

使用 **SAMIFileName** 設定值之後，該值會一直保留到您將新值設定 (或直到使用薩米文 URL 參數) 開啟新的媒體專案為止。 因此，在播放每個新媒體專案之前，您必須為這個屬性設定新的值。 如此一來， **SAMIFileName** 的新值就會在下一個媒體專案開啟 (或) **AxWindowsMediaPlayer** 時才會生效。 為 **SAMIFileName** 指定新的值對目前的媒體沒有任何作用。

若要使 Windows Media Player 使用與特定媒體專案相關聯的預設薩米文檔案，請將 **SAMIFileName** 設定為零長度的字串 ( "" ) ，再播放下一個媒體專案。

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

[**AxWindowsMediaPlayer。關閉**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**IWMPClosedCaption 介面 (VB 和 c # )**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2 介面 (VB 和 c # )**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





