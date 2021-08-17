---
title: 處理資訊
description: 系統會維護正在執行的進程清單。 您可以藉由呼叫 EnumProcesses 函式，來取得這些進程的識別碼。 此函式會使用系統中所有進程的識別碼來填滿 DWORD 值的陣列。
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5facb72f094059997c271cb9f38beaea08981430bba40902d620a23e2875b26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094889"
---
# <a name="process-information"></a>處理資訊

系統會維護正在執行的進程清單。 您可以藉由呼叫 [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) 函式，來取得這些進程的識別碼。 此函式會使用系統中所有進程的識別碼來填滿 **DWORD** 值的陣列。

PSAPI.DLL 中的許多函式都需要進程控制碼。 若要取得正在執行之進程的進程控制碼，請將其進程識別碼 (從 [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) 取得，傳遞給 [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) 函數。 當您完成進程控制碼時，請記得呼叫 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函數。

 

 