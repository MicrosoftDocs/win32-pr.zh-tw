---
title: 連結到遠端存取 DLL
description: 如果應用程式以靜態方式連結至 RASAPI32 DLL，則如果未安裝遠端存取服務，應用程式將無法載入。
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842552"
---
# <a name="linking-to-the-remote-access-dll"></a>連結到遠端存取 DLL

如果應用程式以靜態方式連結至 RASAPI32 DLL，則如果未安裝遠端存取服務，應用程式將無法載入。 如果未使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 來載入 DLL，則可以載入 ras 應用程式，並使用 [**GETPROCADDRESS**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 來取得 ras 函式的指標。

RAS 函數位于 RASAPI32.DLL 中。 這些函數的匯入程式庫是 RASAPI32。自由。 若要使用 RAS 功能，您的程式必須包含下列檔案：



| 檔案       | 描述                                                                 |
|------------|-----------------------------------------------------------------------------|
| Ras。H      | 包含 RAS 函數原型、常數和結構定義。 |
| RASERROR.H | 包含 RAS 錯誤碼。                                               |



 

 

 