---
description: 如此一來，訂閱者就可以找到事件類別並訂閱它，事件類別必須在 COM + 類別目錄中註冊。
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: 註冊事件類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688823"
---
# <a name="registering-an-event-class"></a>註冊事件類別

如此一來，訂閱者就可以找到事件類別並訂閱它，事件類別必須在 COM + 類別目錄中註冊。 COM + 需要一個描述事件介面和方法的類型程式庫，讓它能夠適當地比對和連接訂閱者和發行者。 類型程式庫必須位於或隨附于自行註冊的 DLL。

您可以使用 [元件服務] 系統管理工具或 COM + 系統管理功能，在 COM + 類別目錄中註冊事件類別。

**使用元件服務系統管理工具註冊事件類別**

1.  建立新的 COM+ 應用程式。

2.  開啟應用程式資料夾，然後選取 [ **元件**]。

3.  在 [ **動作** ] 功能表上，按一下 [ **新增**]。  (您也可以選取 [ **元件** ] 資料夾、按一下滑鼠右鍵、指向 [ **新增**]，然後按一下 [ **元件**]。 ) 

4.  按一下 [ **安裝新的事件類別 (es])**。

5.  輸入事件類別元件 DLL 的路徑。

6.  按一下 [確定]  。

事件類別會在 COM + 目錄中註冊，並可由有興趣取得事件類別所提供之資訊的訂閱者找到。 如需如何使用 COM + 系統管理介面註冊事件類別的詳細資訊，請參閱 [**ICOMAdminCatalog：： InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊訂用帳戶](registering-a-subscription.md)
</dt> </dl>

 

 



