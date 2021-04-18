---
description: 您可以使用 [元件服務] 系統管理工具，將已在電腦上註冊的應用程式特定元件匯入至 Windows 登錄中的 COM 元件。
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: 匯入元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468104"
---
# <a name="importing-components"></a>匯入元件

您可以使用 [元件服務] 系統管理工具，將已在電腦上註冊的應用程式特定元件匯入至 Windows 登錄中的 COM 元件。 匯入元件並不會安裝設定介面屬性所需的介面或方法資訊，或是設定遠端用戶端對元件的存取。 因此，可能的話，您應該安裝而非匯入未設定的元件。

> [!Note]  
> 當匯入元件至 COM + 應用程式時，COM + 不會填入元件的介面和方法資訊。 在匯出應用程式 proxy 期間，COM + 將不會提供封送處理資訊 (類型程式庫或 proxy/存根) 適用于部分或所有介面。 匯出包含已匯入元件的應用程式 proxy 將會失敗，或導致發出警告。

 

**將元件匯入至 COM + 應用程式**

1.  在 [元件服務] 系統管理工具的主控台樹中，選取裝載 COM + 應用程式的電腦。

2.  開啟該電腦的 [ **Com + 應用程式** ] 資料夾，然後選取您要在其中安裝元件的應用程式。

3.  開啟應用程式資料夾，然後選取 [ **元件**]。

4.  在 [ **動作** ] 功能表上，指向 [ **新增**]，然後按一下 [ **元件**]。 您也可以用滑鼠右鍵按一下 [ **元件** ] 資料夾，指向 [ **新增**]，然後按一下 [ **元件**]。

5.  在 [COM + 應用程式安裝精靈] 的 [ **歡迎使用** ] 頁面上，按 [ **下一步**]，然後在 [匯 **入或安裝元件** ] 對話方塊中，按一下 **已註冊的 [匯入元件 (s])**。

6.  在 [ **選擇要匯入的元件** ] 對話方塊中，選取 [ **詳細資料** ] 核取方塊以查看已註冊之元件的完整資訊。 從顯示的清單中選取您要匯入的元件 () ，然後按 [ **下一步]**。

7.  按一下 [完成] 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[複製元件](copying-components.md)
</dt> <dt>

[建立新的 COM + 應用程式](creating-a-new-com--application.md)
</dt> <dt>

[刪除 COM + 應用程式](deleting-a-com--application.md)
</dt> <dt>

[安裝新元件](installing-new-components.md)
</dt> <dt>

[移動元件](moving-components.md)
</dt> <dt>

[從 COM + 應用程式移除元件](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



