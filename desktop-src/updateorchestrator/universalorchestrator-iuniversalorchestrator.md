---
title: IUniversalOrchestrator 介面
description: COM 介面，提供可讓用戶端與通用協調器進行通訊的方法。
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "106992213"
---
# <a name="iuniversalorchestrator-interface"></a>IUniversalOrchestrator 介面

> [!NOTE] 
> 此 API 屬於通用 Orchestrator API。

**IUniversalOrchestrator** 是提供下列方法的 COM 介面，可讓用戶端與通用協調器進行通訊。

## <a name="methods"></a>方法

|方法 | 描述 |
|---|---|
|[::ScheduleWork](universalorchestrator-schedulework.md) | 使用通用協調器註冊暫止的工作。 |
|[::WorkCompleted](universalorchestrator-workcompleted.md) | 通知通用協調器所有工作都已完成。 |
|[::HasMoratoriumPassed](universalorchestrator-hasmoratoriumpassed.md) | 查詢通用協調器，以判斷它是否會在新的裝置現成體驗之後立即運作。 |


## <a name="requirements"></a>規格需求

| 需求 | 版本 |
|---|---|
| 最低支援的用戶端 | Windows 10 1903 |
|   |   |