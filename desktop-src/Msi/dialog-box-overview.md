---
description: 在 Windows Installer 中建立對話方塊的程式，類似于使用 Microsoft Windows API 對話方塊範本，以程式設計方式建立對話方塊的流程。
ms.assetid: c46f6b7b-e78c-4dd8-a4ff-7da5465391f9
title: 對話方塊總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884c85f06bc06588084311aee370700d5b2a5290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319511"
---
# <a name="dialog-box-overview"></a>對話方塊總覽

在 Windows Installer 中建立對話方塊的程式，類似于使用 Microsoft Windows API 對話方塊範本，以程式設計方式建立對話方塊的流程。 當 Windows 對話方塊範本儲存在以 null 結束的字元字串中時，Windows Installer 會將對話方塊參數儲存在對話方塊資料表中。 對話方塊資料表所包含的屬性資料行，類似于 Microsoft Windows 使用者介面 API 中的視窗樣式。 不過，Windows Installer 中的對話方塊樣式位數目是縮減且特製化的集合。

若要使用 Windows 使用者介面 API 實際建立對話方塊，會呼叫 [**對話方塊**](/windows/win32/api/winuser/nf-winuser-dialogboxa) ，並將指標傳遞至範本。 在 Windows Installer 中，此對話方塊會在執行三個 UI 順序資料表的其中一個時建立。

Windows Installer 不包含封裝作者可利用其套件的預設 UI。 它包含一組有限的預設對話方塊，可顯示錯誤和資訊訊息，但只有在 Windows Installer 查詢對話方塊和 UI 順序資料表，且找不到可用的自訂對話方塊時，才會顯示這些對話方塊。

安裝程式 SDK 包含名為 Uisample.msi 的最基本資料庫，其中包含已填入的 UI 和執行順序資料表，以及完整的 UI。 您可以輕鬆地自訂此資料庫，並將其合併至任何套件。

某些標準動作和內部 Windows Installer 錯誤狀況會傳回一組特定的 UI 資料，因此需要有一組特定控制項的對話方塊來容納該資料。 Windows Installer 會檢查兩個不同的位置，以取得這些對話方塊的識別碼。

-   Windows Installer 包含一組內嵌的對話方塊名稱。 自訂動作會查詢對話方塊資料表中的這些保留名稱。
-   在三個 UI 順序資料表中，會顯示序號為-1、-2 或-3 的對話名稱，以回應結束、使用者要求結束，以及來自 Windows Installer 的嚴重錯誤訊息。

您可以在 [對話方塊](dialog-boxes.md)中找到完整的保留主鍵對話方塊名稱清單。 請注意，主要索引鍵對話方塊名稱只會由安裝程式保留，且 Windows Installer 內不會有對話方塊的特定執行。 封裝作者仍然必須填入資料庫中的所有欄位，以指定這些保留對話方塊的屬性和控制項。

 

 
