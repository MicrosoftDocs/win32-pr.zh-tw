---
description: 向量化例外狀況處理常式是結構化例外狀況處理的延伸。
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: 向量式例外狀況處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847295"
---
# <a name="vectored-exception-handling"></a>向量式例外狀況處理

向量化例外狀況處理常式是結構化例外狀況處理的延伸。 應用程式可以註冊函式，以監看或處理應用程式的所有例外狀況。 向量處理常式不是以框架為基礎，因此您可以加入將呼叫的處理常式，而不論您在呼叫框架中的哪個位置。 向量處理常式會依其加入的順序來呼叫，偵錯工具會取得第一次可能的通知，但在系統開始回溯堆疊之前。

若要加入向量 continue 處理常式，請使用 [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) 函數。 若要移除這個處理常式，請使用 [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) 函數。

若要加入向量式例外狀況處理常式，請使用 [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) 函數。 若要移除這個處理常式，請使用 [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) 函數。

 

 
