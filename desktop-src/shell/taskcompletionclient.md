---
description: 啟用工作完成。
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: TaskCompletionClient 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: d03e52a15e6689b7f1ea98a2f1021874cab6a8967dd148b7eaf685ff3984e8cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773648"
---
# <a name="taskcompletionclient-interface"></a>TaskCompletionClient 介面

啟用工作完成。

## <a name="members"></a>成員

**TaskCompletionClient** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **TaskCompletionClient** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**TaskCompletionClient** 介面具有這些方法。



| 方法                                                                    | 描述                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [**ApplyTaskCompletion**](taskcompletionclient-applytaskcompletion.md)   | 開始工作完成。<br/> |
| [**RevokeTaskCompletion**](taskcompletionclient-revoketaskcompletion.md) | 結束工作完成。<br/>   |



 

## <a name="remarks"></a>備註

此介面的 GUID 為 "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96"。

此 API 已被取代，未來版本的 Windows 可能無法使用。 應用程式應該使用 Windows 中的 Api [**。改為 ApplicationModel. ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041)命名空間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
