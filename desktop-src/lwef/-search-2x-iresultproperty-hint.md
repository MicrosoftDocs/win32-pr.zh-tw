---
title: 'IResultProperty 提示屬性 (WdsSharedIDL .h) '
description: 用來協助資料抓取的特殊值。
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- 提示屬性舊版 Windows 環境功能
- 提示屬性舊版 Windows 環境功能，IResultProperty 介面
- IResultProperty 介面舊版 Windows 環境功能，提示屬性
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966500"
---
# <a name="iresultpropertyhint-property"></a>IResultProperty：：提示屬性

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

用來協助資料抓取的特殊值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a>屬性值

傳回提示的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





