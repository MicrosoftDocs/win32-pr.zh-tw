---
description: 自動運行是 Windows 作業系統的一項功能。
title: 建立啟用自動安裝的 cd-rom 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b8bc1edad7fe49b996dd8471ae8ce081c36c71b7b7df48ca6296b07f8646ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460928"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>建立啟用自動安裝的 cd-rom 應用程式

自動運行是 Windows 作業系統的一項功能。 它會將安裝及設定產品的程式自動化，這些產品是針對發佈在 cd-rom 上的以 Windows 為基礎的平臺所設計。 當使用者將已啟用自動安裝的光碟片插入 cd-rom 光碟機時，自動執行會自動執行安裝、設定或執行所選產品的 CD-ROM 上的應用程式。

自動執行可以用來安裝和執行 CD-ROM 應用程式。 雖然自動執行最常用於 Windows 的應用程式，但是它也可以用來在 Windows Microsoft MS-DOS 會話中安裝、設定或執行以 ms-dos 為基礎的應用程式。 您可以使用自己的唯一圖示、Config.sys 檔和 Autoexec.bat 檔案，設定每個以 MS-DOS 為基礎的應用程式。 Windows 建立以 ms-dos 為基礎之應用程式的正確設定檔案。 啟動應用程式接著會在視窗中啟動以 ms-dos 為基礎的應用程式。

> [!Note]  
> 若要讓執行正常運作，CD-ROM 光碟機必須有32或64位設備磁碟機，以在使用者插入光碟並通知系統時偵測到。

 

下列各節將討論如何執行啟用自動安裝的 cd-rom 應用程式。

-   [建立 AutoRun-Enabled 應用程式](autoplay-works.md)
-   [自動播放 .inf 專案](autorun-cmds.md)
-   [啟用和停用自動啟動](autoplay-reg.md)

 

 



