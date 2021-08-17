---
title: OBJID_QUERYCLASSNAMEIDX 的附錄 F 物件識別碼值
description: 當 OLEACC 傳送 \_ lParam 參數設定為 OBJIDQUERYCLASSNAMEIDX 的 WM GETOBJECT 訊息時，許多標準使用者或通用控制項 (COMCTL) 會傳回下列其中一個值。
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22368f15fa40e30f909f9ad838cb478ed1e9a9c9ff25929f63bb91ec99e99b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134031"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a>附錄 F： OBJID QUERYCLASSNAMEIDX 的物件識別碼值 \_

當 OLEACC 傳送 *lParam* 參數設定為 OBJIDQUERYCLASSNAMEIDX 的 [**WM \_ GETOBJECT**](wm-getobject.md)訊息時，許多標準使用者或通用控制項 (COMCTL) 會傳回下列其中一個值。



| 使用者或通用控制項 | 傳回值 |
|------------------------|--------------|
| Listbox                | 65536 + 0      |
| Button                 | 65536 + 2      |
| 靜態                 | 65536 + 3      |
| 編輯                   | 65536 + 4      |
| Combobox               | 65536 + 5      |
| 捲軸              | 65536 + 10     |
| 狀態                 | 65536 + 11     |
| 工具列                | 65536 + 12     |
| 進度               | 65536 + 13     |
| 動畫                | 65536 + 14     |
| 索引標籤                    | 65536 + 15     |
| 熱鍵                 | 65536 + 16     |
| 標頭                 | 65536 + 17     |
| 跟蹤               | 65536 + 18     |
| Listview               | 65536 + 19     |
| 上下按鈕                 | 65536 + 22     |
| 提示               | 65536 + 24     |
| Treeview               | 65536 + 25     |
| RichEdit               | 65536 + 28     |



 

只有使用者和 Windows 通用控制項 (COMCTL) 會傳回資料表中的其中一個值。 如果視窗傳回0以回應此訊息，則視窗可以是下列其中一項：

-   自訂控制項
-   上表中一個控制項以外的控制項
-   無法辨識 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息的舊版系統控制項

如果視窗傳回0，用戶端可能需要使用 [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) 或 [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)。 您可以使用這些函式來判斷以類別名稱為基礎的控制項類型。

一般而言，用戶端可以使用 OLEACC 所提供的資訊。

 

 