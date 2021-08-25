---
description: 表示可以用來改善辨識結果的單字清單。
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: 'InkWordList 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: fe46cf8f1befaf2717cfcf0a8e131113ed4552843bd3b6572364c27f3418ab34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938668"
---
# <a name="inkwordlist-class"></a>InkWordList 類別

表示可以用來改善辨識結果的單字清單。

**InkWordList** 具有下列類型的成員：

-   [介面](#interfaces)
-   [方法](#methods)

### <a name="interfaces"></a>介面

**InkWordList** 類別會定義這些介面。



| 介面        | 描述                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkWordList** | 這個物件會實 **IInkWordList** COM 介面。<br/> |



 

### <a name="methods"></a>方法

**InkWordList** 類別有這些方法。



| 方法                                       | 描述                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [**AddWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | 將單一單字加入至 **InkWordList**。<br/>                   |
| [**合併**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | 將另一個 **InkWordList** 合併到這個 **InkWordList** 中。<br/> |
| [**RemoveWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | 從 **InkWordList** 中移除單一單字。<br/>                |



 

## <a name="remarks"></a>備註

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**單詞表屬性**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[模擬常數](factoid-constants.md)
</dt> <dt>

[**InkRecognizerCoNtext 類別**](inkrecognizercontext-class.md)
</dt> </dl>

 

