---
description: 瞭解如何使用 CreateThread 函式來建立進程的新執行緒。 偵錯工具通常需要檢查或變更執行緒的暫存器內容。
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: 用於偵錯工具的執行緒函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46e9c94ef776cd14bc76afb2c824f2150a1e7c0eb8c94176b237e1c6d54430f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655218"
---
# <a name="thread-functions-for-debugging"></a>用於偵錯工具的執行緒函數

[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)函式會為進程建立新的執行緒。 偵錯工具通常需要檢查或變更執行緒的暫存器內容。 若要達成此目的，偵錯工具必須使用 [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) 函式來取得執行緒的控制碼，並指定適當的執行緒存取 (執行緒 \_ 取得 \_ 內容、執行緒 \_ 集 \_ 內容，或這兩個) 。 [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)函式可讓偵錯工具取得現有線程的識別碼。

具有適當執行緒存取權的進程可以使用 [**GetThreadCoNtext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) 函式來檢查執行緒的暫存器，並使用 [**SetThreadCoNtext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) 函式來設定執行緒的暫存器內容。

進程也可以取得執行緒 \_ 的執行緒暫停 \_ 繼續存取。 這種類型的存取可讓偵錯工具使用 [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) 和 [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) 函數來控制執行緒的執行。 如需執行緒的詳細資訊，請參閱 [進程和執行緒](../procthread/processes-and-threads.md)。

 

 
