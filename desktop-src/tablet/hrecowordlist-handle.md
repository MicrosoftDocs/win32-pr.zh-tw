---
description: HRECOWORDLIST 控制碼可用來管理您附加至辨識器內容的字組清單。 您可以使用單字清單來改善辨識結果。
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: 'HRECOWORDLIST 控制碼 (Recapis .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7384873f562627f54326cfca78883c9f3a02351dad1df0bf45a23b61b03c167d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967557"
---
# <a name="hrecowordlist-handle"></a>HRECOWORDLIST 控制碼

**HRECOWORDLIST** 控制碼可用來管理您附加至辨識器內容的字組清單。 您可以使用單字清單來改善辨識結果。


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a>備註

下列函數使用 **HRECOWORDLIST**。



| 函式                                         | 描述                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [**AddWordsToWordList**](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | 將一或多個單字加入至單字清單。<br/> |
| [**DestroyWordList**](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | 終結目前的字組清單。<br/>          |
| [**MakeWordList**](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | 建立字組清單。<br/>                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                        |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>Recapis。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SetWordList 函式**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




