---
description: 包含用來建立平板電腦內容的資訊。
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: TABLET_CONTEXT_SETTINGS 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945351"
---
# <a name="tablet_context_settings-structure"></a>TABLET \_ 內容 \_ 設定結構

包含用來建立平板電腦內容的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a>成員

<dl> <dt>

**cPktProps**
</dt> <dd>

封包中的屬性數目。

</dd> <dt>

**pguidPktProps**
</dt> <dd>

封包屬性的唯一識別碼。

</dd> <dt>

**cPktBtns**
</dt> <dd>

按鈕的數目。

</dd> <dt>

**pguidPktBtns**
</dt> <dd>

按鈕的唯一識別碼。

</dd> <dt>

**pdwBtnDnMask**
</dt> <dd>

按鈕下遮罩。

</dd> <dt>

**pdwBtnUpMask**
</dt> <dd>

按鈕的遮罩。

</dd> <dt>

**lXMargin**
</dt> <dd>

X 方向邊界。

</dd> <dt>

**lYMargin**
</dt> <dd>

Y 方向邊界。

</dd> </dl>

## <a name="remarks"></a>備註

一般而言，應用程式會從 [**ITablet：： GetDefaultCoNtextSettings 方法**](itablet-getdefaultcontextsettings.md)取得預設值、修改值以符合其需求，然後將修改過的設定結構傳遞至 [**ITablet：： CreateCoNtext 方法**](itablet-createcontext.md)。

此結構會決定應用程式將取得哪些事件、如何處理這些事件，以及如何將它們傳遞給應用程式或 Windows 本身。

按鈕會一起遮罩，以決定內容將處理哪些種類的事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                     |



 

 




