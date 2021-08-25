---
title: 使用索引標籤控制項
description: 本主題包含兩個使用索引標籤控制項的範例。
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a373a1d7d1fc44da851480841aab04bf364b27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465265"
---
# <a name="using-tab-controls"></a>使用索引標籤控制項

本主題包含兩個使用索引標籤控制項的範例。 第一個範例示範如何使用索引標籤控制項，在應用程式主視窗中的多個文字頁面之間切換。 第二個範例示範如何使用索引標籤控制項，在對話方塊中的多個控制項頁面之間切換。

## <a name="in-this-section"></a>本節內容




| 主題 | 描述 | 
|-------|-------------|
| <a href="create-a-tab-control-in-the-main-window.md">如何在主視窗中建立索引標籤控制項</a><br /> | 本節中的範例將示範如何建立索引標籤控制項，並將其顯示在應用程式主視窗的工作區中。 應用程式會在索引標籤控制項的顯示區域中，顯示 (靜態控制項) 的第三個視窗。 父視窗在處理 <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> 訊息時，會定位並調整索引標籤控制項和靜態控制項的大小。 <br /> 此範例中有七個索引標籤，一周的每一天都有一個。 當使用者選取索引標籤時，應用程式會在靜態控制項中顯示對應日期的名稱。 <br /> | 
| <a href="create-a-tabbed-dialog-box.md">如何建立索引標籤式對話方塊</a><br /> | 本節中的範例將示範如何建立使用 tab 鍵來提供多個控制項頁面的對話方塊。 主要對話方塊是強制回應對話方塊。 每一頁的控制項都是由具有 <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> 樣式的對話方塊範本所定義。 選取索引標籤時，就會為傳入頁面建立非強制回應對話方塊，並終結傳出頁面的對話方塊。 <br /><blockquote>[!Note]<br />在許多情況下，您可以使用屬性工作表更輕鬆地執行多頁對話方塊。 如需屬性工作表的詳細資訊，請參閱 <a href="property-sheets.md">關於屬性工作表</a>。</blockquote><br /> 主要對話方塊的範本只會定義兩個按鈕控制項。 處理 <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> 訊息時，對話方塊程式會建立一個索引標籤控制項，並為每個子對話方塊載入對話方塊範本資源。 <br /> | 




 

