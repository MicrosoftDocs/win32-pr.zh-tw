---
description: 應用程式必須先建立或開啟金鑰，應用程式才能將資料新增至登錄。
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: 開啟、建立和關閉索引鍵
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605d53a00506122c6350abd7f06e9166ed487de98c7910a3b7c3a913978492f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763960"
---
# <a name="opening-creating-and-closing-keys"></a>開啟、建立和關閉索引鍵

應用程式必須先建立或開啟金鑰，應用程式才能將資料新增至登錄。 若要建立或開啟金鑰，應用程式一律會將金鑰參考為目前開啟金鑰的子機碼。 下列預先定義的金鑰一律會開啟 **： HKEY \_ 本機 \_ 電腦**、 **HKEY \_ 類別 \_ 根**、 **HKEY \_ 使用者**，以及 **HKEY 目前的 \_ \_ 使用者**。 應用程式會使用 [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) 函數來開啟索引鍵，並使用 [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) 函式來建立索引鍵。 登錄樹狀目錄可以是深512層級。 您可以透過單一登入 API 呼叫，一次最多建立32個層級。

應用程式可以使用 [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) 函式來關閉機碼，並將其包含的資料寫入登錄中。 **RegCloseKey** 不一定會在傳回之前將資料寫入登錄;將快取排清至硬碟可能需要數秒鐘的時間。 如果應用程式必須明確地將登錄資料寫入硬碟，則可以使用 [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) 函數。 不過， **RegFlushKey** 會使用許多系統資源，而且只有在絕對必要時才應該呼叫。

 

 



