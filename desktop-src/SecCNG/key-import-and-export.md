---
description: 您可以使用 CNG 匯入和匯出對稱金鑰和非對稱金鑰。 您可以使用金鑰匯出和匯入功能，在機器之間移動金鑰。
ms.assetid: 37bda1e0-5dd2-455c-9627-4e7e1b0e04d3
title: 金鑰匯入和匯出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a4b6c26069911d771697bf06f7464aa14ab7f099e4a0e06991d2fd992efa44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907699"
---
# <a name="key-import-and-export"></a>金鑰匯入和匯出

您可以使用 CNG 匯入和匯出 [*對稱金鑰*](/windows/desktop/SecGloss/s-gly) 和非對稱金鑰。 您可以使用金鑰匯出和匯入功能，在機器之間移動金鑰。

## <a name="symmetric-keys"></a>對稱金鑰

若要匯入或匯出對稱式 (或會話) 金鑰（其中使用相同的金鑰來加密和解密部分資料），您可以使用 [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) 和 [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) 函數。 一般來說，您會先使用 **BCryptExportKey** 函式來匯出索引鍵，然後再使用 **BCryptImportKey** 函數進行匯入。 這些函式是設計用來啟用使用 *hExportKey* 和 *hImportKey* 參數加密匯出和匯入的金鑰;不過，Microsoft 對這些函式的執行不支援加密匯出和匯入的金鑰。

## <a name="asymmetric-keys"></a>非對稱金鑰

若要匯入非對稱式 (或 [*公開/私*](/windows/desktop/SecGloss/p-gly) 用) 金鑰組，其中一個金鑰會用來加密，另一個則用來解密某些資料，您可以使用 [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) 或 [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) 函數的其中一個。 CNG 提供者必須使用支援的 [*金鑰 BLOB*](/windows/desktop/SecGloss/k-gly) 類型，對金鑰組進行編碼。 [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) 可以用來建立編碼的金鑰 BLOB。 [CNG 結構](cng-structures.md)描述 Microsoft key 儲存體 Provider 所支援的主要 BLOB 類型和結構。

若要讓 [**BCryptExportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptexportkey) 建立保存的金鑰組，輸入金鑰 BLOB 必須包含 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)。 [*公開金鑰*](/windows/desktop/SecGloss/p-gly) 不會保存。

金鑰名稱和匯出原則不是 [CNG 結構](cng-structures.md)中所定義之 [*BLOB*](/windows/desktop/SecGloss/b-gly)結構的一部分。 但是，如果 BLOB 的 BLOB 類型不是不透明的， (例如內部金鑰狀態) 的記憶體映射，則 BLOB 可能會包含金鑰名稱和匯出原則屬性。

下列程式說明如何使用其屬性匯入保存的私密金鑰。

**匯入保存的金鑰**

1.  使用 [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) 函數建立保存的金鑰。
2.  使用 [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) 函式，在金鑰組象上設定任何所需的屬性。
3.  將 [匯入金鑰 BLOB] 設定為索引鍵上的屬性，並將 BLOB 類型設定為 [屬性名稱]。
4.  使用 [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) 函數完成保存的金鑰匯入。

 

 
