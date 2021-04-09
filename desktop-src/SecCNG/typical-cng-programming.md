---
description: CNG API 會執行可延伸的提供者模型，可讓您指定所需的密碼編譯演算法，而不是特定的提供者，以載入提供者。
ms.assetid: a88a089b-4afe-4201-96f7-97f19bce18a1
title: 一般 CNG 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1119da63ca1ea0613444b150914c06664f36c121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690507"
---
# <a name="typical-cng-programming"></a>一般 CNG 程式設計

CNG API 會執行可延伸的提供者模型，可讓您指定所需的密碼編譯演算法，而不是特定的提供者，以載入提供者。 優點是可以取代或升級演算法提供者，而且您不需要以任何方式變更程式碼，就能使用新的提供者。 此外，如果某些演算法在未來判斷為不安全，則可以安裝該演算法的安全版本，而不會影響您的程式碼。 大部分的 CNG Api 都需要提供者或提供者所建立的物件。

使用 CNG API 進行密碼編譯基本作業時所牽涉到的一般步驟如下：

1.  開啟演算法提供者
2.  取得或設定演算法屬性
3.  建立或匯入金鑰
4.  執行密碼編譯作業
5.  關閉演算法提供者

如需詳細資訊，請參閱程式設計範例。

## <a name="opening-the-algorithm-provider"></a>開啟演算法提供者

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)函式會為您提供用於後續 CNG api 的演算法提供者控制碼，例如 [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash)或 [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair)。

## <a name="getting-or-setting-algorithm-properties"></a>取得或設定演算法屬性

您可以使用演算法提供者控制碼來取得演算法的實作為詳細資料，例如金鑰大小或目前的作業模式。 您可以使用 [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) 函數來取得特定屬性。

您也可以修改演算法的屬性。 例如，如果您想要將 ECB 區塊加密連結與 AES 搭配使用，您可以將 AES 演算法的 **BCRYPT \_ 鏈式 \_ 模式** 屬性設定為 **BCRYPT \_ 鏈 \_ 模式 \_ ECB**; 此屬性會指派給使用此演算法控制碼建立的所有 AES 金鑰，而不需要設定每個 aes 金鑰。 您可以使用 [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) 函數來修改這些屬性。

## <a name="creating-or-importing-a-key"></a>建立或匯入金鑰

視您使用的演算法類型而定，您可能需要建立或載入金鑰。 例如， [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) 函式會接受第一個參數的按鍵控制碼。 如果您希望該函式使用對稱式加密演算法（例如 AES）來加密資料，您必須先取得金鑰。 您取得金鑰的方式取決於所使用的演算法類型和金鑰的來源。

您可以使用 [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) 和 [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) 函數來建立暫時金鑰。 您也可以使用 [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) 和 [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) 函數，從記憶體 BLOB 匯入暫時金鑰。

針對保存的金鑰，您可以使用金鑰儲存功能來載入金鑰儲存提供者，然後建立或載入金鑰。 您也可以使用這些函式，藉由傳遞任何容器名稱的 **Null** 來建立或載入暫時金鑰。 如需金鑰儲存功能的詳細資訊，請參閱 [CNG 金鑰儲存功能](cng-key-storage-functions.md)。

## <a name="performing-cryptographic-operations"></a>執行密碼編譯作業

您現在已準備好執行密碼編譯作業，例如分別使用 [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) 或 [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) 函數來加密或解密資料。

## <a name="closing-the-algorithm-provider"></a>關閉演算法提供者

當不再需要提供者時，您必須將控制碼傳遞至 [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) 函式來關閉提供者。 這會導致提供者釋放已配置給該演算法提供者實例的任何資源。 提供者控制碼關閉之後，就無法重複使用。

載入提供者可能是相當耗時的進程。 因此，您應該在應用程式的存留期期間，快取您將參考多次的提供者控制碼。

## <a name="programming-examples"></a>程式設計範例

下列範例說明如何使用 CNG 執行特定的密碼編譯作業。

-   [使用 CNG 建立雜湊](creating-a-hash-with-cng.md)
-   [使用 CNG 簽署資料](signing-data-with-cng.md)
-   [使用 CNG 加密資料](encrypting-data-with-cng.md)

 

 



