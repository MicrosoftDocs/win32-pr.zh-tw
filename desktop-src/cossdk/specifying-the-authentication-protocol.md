---
description: 指定驗證通訊協定
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: 指定驗證通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9bb2ec20df1ec398f32f3a1ee17334c10d9735
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468297"
---
# <a name="specifying-the-authentication-protocol"></a>指定驗證通訊協定

視您網站的安全性需求而定，您可以要求已排入佇列的元件服務一律驗證用戶端的身分識別、永遠不要驗證用戶端的身分識別，或只有在元件已設定為需要驗證時，才會驗證用戶端的身分識別，即使未透過佇列存取也是一樣。

> [!Note]  
> 若要在工作組模式中使用已排入佇列的元件，驗證等級必須設定為 [無]。

 

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

若要指定驗證通訊協定，請使用下列步驟：

1.  在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。

2.  以滑鼠右鍵按一下您要指定驗證通訊協定的佇列應用程式，然後按一下 [ **屬性**]。

3.  在 [屬性] 對話方塊中，選取 [ **佇列** ] 索引標籤。

4.  在 [ **MSMQ 訊息驗證**] 底下，選取與您要執行的驗證通訊協定相關聯的選項按鈕。

5.  按一下 [確定]  。

## <a name="visual-basic"></a>Visual Basic

啟用已排入佇列的應用程式時，請使用 *AuthLevel* 參數，如 [使用佇列名字標記](using-the-queue-moniker.md)中所述。

## <a name="cc"></a>C/C++

啟用已排入佇列的應用程式時，請使用 *AuthLevel* 參數，如 [使用佇列名字標記](using-the-queue-moniker.md)中所述。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[已排入佇列的元件安全性](queued-components-security.md)
</dt> <dt>

[工作組模式中的安全性限制](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



