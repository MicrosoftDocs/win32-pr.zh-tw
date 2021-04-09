---
description: 描述通知或通知結果中所包含的顯示接收物件資料。
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: 'WFD_DISPLAY_SINK_OBJECT_HEADER 結構 (Wfdsink .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849136"
---
# <a name="wfd_display_sink_object_header-structure"></a>WFD \_ 顯示 \_ 接收 \_ 物件 \_ 標頭結構

[ **WFD \_ 顯示 \_ 接收 \_ 物件 \_ 標頭** ] 結構描述通知或通知結果中所包含的顯示接收物件資料。

## <a name="syntax"></a>語法


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**型別**
</dt> <dd>

顯示接收物件的型別。 您可以使用識別碼 **WFD \_ 顯示 \_ 接收 \_ 物件 \_ 類型 \_ 預設** 值，其定義為值1。

</dd> <dt>

**修訂**
</dt> <dd>

顯示接收物件的修訂版本。 您可以使用識別碼 **WFD \_ 顯示 \_ 接收 \_ 物件 \_ 修訂 \_ \_ 第1版** ，其定義為值1。

</dd> <dt>

**長度**
</dt> <dd>

通知或通知結果中的資料長度。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Wfdsink。h</dt> </dl> |



 

 




