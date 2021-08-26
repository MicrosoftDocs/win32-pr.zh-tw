---
title: 'IResultVerb Enabled 屬性 (WdsSharedIDL .h) '
description: 如果已啟用動詞，這個屬性會傳回 TRUE。
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- 已啟用屬性舊版 Windows 環境功能
- 已啟用屬性舊版 Windows 環境功能，IResultVerb 介面
- IResultVerb 介面舊版 Windows 環境功能，已啟用屬性
topic_type:
- apiref
api_name:
- IResultVerb.Enabled
- IResultVerb.get_Enabled
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c96a4c40252bf6b5ab74d3d4ec96e2568dffeed624ae2b5126059192dd72d9e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014318"
---
# <a name="iresultverbenabled-property"></a>IResultVerb：： Enabled 屬性

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

如果已啟用動詞，這個屬性會傳回 TRUE。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a>屬性值

如果已啟用動詞，這個屬性會傳回 True，否則會傳回 False。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 2.6。5<br/>                                             |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

 





