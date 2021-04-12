---
description: 進程會使用 CreateFile 函式來開啟通訊資源的控制碼。
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: 通訊資源控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385938"
---
# <a name="communications-resource-handles"></a>通訊資源控制碼

進程會使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來開啟通訊資源的控制碼。 例如，指定 COM1 會開啟序列埠的控制碼，而 LPT1 會開啟平行埠的控制碼。 如果指定的資源目前正由另一個進程使用中， **CreateFile** 就會失敗。 進程的任何執行緒都可以使用 **CreateFile** 所傳回的控制碼，來識別存取資源之任何函式中的資源。

當進程呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 開啟通訊資源時，它會指定下列屬性：

-   指定資源存在何種類型的讀取/寫入存取權。
-   控制碼是否可由子進程繼承。
-   控制碼是否可用於重迭 (非同步) i/o 作業。  (如需重迭作業的描述，請參閱 [同步](/windows/desktop/Sync/synchronization)處理。 ) 

當程式使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 開啟通訊資源時，它必須指定下列參數的特定值：

-   *FdwShareMode* 參數必須為零，開啟資源以進行獨佔存取。
-   *FdwCreate* 參數必須指定 OPEN \_ EXISTING 旗標。
-   *HTemplateFile* 參數必須為 **Null**。

使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)直接將控制碼開啟至裝置時，應用程式必須使用特殊字元 " \\ \\ . \\ " 來識別裝置。 例如，若要開啟磁片磁碟機 A 的控制碼，請指定 \\ \\ 。 \\a：適用于 **CreateFile** 的 *lpszName* 參數。 呼叫進程可使用 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式中的控制碼，將控制程式代碼傳送至裝置。

 

 
