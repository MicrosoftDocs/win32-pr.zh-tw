---
title: IUniversalOrchestrator 介面
description: COM 介面，提供可讓用戶端與通用協調器進行通訊的方法。
ms.date: 01/14/2021
ms.topic: reference
ms.openlocfilehash: 5dbbaafb38ab9d790d32beca9b014f933d5d53d5
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991845"
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