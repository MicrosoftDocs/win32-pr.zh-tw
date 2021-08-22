---
description: 下列程式示範如何對監視器進行偵錯工具。
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: 偵測監視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7ce15252470b280a988f81fe221218778a0fa5e4851db0d3e419d1653fbe92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144201"
---
# <a name="debugging-a-monitor"></a>偵測監視

下列程式示範如何對監視器進行偵錯工具。

**若要對監視器進行調試**

1.  當您在正確的位置中編譯監視器時，請安裝監視 DLL 和程式資料庫 ( .pdb) 檔案。 如需進一步的詳細資料，請參閱 [安裝監視器以網路監視器](installing-a-monitor-to-network-monitor.md) 。
2.  選取 [主控台]、[服務]，確認監視器控制服務已設定為伺服器，而不是服務。
3.  開啟命令提示字元，然後移至網路監視器目錄。 輸入：

    **Mcsvc.exe/RegServer**

    在監視的偵錯工具完成之後，您可以輸入下列命令，將 MCSVC 傳回到其預設條件：

    **Mcsvc.exe/Service**

4.  在 Microsoft Visual Studio 中，啟動 Microsoft Visual C++。
5.  從 [**檔案] 的 [****開啟** 功能表] 選項中，選取您的監視器 DLL 名稱。
6.  Microsoft Visual C++ 載入之後，請按一下 [ **Project**]，**設定**。
7.  按一下 [**可執行檔**] 下的 [**調試** 程式] 索引標籤來進行 debug session，然後輸入 Mcsvc.exe 的完整路徑 例如，C： \\ Program files \\ Netmon2 \\Mcsvc.exe。
8.  在程式碼中設定中斷點。

> [!Note]  
> 請勿使用訊息方塊來監視偵錯工具。 如果 MCSVC 是以服務的形式執行，您將不會看到快顯視窗，而且 MCSVC 會顯示為「停止回應」。

 

 

 



