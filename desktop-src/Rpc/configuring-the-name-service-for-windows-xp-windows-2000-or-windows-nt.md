---
title: 設定名稱服務
description: 從 Windows 2000 開始，當您安裝 Windows SDK 時，安裝程式會自動選取 Microsoft 定位器作為名稱服務提供者。 您可以透過主控台變更名稱服務提供者。
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462201"
---
# <a name="configuring-the-name-service"></a>設定名稱服務

從 Windows 2000 開始，當您安裝 Windows SDK 時，安裝程式會自動選取 Microsoft 定位器作為名稱服務提供者。 您可以透過主控台變更名稱服務提供者。

執行 nsid 的主機電腦會作為 DCE Cell Directory 服務的閘道，並在執行 Microsoft 作業系統和 DCE 電腦的電腦之間傳遞 NSI 函式呼叫。 網路位址最多可有80個字元，例如，11.1.9.169 是有效的位址。

> [!Note]  
> 您必須擁有數位設備公司的 DCE CD 產品，才能將 DCE CD 設定為您的名稱服務提供者。 請參閱數位設備公司提供的檔，以取得 DCE CD 的相關資訊。

 

**重新設定名稱服務提供者**

1.  在主控台中，按一下 [ **網路** 連線] 圖示。 [ **網路** 連線] 視窗隨即出現。
2.  選取要設定的網路連線，按一下滑鼠右鍵， **然後從操作** 功能表中選取 [內容]。 [ **連接屬性** ] 對話方塊隨即出現。
3.  在 [ **連接屬性** ] 對話方塊中，選取 [ **Microsoft 網路用戶端** ]，然後按一下 [ **屬性** ] 按鈕。 [ **Microsoft 網路的用戶端屬性** ] 對話方塊隨即出現。
4.  在 [ **Microsoft 網路的用戶端] 屬性** 對話方塊中，開啟 [ **名稱服務提供者** ] 下拉式清單，並從清單中選取名稱提供者。
    1.  當您選取 [Microsoft 定位器] 時，按一下 [確定]。 完成設定程式。
    2.  當您選取 [DCE Cell Directory 服務，請在 [ **網路位址** ] 方塊中，輸入執行 NSI daemon (nsid) 的主電腦名稱稱，然後按一下 [確定]。

**重新設定 Windows 2000 的名稱服務提供者**

1.  在主控台中，按一下 [ **網路** ] 圖示。

    [ **網路** ] 對話方塊隨即出現。

2.  在 [ **網路** ] 對話方塊中，按一下 [ **設定**]。
3.  在 [ **NetworkSoftware** ] 清單中選取 [ **RPC** 設定]。

    [ **RPC 名稱服務提供者** 設定] 對話方塊隨即出現。

4.  在 [ **RPC 名稱服務提供者** 設定] 對話方塊中，從清單中選取名稱服務提供者。
    1.  當您選取 [Microsoft 定位器] 時，按一下 [確定]。 完成設定程式。
    2.  當您選取 [DCE Cell Directory 服務，請在 [ **網路位址** ] 方塊中，輸入執行 NSI daemon (nsid) 的主電腦名稱稱，然後按一下 [確定]。

 

 




