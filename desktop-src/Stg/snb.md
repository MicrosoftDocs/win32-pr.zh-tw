---
title: 'SNB (Objidl.idl) '
description: 字串名稱區塊 (SNB) 是指向字串指標陣列的指標，而這些指標是以 Null 指標結尾。
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- 瑞士 央行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934148"
---
# <a name="snb"></a>瑞士 央行

字串名稱區塊 (**SNB**) 是指向字串指標陣列的指標，而這些指標是以 **Null** 指標結尾。 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)介面和開啟儲存體物件的函式呼叫會使用字串名稱區塊。 字串指向所包含的儲存物件或要在開啟的呼叫中排除的資料流程。


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

**瑞士 央行**
</dt> <dd>

\[\_ (wireSNB) 的有線封送處理\]

</dd> </dl>

## <a name="remarks"></a>備註

**SNB** 的建立方式是配置連續的記憶體區塊，其中字串的指標後面接著 **Null** 指標，後面接著實際的字串。

**SNB** 的封送處理是以這種方式建立的 **SNB** 為基礎。 雖然可以透過其他方式來儲存，但以這種方式建立的 **SNB** 有一個優點，就是只需要一個配置作業和一個釋出記憶體給所有字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Objidl.idl。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Objidl.idl .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





