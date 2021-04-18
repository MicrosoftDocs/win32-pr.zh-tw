---
title: 'TITLEBAR_TYPE 列舉 (Softkbdc .h) '
description: 標題列型別 \_ 列舉的元素是用來指定可供軟鍵盤視窗使用的 titlebars 類型。
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- TITLEBAR_TYPE 列舉文字服務架構
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965087"
---
# <a name="titlebar_type-enumeration"></a>標題列 \_ 類型列舉

**標題列 \_ 型** 別列舉的元素是用來指定可供軟鍵盤視窗使用的 titlebars 類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**標題列 \_ 無**
</dt> <dd>

[螢幕小鍵盤] 視窗不會使用標題列。

</dd> <dt>

<span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**標題 \_ 欄 \_ \_ 僅限水準控制**
</dt> <dd>

[螢幕小鍵盤] 視窗只會使用水準移出控制條。

</dd> <dt>

<span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**標題列 \_ 抓取 \_ VERTI \_**
</dt> <dd>

[螢幕小鍵盤] 視窗只會使用垂直的控制手柄列。

</dd> <dt>

<span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**標題列 \_ 抓取 \_ 按鈕**
</dt> <dd>

[螢幕小鍵盤] 視窗只會使用 [移出控制] 按鈕。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Softkbdc。h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd .idl</dt> </dl> |



 

 





