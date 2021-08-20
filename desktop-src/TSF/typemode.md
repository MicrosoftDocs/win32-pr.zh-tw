---
title: 'TYPEMODE 列舉 (Softkbdc) '
description: TYPEMODE 列舉的元素可用來指定可供軟鍵盤使用的類型模式。
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- TYPEMODE 列舉文字服務架構
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ae25435b48d1482441b8617a52bace8debabb210b62782a234837553e2c36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949835"
---
# <a name="typemode-enumeration"></a>TYPEMODE 列舉

**TYPEMODE** 列舉的元素可用來指定可供軟鍵盤使用的類型模式。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**
</dt> <dd>

使用者可以按一下螢幕上的按鍵來輸入文字。

</dd> <dt>

<span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**懸停**
</dt> <dd>

使用者可以在預先定義的時間點指向金鑰，而選取的字元會自動輸入。

</dd> <dt>

<span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**掃描**
</dt> <dd>

軟鍵盤會持續掃描輸入區域，並反白顯示使用者可以按下快速鍵或使用切換輸入裝置的區域。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Softkbdc。h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd .idl</dt> </dl> |



 

 





