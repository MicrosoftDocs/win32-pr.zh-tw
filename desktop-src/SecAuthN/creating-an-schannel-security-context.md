---
description: 說明如何建立安全性內容，以保護用戶端與伺服器之間的通訊。
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: 建立 Schannel 安全性內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e364e6319fbaddb50bffaf59541af9e8f43bfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986928"
---
# <a name="creating-an-schannel-security-context"></a>建立 Schannel 安全性內容

若要建立可保護用戶端和伺服器之間通訊的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) ，這兩者都必須參與下列資訊交換流程：

## <a name="client"></a>用戶端

1.  用戶端會呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函數。
2.  Schannel 會根據所選安全性通訊協定的規則開始建立安全性內容。 函數的傳回碼會指出用戶端是否必須再次呼叫函式。 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 可能會傳回代表內容的權杖。
3.  如果傳回權杖，用戶端會將它傳送至伺服器。
4.  [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)傳回 SEC \_ E OK 時 \_ ，用戶端就完成了。 如果函式傳回每 \_ 秒 \_ 繼續 \_ 需要的時間，用戶端必須等待伺服器傳送權杖給它。 當用戶端具有來自伺服器的權杖時，它必須再次呼叫 **InitializeSecurityCoNtext (一般)** [*函數*](/windows/desktop/SecGloss/c-gly) 。  (返回步驟 2. ) 

## <a name="server"></a>伺服器

1.  伺服器會等候用戶端傳送包含安全性權杖的訊息。 伺服器會將接收自用戶端的權杖傳遞至 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式。
2.  Schannel 是以權杖所代表的部分安全性內容為基礎。 Schannel 會將權杖傳回給伺服器，並傳回指出伺服器是否必須再次呼叫函式的傳回碼。
3.  如果傳回了權杖，伺服器會將它傳送給用戶端。
4.  當 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 傳回 SEC \_ E \_ OK 時，伺服器就完成了。 如果函式傳回每 \_ 秒 \_ 繼續需要的時間，則 \_ 伺服器必須等待用戶端傳送權杖給它。 當伺服器具有來自用戶端的權杖時，它必須再次呼叫 **AcceptSecurityCoNtext (一般)** 函數。  (返回步驟 2. ) 

如果任一個函式傳回 SEC E OK 以外的值 \_ \_ ， \_ \_ 就會繼續 \_ 需要 sec 或 sec \_ e \_ 未完成 \_ 的訊息 (請參閱下列段落) 發生錯誤。 用戶端和伺服器應呼叫 [**DeleteSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) 函數，以刪除部分建立的安全性內容。

可以改變用戶端和伺服器處理的特殊案例，就是從其他一方傳送太少或太多的資訊給用戶端或伺服器。 如果資訊太少，這兩個函式會傳回 SEC \_ E \_ 未完成 \_ 的訊息。 如需辨識和處理不足或超過資訊的相關資訊，請參閱 [Schannel 傳回的額外緩衝區](extra-buffers-returned-by-schannel.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Schannel 執行驗證](performing-authentication-using-schannel.md)
</dt> <dt>

[對應憑證](mapping-certificates.md)
</dt> <dt>

[手動驗證 Schannel 認證](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
