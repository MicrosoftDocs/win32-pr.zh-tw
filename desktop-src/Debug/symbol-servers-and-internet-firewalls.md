---
description: 某些系統會使用需要驗證所有網際網路流量的網際網路防火牆或 proxy 伺服器。
ms.assetid: b79e9a6f-2ffb-4ec0-ac2d-63e79ecfc26c
title: 符號伺服器和網際網路防火牆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2a85a5d0ee2d41e6ffee40bbb275155bdf1e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510428"
---
# <a name="symbol-server-and-internet-firewalls"></a>符號伺服器和網際網路防火牆

某些系統會使用需要驗證所有網際網路流量的網際網路防火牆或 proxy 伺服器。 除非系統使用以透明方式處理驗證的防火牆用戶端，否則符號伺服器的早期版本無法從網際網路存取符號。

從 Dbghelp 6.1 開始，符號伺服器支援需要這類驗證的 proxy 伺服器。 符號伺服器會使用在電腦的 LAN 設定中設定為預設值的任何伺服器。 若要找到此專案，請在主控台中開啟 [ **網際網路選項** **]，** 按一下 [連線] 索引標籤，然後按一下 [ **區域網路設定**] 您也可以按一下 [**工具**] 功能表上的 [**網際網路選項**]，從 Internet Explorer 完成這項操作。 符號伺服器已使用驗證的基本和挑戰回應方法，在許多品牌的 proxy 伺服器上進行測試。

若要為要使用的符號伺服器定義特定的 proxy 伺服器，請將 \_ NT \_ 符號 \_ proxy 環境變數設定為 proxy 伺服器的名稱 (或 IP 位址) ，後面接著埠號碼。 以冒號分隔兩個值。 例如：

**設定 \_NT \_ 符號 \_ PROXY =**_myproxyserver_*_： 80_*

使用 windbg 偵錯工具時，請將符號路徑設定為指向您想要使用的符號存放區。 其中一個差異是系統會顯示一個對話方塊，您必須在此對話方塊中輸入您的使用者識別碼和密碼，才能傳遞至 proxy 伺服器。 如果您輸入不正確的資訊，將會重新顯示對話方塊。 如果您按一下 [ **取消** ] 按鈕，則會關閉對話方塊，並停用符號伺服器以透過網際網路使用。

使用 cdb.exe 或 ntsd.exe 的最新版本時，預設會關閉此功能。 不過，您可以使用！ sym 擴充功能命令來啟用或停用此功能，如下所示：

-   開啟提示輸入使用者識別碼和密碼： **！ sym 提示**。
-   關閉使用者識別碼和密碼： **！ sym 提示關閉** 的提示。

如果您開啟提示，您將需要使用. 重載命令重載符號。

已擴充 DbgHelp API 來支援這些變更。 [**SymbolServerSetOptions**](/previous-versions//ms680676(v=vs.85))函數支援 SSRVOPT \_ PROXY 選項。 如果資料參數為 **Null**，則會使用 [ **網際網路選項** ] 中定義的預設 proxy。 否則，會傳遞以零結束的字串，指定 proxy 伺服器的名稱和埠號碼。 名稱和埠會以冒號分隔，如下所示： *myproxyserver*：80。 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)函數支援 SYMOPT \_ NO \_ 提示選項。 這會關閉從符號伺服器進行驗證的所有提示。

 

 
