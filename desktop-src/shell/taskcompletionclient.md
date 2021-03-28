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
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194428"
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

此 API 已被取代，在未來的 Windows 版本中可能無法使用。 應用程式應該改為使用 [**ApplicationModel. ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) 命名空間中的 api。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
