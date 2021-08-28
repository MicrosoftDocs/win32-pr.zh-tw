---
description: 有一些威脅防護技術可供您使用，以提供更安全的密碼。
ms.assetid: b2442579-e559-4053-869f-9d96e4db202e
title: 威脅緩和技巧
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 315a79ec1db48a16de858d655bd1550fa1458720
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482444"
---
# <a name="threat-mitigation-techniques"></a>威脅緩和技巧

有一些威脅防護技術可供您使用，以提供更安全的密碼。 這些技術是使用下列四種主要技術的一或多個來實行。



| 技術                      | 描述                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CryptoAPI                       | CryptoAPI 提供一組功能，可協助您將密碼編譯常式套用至目標實體。 CryptoAPI 可以提供雜湊、摘要、加密和解密，以提及其主要功能。 CryptoAPI 也有其他功能。 若要瞭解密碼編譯和 CryptoAPI，請參閱 [密碼編譯基本](/windows/desktop/SecCrypto/cryptography-essentials)資訊。           |
| 存取控制清單            |  (ACL) 的 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) 是適用于物件的安全性保護清單。 物件可以是檔案、進程、事件，或是具有安全描述項的任何其他專案。 如需 Acl 的詳細資訊，請參閱)  (Acl 的 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists) 。 |
| 資料保護 API             |  (DPAPI) 的資料保護 API 提供下列四個函式，用來加密和解密機密資料： [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata)、 [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata)、 [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)和 [**CryptUnprotectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory)。                  |
| 儲存的使用者名稱和密碼 | 儲存體的功能，可處理使用者的密碼和其他認證，例如私密金鑰、更簡單、更一致且更安全。 如需此功能的詳細資訊，請參閱 [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa)。                                                                                                         |



 

這些技術在所有作業系統上都無法使用。 因此，安全性可以改善的範圍取決於所涉及的作業系統。 以下是每個作業系統所提供的技術。


| 作業系統 | 技術 | 
|------------------|------------|
| Windows Server 2003 和 Windows XP | <ul><li>CryptoAPI</li><li>存取控制清單</li><li>資料保護 API</li><li>儲存的使用者名稱和密碼</li></ul> | 
| Windows 2000 | <ul><li>CryptoAPI</li><li>存取控制清單</li><li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></li><li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></li></ul> | 




 

下列威脅防護技術會使用四種技術中的一或多個技術。 不能使用不包含在作業系統中的技術需要使用的技術。

## <a name="getting-passwords-from-the-user"></a>從使用者取得密碼

當您允許使用者設定密碼時，請強制使用強式密碼。 例如，要求密碼必須是最小長度，例如八個字元以上。 密碼也必須包含大寫和小寫字母、數位和其他鍵盤字元，例如貨幣符號 ($) 、驚嘆號 (！ ) 或大於 (>) 。

取得密碼之後，您可以快速地 (使用盡可能少的程式碼) ，然後清除密碼的所有 vestiges。 這可將入侵者可用來「陷阱」密碼的時間降到最低。 這項技術的取捨是必須從使用者抓取密碼的頻率。不過，您應該盡可能採用此原則。 如需如何正確取得密碼的相關資訊，請參閱 [要求使用者提供認證](asking-the-user-for-credentials.md)。

避免提供「記住我的密碼」使用者介面選項。 通常，使用者會要求使用此選項。 如果您必須提供，則至少要確保密碼會以安全的方式儲存。 如需詳細資訊，請參閱本主題稍後的「儲存密碼」一節。

限制密碼輸入嘗試。 在特定次數的嘗試次數沒有成功之後，請將使用者鎖定一段時間。 （選擇性）延長每次嘗試的回應時間上限。 這項技術的目標是要失去猜測攻擊。

## <a name="storing-passwords"></a>儲存密碼

絕對不要將密碼以純文字格式儲存 (未加密的) 。 加密密碼可大幅提高安全性。 如需有關儲存加密密碼的詳細資訊，請參閱 [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata)。 如需有關在記憶體中加密密碼的詳細資訊，請參閱 [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)。 將密碼儲存在盡可能少的位置。 儲存密碼的位置愈多，入侵者可能會發現它的機率就愈大。 絕對不要將密碼儲存在網頁或網頁檔案中。 將密碼儲存在網頁或網頁檔案中，可讓使用者輕鬆遭到入侵。

加密密碼並儲存密碼之後，請使用安全的 Acl 來限制檔案的存取權。 或者，您也可以將密碼和加密金鑰儲存在可移動裝置上。 在卸載式媒體（例如智慧卡）上儲存密碼和加密金鑰，有助於建立更安全的系統。 針對指定的會話取出密碼之後，就可以移除該卡片，藉此移除入侵者可以取得存取權的可能性。

 

 
