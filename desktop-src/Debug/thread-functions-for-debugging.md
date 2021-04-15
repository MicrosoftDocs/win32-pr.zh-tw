---
description: CreateThread 函式會為進程建立新的執行緒。
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: 用於偵錯工具的執行緒函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5ab0865d5585656a5c22c24e2604032de8b888
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510579"
---
# <a name="thread-functions-for-debugging"></a>用於偵錯工具的執行緒函數

[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)函式會為進程建立新的執行緒。 偵錯工具通常需要檢查或變更執行緒的暫存器內容。 若要達成此目的，偵錯工具必須使用 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 函式來取得執行緒的控制碼，並指定適當的執行緒存取 (執行緒 \_ 取得 \_ 內容、執行緒 \_ 集 \_ 內容，或這兩個) 。 [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)函式可讓偵錯工具取得現有線程的識別碼。

具有適當執行緒存取權的進程可以使用 [**GetThreadCoNtext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) 函式來檢查執行緒的暫存器，並使用 [**SetThreadCoNtext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) 函式來設定執行緒的暫存器內容。

進程也可以取得執行緒 \_ 的執行緒暫停 \_ 繼續存取。 這種類型的存取可讓偵錯工具使用 [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) 和 [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) 函數來控制執行緒的執行。 如需執行緒的詳細資訊，請參閱 [進程和執行緒](../procthread/processes-and-threads.md)。

 

 
