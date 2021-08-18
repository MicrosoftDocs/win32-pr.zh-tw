---
title: 'IResultType DisplayName 屬性 (WdsSharedIDL .h) '
description: 類型的當地語系化顯示名稱
ms.assetid: 21695ba3-aa6d-419b-961a-0643caa5ea1f
keywords:
- DisplayName 屬性舊版 Windows 環境功能
- DisplayName 屬性舊版 Windows 環境功能，IResultType 介面
- IResultType 介面舊版 Windows 環境功能，DisplayName 屬性
topic_type:
- apiref
api_name:
- IResultType.DisplayName
- IResultType.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e045306250d2642ae281d81c8ffb8ab5a298134bf999ddba6abd5fd1660aeb1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399784"
---
# <a name="iresulttypedisplayname-property"></a>IResultType：:D isplayName 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

類型的當地語系化顯示名稱：

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>屬性值

傳回類型的當地語系化顯示名稱位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





