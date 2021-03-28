---
title: 模組資訊
description: 模組是可執行檔或 DLL。
ms.assetid: e15b5e15-ca06-4733-bd0a-705058ba2db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625877832b7e57e68ec6baff79f0c34b4478176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375529"
---
# <a name="module-information"></a>模組資訊

*模組* 是可執行檔或 DLL。 每個處理序都是由一或多個模組組成的。 您可以藉由呼叫 [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) 函式，來取出進程的模組控制碼清單。 此函式會使用指定進程的模組控制碼來填滿 **HMODULE** 值的陣列。 第一個模組是可執行檔。 請記住，這些模組控制碼最有可能來自某些其他進程，因此您無法將它們與 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)等函式搭配使用。 不過，您可以使用 [psapi.dll 函數](psapi-functions.md) ，從另一個進程取得模組的相關資訊。

下列程式描述如何從另一個進程取得模組資訊。

**若要從另一個進程取得模組資訊**

1.  呼叫 [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) 函數。 此函式會採用進程控制碼和模組控制碼做為輸入，並以模組的基底名稱填入緩衝區 (例如 Kernel32.dll) 。 相關的函式 [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa)會採用與輸入相同的參數，但會傳回模組的完整路徑 (例如，C： \\ Windows \\ System32 \\Kernel32.dll) 。
2.  呼叫 [**GetModuleInformation**](/windows/desktop/api/Psapi/nf-psapi-getmoduleinformation) 函數。 此函式會採用進程控制碼和模組控制碼，並使用模組的載入位址、它所佔用的線性位址空間大小，以及其進入點的指標來填滿 [**MODULEINFO**](/windows/desktop/api/Psapi/ns-psapi-moduleinfo) 結構。

如果應用程式需要目前進程的模組資訊，則應該使用 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) 函式，而不是 psapi.dll 模組函數。 這可協助應用程式效能的方式有兩種： **GetModuleFileName** 函式比 psapi.dll 模組函式更有效率，而且應用程式可以避免在未使用任何 psapi.dll 函式的情況下載入 psapi.dll。

[**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea)和 [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa)函式的主要設計目的是要讓偵錯工具和類似的應用程式使用，這些應用程式必須從另一個進程中解壓縮模組資訊。 如果目標進程中的模組清單已損毀或尚未初始化，或模組清單在函式呼叫期間因為載入或卸載 Dll 的結果而變更，這些函式可能會失敗或傳回不正確的資訊。

 

 