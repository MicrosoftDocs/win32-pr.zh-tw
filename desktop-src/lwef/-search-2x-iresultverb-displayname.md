---
title: 'IResultVerb DisplayName 屬性 (WdsSharedIDL .h) '
description: 這個屬性會傳回動詞之當地語系化顯示名稱的指標。
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- DisplayName 屬性舊版 Windows 環境功能
- DisplayName 屬性舊版 Windows 環境功能，IResultVerb 介面
- IResultVerb 介面舊版 Windows 環境功能，DisplayName 屬性
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d7f72d0d028fa6a6ecdede7f2d88e3e3dea0a37a14cc6365dc5da2d14992af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117694716"
---
# <a name="iresultverbdisplayname-property"></a>IResultVerb：:D isplayName 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

這個屬性會傳回動詞之當地語系化顯示名稱的指標。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a>屬性值

這個屬性會傳回動詞之當地語系化顯示名稱的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





