---
description: 此控制項事件會執行指定的檔案。 如果檔案不存在，或事件失敗，Windows Installer 會將錯誤記錄在詳細資訊記錄檔中，而不會顯示包含錯誤訊息的對話方塊。
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982152d58748ba8b1b8f9d302766e1e9c55eb2ee3c9fa0ce7582507c017dc9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627786"
---
# <a name="msilaunchapp-controlevent"></a>MsiLaunchApp ControlEvent

此控制項事件會執行指定的檔案。 如果檔案不存在，或事件失敗，Windows Installer 會將錯誤記錄在詳細資訊記錄檔中，而不會顯示包含錯誤訊息的對話方塊。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始提供此 ControlEvent。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

引數值的欄位會以空格分隔。 第一個欄位包含指定要執行之檔案的字串值。 使用 filekey 的字串值 \[ \#  \] 來識別檔案，並將 *filekey* 取代 [為檔案](file-table.md)資料表的 file 資料行中顯示的檔案識別碼。 引數的任何剩餘欄位都可以包含正在執行之檔案所使用的參數。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行任何動作。

## <a name="typical-use"></a>一般用法

讓使用者選擇在安裝結束時執行檔案。 此事件可以在安裝的最後一個對話方塊上顯示的 [核取方塊](checkbox-control.md) 控制項設定屬性。 移除套件時不應顯示 CheckBox 控制項。

 

 



