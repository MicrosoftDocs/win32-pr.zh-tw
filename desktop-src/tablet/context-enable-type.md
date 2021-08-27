---
description: 指出是否應該將內容訊息傳送至擁有視窗的視窗程式。
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: CONTEXT_ENABLE_TYPE 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 94bffba211f75416ccae5e9a55342441b7b11b41b1a9f1f4b085ec190f991645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110968"
---
# <a name="context_enable_type-enumeration"></a>內容 \_ 啟用 \_ 類型列舉

指出是否應該將內容訊息傳送至擁有視窗的視窗程式。

## <a name="syntax"></a>Syntax


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**\_啟用內容**
</dt> <dd>

應該啟用平板電腦內容，以產生將內容訊息傳送至擁有視窗的視窗程式。

</dd> <dt>

<span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**內容 \_ 停用**
</dt> <dd>

應該停用 tablet 內容，防止任何進一步的內容訊息傳送至主控視窗的視窗程式或事件接收器。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITablet：： CreateCoNtext 方法**](itablet-createcontext.md)
</dt> </dl>

 

 




