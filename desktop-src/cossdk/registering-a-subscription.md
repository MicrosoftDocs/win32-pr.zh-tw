---
description: 在 COM + 目錄中註冊事件類別之後，您可以將訂閱者加入至事件類別和訂閱者的訂閱。
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: 註冊訂用帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f152834c805bd905019d2afe0e353c0a962452c32ef144cc3c3d445b59fbbed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547108"
---
# <a name="registering-a-subscription"></a>註冊訂用帳戶

在 COM + 目錄中註冊事件類別之後，您可以將訂閱者加入至事件類別和訂閱者的訂閱。 訂閱可以訂閱單一方法或介面的所有方法。 若要接收對介面的多個方法（但不是每個方法）的呼叫，您必須為想要接收呼叫的每個方法加入訂用帳戶。 元件服務管理工具可以搜尋 COM + 目錄中是否有已註冊的事件類別，這些類別支援訂閱者所執行的介面，並提供您訂閱的選擇。 選擇提供您所需事件的發行者。

若要將訂閱者加入訂閱者元件，請使用下列步驟：

1.  建立新的 COM + 應用程式並安裝訂閱者元件之後，以滑鼠右鍵按一下 [ **訂閱** ] 資料夾，以啟用 [Com + 新增訂閱]。

2.  選擇您要從中接收事件的事件類別。

3.  輸入訂用帳戶名稱。

4.  啟用訂用帳戶。

5.  按一下 [確定]。

當發行者應用程式想要引發事件時，發行者會將事件類別物件具現化，並在其上呼叫方法。 COM + 會搜尋 COM + 類別目錄，以找出所有的訂閱者。 它會建立訂閱者物件 (直接、排入佇列，或使用標記) ，然後在發行者最初進行的方法呼叫中傳遞。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊事件類別](registering-an-event-class.md)
</dt> </dl>

 

 



