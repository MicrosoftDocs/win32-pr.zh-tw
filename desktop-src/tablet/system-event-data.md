---
description: 包含 tablet 系統事件的相關資訊。
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: SYSTEM_EVENT_DATA 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 58e153da2695990f74d1268aa3e861bb9011b108ebdd1ea2d5128ff6f8e40a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708208"
---
# <a name="system_event_data-structure"></a>系統 \_ 事件 \_ 資料結構

包含 tablet 系統事件的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**bModifier**
</dt> <dd>

修飾詞的位值。 如需詳細資訊，請參閱「備註」一節。

</dd> <dt>

**wKey**
</dt> <dd>

掃描鍵盤字元的程式碼。

</dd> <dt>

**xPos**
</dt> <dd>

事件的 X 位置。

</dd> <dt>

**yPos**
</dt> <dd>

事件的 Y 位置。

</dd> <dt>

**bCursorMode**
</dt> <dd>

造成事件的資料指標類型。 如需詳細資訊，請參閱「備註」一節。

</dd> <dt>

**dwButtonState**
</dt> <dd>

系統事件時按鈕的狀態。

</dd> </dl>

## <a name="remarks"></a>備註

下列系統事件已定義為在 **bModifier** 成員中使用。



| 值               | 描述                  |
|---------------------|------------------------------|
| SE \_修飾詞 \_ CTRL  | 已按下控制項鍵。 |
| SE \_修飾詞 \_ ALT   | 已按下 ALT 鍵。     |
| SE \_修飾詞 \_ 移位 | 已按下 Shift 鍵。   |



 

下列系統事件已定義為在 **bCursorMode** 成員中使用。



| 值              | 描述               |
|--------------------|---------------------------|
| SE \_一般資料 \_ 指標 | 表示畫筆提示。    |
| SE \_橡皮擦 \_ 游標 | 表示畫筆橡皮擦。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IStylusPlugin：： SystemEvent 方法**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[**ITabletEventSink：： SystemEvent 方法**](itableteventsink-systemevent.md)
</dt> </dl>

 

 




