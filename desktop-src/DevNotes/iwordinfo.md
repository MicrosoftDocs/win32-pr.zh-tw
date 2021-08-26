---
description: IWordInfo 介面是日文專用的語言資源元件。 物件會剖析文字並識別個別的單字，並傳回字串中的文字，或傳回字典 (根) 形式的字串文字中的單字。
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: IWordInfo 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: a82ff0c5d817dbec6d64d1d38d40245983877563416b30760926bb7522cd14c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001468"
---
# <a name="iwordinfo-interface"></a>IWordInfo 介面

\[此介面已淘汰，且在 Windows Vista 中不受支援。\]

**IWordInfo** 介面是日文專用的語言資源元件。 物件會剖析文字並識別個別的單字，並傳回字串中的文字，或傳回字典 (根) 形式的字串文字中的單字。

## <a name="members"></a>成員

**IWordInfo** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWordInfo** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWordInfo** 介面具有這些方法。



| 方法        | 描述                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| **BreakText** | 剖析文字以識別單字，並將結果提供給 [WordSink](/previous-versions//ms691570(v=vs.85)) 物件。<br/> |



 

## <a name="remarks"></a>備註

這個介面是用來針對要分析的文字，取得日文斷詞或字典表單。 單字的字典形式是單字的 uninflected 形式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                  |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
