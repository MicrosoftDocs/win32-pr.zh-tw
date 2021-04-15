---
title: 關於版本資訊
description: 本主題討論版本資訊功能。
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- 資源，版本資訊
- 版本資訊
- 加入版本資訊
- 檔案衝突
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375105"
---
# <a name="about-version-information"></a>關於版本資訊

您可以使用版本資訊函式來判斷應該安裝檔案的位置，以及識別與目前已安裝之檔案的衝突。 這些函數可讓您避免下列問題：

-   在較新版本上安裝較舊版本的元件
-   在混合語言系統中變更語言而不發出通知
-   在不同的目錄中安裝程式庫的多個複本
-   將檔案複製到多個使用者共用的網路目錄

版本資訊函式可讓應用程式查詢版本資源以取得檔案資訊，並以純文字格式呈現資訊。 此資訊包括檔案的用途、作者、版本號碼等等。

您可以將版本資訊新增至任何可以有 Windows 資源的檔案，例如 Dll、可執行檔或 fon 字型檔案。 若要新增資訊，請建立 [VERSIONINFO 資源](/windows/desktop/menurc/versioninfo-resource) ，並使用資源編譯器來編譯資源。

 

 