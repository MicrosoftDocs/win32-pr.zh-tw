---
description: 您可以使用下列程式，來對以 Microsoft Visual C++ 撰寫的專家進行 debug 錯。
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: 錯專家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985205"
---
# <a name="debugging-an-expert"></a>錯專家

您可以使用下列程式，來對以 Microsoft Visual C++ 撰寫的專家進行 debug 錯。

**錯專家**

1.  將專家 (DLL 檔) 和程式資料庫檔案 ( .pdb) 當您在正確的位置中編譯專家時產生。 如需詳細資訊，請參閱 [安裝專家至網路監視器 2.1](installing-an-expert-to-network-monitor-2-1.md)。
2.  開始 Microsoft Visual C++。
3.  **在 [檔案] 功能表中**，按一下 [**開啟**]，然後選取您的專家 DLL 名稱。
4.  Microsoft Visual C++ 載入之後，請按一下 [ **專案** ] 功能表，然後按一下 [ **設定**]。
5.  按一下 [ **Debug**]。 在 [ **可執行檔**] 下，輸入 Netmon.exe 的完整路徑，例如：

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  在您的程式碼中設定中斷點。

 

 



