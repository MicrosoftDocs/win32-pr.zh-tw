---
description: 裝載應用程式可以透過兩種方法來搜尋並存元件。
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: 搜尋元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f257b7da8099508fb268623a175d8ebd8e9d8337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983847"
---
# <a name="searching-for-assemblies"></a>搜尋元件

裝載應用程式可以透過兩種方法來搜尋並存元件。

裝載的模組可以藉由擴充一些共用設定資訊，向主控應用程式註冊自己的模組。 然後，應用程式可以使用此設定資訊來載入新功能所需的元件。 這可以藉由呼叫註冊資料中指定之資訊清單的 [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) 來完成，然後呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以進入新的模組。 請注意，使用此方法時，新元件必須更新某些共用應用程式狀態，以指出其存在。

裝載應用程式可以在啟動時使用 [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) 和 [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) 主動搜尋元件，以便在指定的位置尋找 dll 或資訊清單，然後使用 [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) 來存取訊號。 此方法不需要註冊元件。

 

 
