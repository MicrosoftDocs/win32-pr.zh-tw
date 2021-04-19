---
title: IWMPClosedCaption2 getSAMILangID 方法
description: GetSAMILangID 方法會傳回目前薩米文檔案所支援語言 (LCID) 的地區設定識別碼。
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- getSAMILangID 方法 Windows Media Player
- getSAMILangID 方法 Windows Media Player，IWMPClosedCaption2 介面
- IWMPClosedCaption2 介面 Windows Media Player，getSAMILangID 方法
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9aaebecf8e86c056fa9c91141042facc6bcc18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987942"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a>IWMPClosedCaption2：： getSAMILangID 方法

**GetSAMILangID** 方法會傳回目前薩米文檔案所支援語言 (LCID) 的地區設定識別碼。

## <a name="syntax"></a>語法


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a>參數

<dl> <dt>

*nIndex* \[在\]
</dt> <dd>

要抓取之 LCID 的以零為基底之索引的 **system.object** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

使用指定索引之語言的 LCID 的 **system.object。**

## <a name="remarks"></a>備註

薩米文檔案中的語言會依照檔案中顯示的順序編制索引，從零開始。

除非 (AxWindowsMediaPlayer 開啟數位媒體檔案，否則這個方法會傳回0。 openState 等於 13) 。

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

[**IWMPClosedCaption2 介面 (VB 和 c # )**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





