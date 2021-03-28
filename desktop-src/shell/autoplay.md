---
description: 自動執行時間是 Windows 作業系統的一項功能。
title: 建立啟用自動安裝的 cd-rom 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191188"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>建立啟用自動安裝的 cd-rom 應用程式

自動執行時間是 Windows 作業系統的一項功能。 它會將安裝及設定產品的程式自動化，這些產品是在 CD-ROM 上發佈的以 Windows 為基礎的平臺所設計。 當使用者將已啟用自動安裝的光碟片插入 cd-rom 光碟機時，自動執行會自動執行安裝、設定或執行所選產品的 CD-ROM 上的應用程式。

自動執行可以用來安裝和執行 CD-ROM 應用程式。 雖然自動執行最常用於 Windows 應用程式，但是它也可以用來在 Windows Microsoft MS-DOS 會話中安裝、設定或執行以 MS-DOS 為基礎的應用程式。 您可以使用自己的唯一圖示、Config.sys 檔和 Autoexec.bat 檔案，設定每個以 MS-DOS 為基礎的應用程式。 Windows 會為以 MS-DOS 為基礎的應用程式建立正確的設定檔。 啟動應用程式接著會在視窗中啟動以 ms-dos 為基礎的應用程式。

> [!Note]  
> 若要讓執行正常運作，CD-ROM 光碟機必須有32或64位設備磁碟機，以在使用者插入光碟並通知系統時偵測到。

 

下列各節將討論如何執行啟用自動安裝的 cd-rom 應用程式。

-   [建立 AutoRun-Enabled 應用程式](autoplay-works.md)
-   [自動播放 .inf 專案](autorun-cmds.md)
-   [啟用和停用自動啟動](autoplay-reg.md)

 

 



